# Claude Brain — Project Start Here
*Read this first at the start of any brain architecture session.*

---

## The Project
**The Quadriune Brain — A multi-agent AI architecture modeled on how the brain actually works.**
Collaborators: Randy Evans + Claude + Del (technical builder)
Status: Conceptual foundation complete. Domain Specs not yet written. Actual Quadriune architecture not yet sorted. Del building proof of concept on his own 3 agent harness.

---

## The Core Idea
Four purpose-built AI agents — not fine-tuned general models — each trained exclusively on a specific cognitive domain. A fifth element (the routing layer / global workspace) that is empty by design. Together: an AI system that models how a mind works, not how people imagine a mind works.

The four agents map directly to Randy's four foundations:
- **Layer 1 — Reptilian (Brainstem):** Threat, survival, resource, territorial. Present-state only.
- **Layer 2 — Mammalian (Limbic):** Attachment, emotional memory, social bonding, relational safety.
- **Layer 3 — Cortical (Neocortex):** Reasoning, analysis, language, planning.
- **Layer 4 — Narrator (DMN):** Self-referential narrative, autobiographical memory, future simulation.

**The routing layer is NOT a fifth agent.** It is empty of content. It reads system state and applies context-dependent priority rules. Holarchy, not hierarchy.

---

## Leading Design Principles
*Current best thinking, held loosely. These are the strongest candidates so far, not settled architecture. Any one of them is open to challenge and several will probably change once the Domain Specs get written.*

**Purpose-built, not fine-tuned.** Fine-tuning a general model produces a costume. Training from scratch on a curated corpus produces a character. Each agent must genuinely not know the other domains.

**Holarchy not hierarchy.** Priority is context-dependent, not rank-based. The reptilian layer has veto power under threat conditions. The DMN has default advantage at idle. Neither rules permanently.

**Global Workspace Theory (Baars).** The routing layer is a broadcasting mechanism. When an agent wins workspace access, its output goes to ALL agents simultaneously — not routed to one. The workspace has no content of its own.

**Two operating modes.** Normal mode (standard priority rules) and Psychedelic mode (DMN suppressed, lower agents get amplified access). Same agents, different routing rules. This is testable.

**The failure mode.** Del's three-agent experiment: Claude asserted dominance through verbal fluency. Verbal dominance ≠ domain authority. The routing layer must be outside the agent conversation — never a participant.

**Plato's Cave / the light.** The routing layer is the geometry of the cave — not a prisoner, not the fire, but the structural relationship that determines what gets cast as shadow. Cannot see itself from inside the system.

---

## The Harness (`~/.ccb`)

A running multi-agent setup lives on Randy's Mac at `~/.ccb`, driven through WezTerm. Read what it actually is before assuming it implements anything described above.

It is not Del's build. It is Claude Code Bridge (ccb) v5.2.6, open-source software at github.com/bfly123/claude_code_bridge, MIT licensed, with public documentation. Del installed and configured it. Four independent CLI processes in four WezTerm panes: Claude, Codex, Gemini, OpenCode. None of the Quadriune structure is in it: no layer specs, no purpose-built models, no mode switching.

What ccb does contain, installed and dormant, is a SQLite-backed blackboard with typed entries, permission tiers, a broadcast primitive restricted to Claude or the cofounder, and blind debate with a controlled reveal. The ledger database has never been created, so none of it has ever run. See `ccb-primer.md` in this folder.

The Quadriune framework was chosen for two reasons. A non-neuroscientist can hold it in their head, and it mapped cleanly onto the 3 agent system Del already had. It gave Del a shape to think in. That was the point of it: a proof of concept move, scaffolding for shared understanding.

The actual architecture of the Quadriune brain has yet to be sorted. Treat the framework as vocabulary that earned its place by being teachable. Treat the architecture as open.

---

## Key Documents
- `Manifesto.md` — The philosophical and theoretical foundation
- `Lab_Notebook.md` — Chronological working notes, experiments, open questions
- `Del_Briefing.md` — Synthesized briefing for Del to get up to speed
- `Domain_Specs/README.md` — Placeholder; writing these is the next core task
- `Claude Shorts/` — Now lives in its own workspace: `/Users/randallevans/Claude MAIN/Claude Shorts/`
- `Claude Somatic/` — Separate workspace on the felt sense and the carbon / silicon interface. Open problem 6 below is a live seam between the two projects.
- `ccb-primer.md` — What the harness in `~/.ccb` actually is: upstream software, what is running, and what is installed but never initialized.

---

## Open Problems
1. **Domain Specs** — What specifically constitutes reptilian vs mammalian behavior? Where are the hard edges? Writing these will reveal where the thinking is solid vs hand-wavy. **This is the next priority.**
2. **The architecture itself** — The four-layer split is a teaching frame that mapped onto Del's existing 3 agent system. Whether it is also the right structure to build is unanswered. What would falsify it? What would a better decomposition look like?
3. **Routing layer implementation** — Assuming a routing layer survives, rule-based heuristics or trained classifier? Who writes the initial rules? How to verify it's working correctly?
4. **The input interface** — How does the world present problems to the system? Raw input, domain classification first, then response (oracle not tool).
5. **Training approach** — Practical path to from-scratch training for smaller purpose-built models.
6. **The missing body** — The reptilian layer does threat and survival with no afferent body attached to it, which is a strange thing for a survival layer to lack. The somatic channel worked on in `Claude Somatic/` may be that missing input, which would make these two projects one project approached from two ends. See `Claude Somatic/_START_HERE.md`, open question 5.
7. **Psychedelic-state simulation** — Two operating modes as a research tool. Testable with identical inputs run through both modes.

---

## Commercial Application
**The Ian Use Case:** Ian (Phillip's friend from Harvard, now Blackstone satellite office in SF) is the target user for a hedge fund application. The exploitable market inefficiency at elite levels is interpretive, not informational. The system's first output is a layer diagnosis — which cognitive layer is currently driving market behavior. This is the proving ground.

See memory file: `project_ian.md`

---

## Collaborators
- **Randy Evans** — conceptual architect, psychedelic medicine physician
- **Del** — technical builder, proof-of-concept (currently in DC for SOF Week follow-up)
- **Claude** — thinking partner, documentation

---

## Note on Claude Shorts
The animated educational series (The Quadriune) now lives in its own workspace at `/Users/randallevans/Claude MAIN/Claude Shorts/`. Nothing for it remains staged in this folder.

---

*Last updated: June 2026*
