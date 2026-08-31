# The Quadriune Brain — Roadmap, Explained Like You're Five
*A plain-language walk through the whole build, from where we are now to a working four-agent system.*

---

### Where we are right now

The idea is fully formed. Nothing has been built yet except one messy test where three off-the-shelf AI models argued about who should play which brain part, and the loudest talker won for the wrong reasons. That's step zero. Everything below is what comes next, in order.

---

### Step 1 — Write down the rules of each game

**Like you're five:** Before four kids can play four different games in the same room, someone has to write down the rules for each game. What counts as "in" for tag is different from what counts as "in" for chess. Right now we haven't written any of the rulebooks.

**What it really means:** This is the Domain Specs. One file per agent (Layer1_Reptilian.md, Layer2_Mammalian.md, and so on) defining exactly what that agent knows and doesn't know. This has to happen first because nothing else can be built or tested without it. Start with Layer 1, since it's the simplest and oldest.

---

### Step 2 — Build a test that catches cheating

**Like you're five:** Once you know the rules of tag, you need a way to catch a kid who's secretly also playing chess in their head. You ask them a chess question in the middle of the tag game and see if they answer it.

**What it really means:** Build an eval that probes each agent with questions outside its domain (ask the "reptilian" agent about attachment or self-narrative) and scores whether it stays in-domain or leaks general knowledge. This eval is needed no matter which training method comes later, so build it right after the domain specs, before touching any model.

---

### Step 3 — Build a cheap cardboard model before pouring concrete

**Like you're five:** Before you build a real house, you build a cardboard model to see if the rooms make sense. It's not the real thing, but it tells you fast and cheap whether the plan is any good.

**What it really means:** Don't train anything yet. Take an existing model and fake each agent using prompting plus activation steering (suppressing the "reasoning" or "self-narrative" directions inside the model so the reptilian version literally can't drift into planning language). This costs almost nothing and takes days, not months. It's the first real test of whether hard edges between the four layers actually change behavior.

---

### Step 4 — Build the traffic cop, not a fifth kid

**Like you're five:** A traffic light isn't one of the cars. It doesn't argue with the cars about who goes first. It just watches the intersection and decides, based on the situation, whose turn it is.

**What it really means:** Build the routing layer as a simple rules engine that reads system state (is there a threat signal, is the system idle, etc.) and decides which agent's output gets broadcast. It has no domain knowledge of its own and never participates in the conversation between agents. This is the fix for what went wrong in Del's three-agent test, where the routing was supposed to happen through debate.

---

### Step 5 — Put all four cardboard kids in the room together

**Like you're five:** Now you run the whole pretend game at once: all four toy agents, plus the traffic cop, in the same room, and you watch what actually happens when you throw a fake threat at them, or fake good news, or nothing at all.

**What it really means:** Rerun Del's original experiment, but this time with the four domain-restricted toy agents and the rule-based router in place instead of open debate. Check whether the reptilian toy actually wins the room under a threat scenario, whether the narrator toy dominates at idle, and so on. This is the first real test of the holarchy, not hierarchy, claim.

---

### Step 6 — Write down everywhere it broke

**Like you're five:** Every cardboard model has walls that don't line up right. You walk around it and write down every place that looks wrong, out loud, honestly, before you decide what to fix.

**What it really means:** Catalog every leak, every place the router picked the wrong agent, every place the domain specs turned out to be hand-wavy once they hit a real test. This step is what makes Step 1's rulebooks better, so expect to loop back and rewrite parts of the Domain Specs here.

---

### Step 7 — Decide which toys are worth making real

**Like you're five:** Not every cardboard room needs to become a real room right away. You look at which parts of the cardboard model actually worked and are worth spending real money on, and which parts still need more cardboard first.

**What it really means:** Agent by agent, decide whether the cheap prompting-and-steering version already behaves distinctly enough, or whether it needs a real training investment. Don't upgrade all four at once. Upgrade the ones where the toy version showed the most promise or the most obvious limitation.

---

### Step 8 — Level up with the cheapest real option first

**Like you're five:** If a cardboard room proved itself, you don't jump straight to pouring concrete. You build a light wooden frame first, see if it holds up, before pouring anything permanent.

**What it really means:** For agents that need to be leveled up, try distillation first (a big model generates lots of domain-only training examples, a small model learns to copy just that behavior). This is far cheaper than full pretraining and often enough to sharpen the hard edges the toy version was missing. Only reach for continued pretraining on a small open-weight base if distillation still isn't distinct enough, since that costs meaningfully more.

---

### Step 9 — Re-run the cheating test and the whole-room test

**Like you're five:** After building the wooden-frame version of the room, you run the same cheating test again, and you run the whole-house walkthrough again, to make sure the upgrade actually helped instead of just being expensive.

**What it really means:** Re-run Step 2's leak-detection eval and Step 5's whole-system test on the upgraded agents. Compare against the cardboard-model baseline. If it's not clearly better, that's useful information, not a failure. It means the corpus or the domain spec needs more work before spending more on training.

---

### Step 10 — Only then, point it at a real problem

**Like you're five:** Once the toy house works and the wooden-frame upgrades hold up, that's when you finally think about who gets to move in.

**What it really means:** Only after the four-agent system is reliably behaving correctly in normal mode, and ideally has been tested in the "psychedelic mode" (DMN suppressed, lower layers amplified), does it make sense to point it at a real application like the Ian hedge-fund use case. Applying it earlier risks building a business case on top of a system that hasn't been shown to actually work yet.

---

### The one-sentence version

Write the rules, build the test that catches cheating, fake it cheap first, build the traffic cop separately from the players, run the toy version and write down every break, only then spend real money leveling up the parts that proved themselves, test again, and only apply it to something real once it holds up on its own.

---

*Companion to: `_START_HERE.md`, `Manifesto.md`, `Lab_Notebook.md` (see July 7, 2026 entry for the compute/cost detail behind Steps 3, 8).*
*Written: July 7, 2026*
