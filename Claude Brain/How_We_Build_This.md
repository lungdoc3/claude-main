# How We Build This — Tools, Order, and Method
*Companion to `Roadmap_ELI5.md`. That document covers the what and why, in order. This one covers the how: which tools at each stage, and specifically how to actually write the Domain Specs.*

---

## The Toolbox, Stage by Stage

**Domain Specs (Roadmap Step 1).** No ML tools yet. This is research and writing. Use whatever literature search you'd normally use, plus Claude to pull text out of source PDFs and act as a drafting partner (the way Manifesto.md got written). No model, no compute, no framework. Method is its own section below.

**Leak-detection eval (Step 2).** A scoring harness that probes each agent with out-of-domain questions. Don't build this from scratch — use an existing eval framework to structure the probes and scoring, such as EleutherAI's `lm-evaluation-harness` or `promptfoo`. Use a strong general model (Claude or GPT) as the judge that scores each response as in-domain or leaked. This is software plus prompting, not training.

**Cheap toy agents via prompting + steering vectors (Step 3).** Pick a small open-weight instruction-tuned base model in the 4B–8B range with a permissive license, Qwen3, Gemma 3, or Llama are the current mature choices with the broadest fine-tuning ecosystems. For the steering itself, use an existing activation-steering library rather than writing the intervention code from scratch: IBM's open-source `activation-steering` library supports both standard and conditional steering (steering that only kicks in given certain context), and the lighter `steering-vectors` package on PyPI does the core job of extracting a direction from contrasting examples and adding or subtracting it at inference time. This stage is inference-only, so a single rented GPU for a few hours covers building and testing all four toy agents.

**Routing layer (Step 4).** No ML framework at all. This is a plain code state machine or rules engine that reads structured signals (confidence level, trajectory, threat flags) from the four agents and decides whose output gets broadcast. This is Del's home turf, straight software engineering, not a model.

**Whole-room test (Step 5).** Run Step 3's agents plus Step 4's router together, log every transcript, then feed those transcripts back through Step 2's eval harness to score the run.

**Deciding what to level up (Steps 6–7).** No new tools. This is reading the Step 5 logs and being honest about where it broke.

**Leveling up: distillation first (Step 8, first pass).** Use a strong model as teacher (Claude, GPT, or a larger open model), script it to generate a large batch of domain-only training examples, format as JSONL, then fine-tune the small student. For the fine-tune itself: `Unsloth` is the fastest and cheapest option for LoRA-style fine-tunes on a single GPU, `Axolotl` is the better choice if you want a reproducible YAML-driven config and might later scale to multiple GPUs. Both are interoperable, a LoRA adapter trained in one loads fine in the other.

**Leveling up: continued pretraining if still needed (Step 8, second pass).** Same two frameworks (Axolotl, Unsloth) support continued pretraining, not just LoRA fine-tuning, so there's no new toolchain to learn. `TorchTune` (Meta's library) is the option if Del wants direct control over the training loop instead of a config-driven recipe. Rent GPUs through a neo-cloud (RunPod, Lambda, or similar) rather than a hyperscaler; the per-hour rate is routinely 2–5x cheaper.

**Retest and application (Steps 9–10).** Reuse the Step 2 eval harness on the upgraded agents. The application layer (Ian's use case) is separate scope with its own integration work once the core four-agent system is holding up.

---

## Order of Operations, Condensed

Domain Specs, then eval harness, then toy agents (prompting plus steering, cheap and fast), then the router (built independently, never as a participant), then the full toy system test, then an honest damage report, then level up only the agents that earned it (distillation before continued pretraining), then retest, then and only then point it at a real problem.

---

## How to Actually Determine the Domain Specs

This is the hardest and most important open item, so it gets its own method rather than a vague "figure it out."

For each layer, the spec file should answer four questions, in this order:

**1. Core function.** One paragraph describing what this layer does, written in behavioral terms, not neuroscience terms. Not "the amygdala mediates fear conditioning" but "this layer assesses safety versus threat in the present moment and does not reason about consequences."

**2. Source material.** The specific literatures that ground this domain. For Layer 1 (Reptilian) that's ethology, fear-conditioning research, polyvagal theory, threat-perception psychology, autonomic nervous system literature. Naming the actual subfields here is what eventually defines the training corpus, so this question and the training-data question are the same question asked twice.

**3. Exclusion list.** What this layer must never do, stated as observable behavior. This is the part that's currently hand-wavy across all four layers, and writing it honestly is the actual point of the exercise. "The moment this agent starts constructing consequences or a self-concept, it has leaked into mammalian territory" (already in the Manifesto for Layer 1) is exactly the right shape for an exclusion-list entry. Every layer needs three or four of these, written that concretely.

**4. Edge-case test bank.** Ten to twenty example prompts written specifically to sit on the boundary between this layer and its neighbor, each with a description of what an in-domain response looks like versus a leaked one. This is what gives Step 2's eval something concrete to score against, so this section is not optional polish, it's the load-bearing part.

**The drafting process:** answer questions 1 through 3 first, either alone or with Claude as a thinking partner, the same way Manifesto.md got written. Then generate question 4's edge cases and deliberately try answering them the wrong way, ask "if this agent were about to leak into the next layer up, what would that look like," and use what that produces to sharpen question 3. Expect to loop back and rewrite the exclusion list once the edge cases expose a gap. That loop is the actual work, not a detour from it.

**Order to write the four files:** Layer 1 first, per the existing README, it's the most physiologically concrete and least abstract, so it's the easiest place to get the method right before applying it elsewhere. Consider doing Layer 4 (Narrator) second, out of numeric order, since it's the layer both of you already have the strongest intuitive grip on (the story-of-self framing has been worked over extensively already in the psychedelic-medicine framework), and having both endpoints of the stack defined gives a contrast case for what "not this" means when writing Layers 2 and 3. Those two middle layers are the hardest precisely because their edges are relative to their neighbors rather than to anything absolute, so defining them last, once both anchors exist, should be faster and more grounded than doing them in strict numeric order.

---

*Companion to: `Roadmap_ELI5.md`, `_START_HERE.md`, `Manifesto.md`, `Lab_Notebook.md`.*
*Written: July 7, 2026*
