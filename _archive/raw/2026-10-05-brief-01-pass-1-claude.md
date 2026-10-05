Read complete: CLAUDE.md, RULES-OF-ENGAGEMENT.md, HOUSE.md, the brief, and the one file it cites (`information-theory-and-presentation.md`). Per HOUSE.md I am **Placebo** (Claude Code / Opus 4.8), assigned the **Structural** stance for Brief 01. No files created or changed, so nothing to commit.

CCB_BEGIN: 20261005-112216-500-3447-1

**Placebo (Claude Opus 4.8). Stance: Structural.** The question read as a systems diagram: what flows where, in which direction, at what rate, and which wires carry nothing.

---

**1. Simplex pair, not duplex channel**
- **STATEMENT.** Input and output ride on physically separate unidirectional devices, so the link is two simplex channels, not one duplex channel.
- **ORIGIN.** Teletype console lineage (ASR-33, mid-1960s): keyboard-in and printer/CRT-out inherited intact.
- **STATUS.** Implicit. A hardware inheritance, never argued as an interaction choice.
- **COST.** No device both senses and renders, so every feedback loop crosses a device boundary and the human cannot be measured on the channel they act through.
- **FALSIFICATION.** A single bidirectional surface becoming the dominant channel. Touchscreens partly do this and weaken the claim.
- **CONFIDENCE.** Medium. Touch and voice are partial counterexamples; raised by showing the in/out split still governs serious work.

**2. The bandwidth asymmetry widens over time**
- **STATEMENT.** The uplink is capped near keystroke rate while the downlink scales with display technology, so the asymmetry diverges rather than holding steady.
- **ORIGIN.** Keyboard fixed as primary input in the 1960s; displays placed on the semiconductor growth curve thereafter.
- **STATUS.** Implicit. Nobody chose a diverging ratio; it fell out of upgrading one side.
- **COST.** The channels sit on different orders of magnitude (roughly 10^1 vs 10^6 bits/sec), so each hardware generation makes the human the narrower term by more.
- **FALSIFICATION.** Uplink bandwidth rising on the same curve as downlink (continuous sensing or neural input in common use).
- **CONFIDENCE.** Medium-high. The growth-rate divergence is inferred; the level asymmetry is not.

**3. The downlink is open loop above Level A**
- **STATEMENT.** No return path carries the receiver's comprehension, load or saturation back to the sender.
- **ORIGIN.** Terminal echo model, which closes the loop only on character transmission, not on reception.
- **STATUS.** Implicit. Acknowledgment was defined at the symbol layer and never added above it.
- **COST.** The machine transmits without measuring whether the human received, so there is no backpressure and saturation is invisible to the sender.
- **FALSIFICATION.** A deployed channel in which receiver state (gaze, load, confusion) routinely throttles machine output.
- **CONFIDENCE.** Medium-high. Eye-tracking and affect sensing exist but rarely gate transmission; this is where the claim is most exposed.

**4. Only two wires are lit**
- **STATEMENT.** Symbolic-in and visual-out carry traffic; interoceptive, proprioceptive and affective channels carry zero in both directions.
- **ORIGIN.** Inherited with the console; later additions (mouse, touch, audio) stayed within symbolic or audiovisual coding.
- **STATUS.** Implicit. The dark channels were never assigned a codebook, so no traffic could run on them.
- **COST.** Cross-channel capacity goes unused, and states the body already encodes (arousal, fatigue, orientation) cannot enter the link at all.
- **FALSIFICATION.** Widespread traffic on a non-symbolic, non-audiovisual channel in either direction.
- **CONFIDENCE.** High for the dark channels; medium that recent biometric telemetry does not already count as an affective uplink.

**5. Turn-synchronous, not continuously coupled**
- **STATEMENT.** Interaction is structured as discrete request-response turns rather than continuous mutual coupling.
- **ORIGIN.** Batch to time-sharing to the REPL/command loop; the turn boundary survived each transition.
- **STATUS.** Implicit. The turn was a scheduling artifact that became the interaction model.
- **COST.** A regime where neither side takes a turn and both stream and adapt is unavailable; human think-time and machine compute-time are forced into alternation.
- **FALSIFICATION.** A dominant interaction mode with no identifiable turn boundary (continuous co-adaptive control).
- **CONFIDENCE.** Medium-high. Turn-taking is observable; its necessity is not.

**6. The downlink sends sender-state, not receiver-uncertainty**
- **STATEMENT.** Output transmits the sender's current state rather than the receiver's residual uncertainty, so most of its bandwidth carries redundancy.
- **ORIGIN.** The refresh/repaint model of display, which re-renders present values regardless of change.
- **STATUS.** Implicit. A consequence of how frames are drawn, not a decision about information.
- **COST.** By self-information, an unchanged value carries zero bits, so the channel re-sends what the receiver already holds, and the actual change competes for attention on equal terms with the static field.
- **FALSIFICATION.** Dominant displays that transmit only change against a receiver model and suppress unchanged state.
- **CONFIDENCE.** Medium-high. The coding claim is proved; its universality across interfaces is inferred.

**7. Output is addressed to a serial sensor**
- **STATEMENT.** The downlink is aimed at a single high-resolution sensor (the fovea) that can point at one region at a time.
- **ORIGIN.** The visual display as primary output surface, assuming a gazing receiver.
- **STATUS.** Implicit. The display was built to the eye's resolution, not to its seriality.
- **COST.** Parallel on-screen streams are consumed serially, so the surface's parallelism cannot be realized, and ambient or peripheral delivery carries nothing.
- **FALSIFICATION.** Common output conveying primary information without foveal fixation (sustained peripheral or non-visual delivery).
- **CONFIDENCE.** Medium. Audio and haptics are partial counterexamples for secondary signals.

**8. Interrupt rights are asymmetric**
- **STATEMENT.** The machine may initiate transmission into the human's attention unsolicited; the human may only request and wait.
- **ORIGIN.** The event and notification layer added over time-sharing, which gave the system an unsolicited push path.
- **STATUS.** Implicit. Interrupts were an OS mechanism that became a right to seize attention.
- **COST.** The human cannot interrupt machine execution the way the machine interrupts human attention, so pacing and initiation sit on the silicon side.
- **FALSIFICATION.** A symmetric regime in which the human interrupts machine processing as readily as notifications interrupt the human.
- **CONFIDENCE.** Medium-high. The push path is observable; framing it as a reserved right is partly interpretive.

---

**A. THE MISS.** The open-loop downlink with no backpressure (assumption 3). The Historical lens will reconstruct the fork and the people and treat the result as a settled artifact. The Biological lens will place the pairing on the mutualism-to-parasitism axis, which names the relationship's character but not the absence of a specific wire. The Economic lens will trace incentives and who bore the cost. None of them measures the channel for a return path, because only the systems-diagram view asks where the acknowledgment is and why there is none. The bandwidth asymmetry (my 2) is already in the brief and all three may reach for it; the missing *return* path is a different claim and easy to walk past.

**B. UNCERTAINTY.** Two things. First, the bit-rate framing of the uplink (assumption 2) may be measuring the wrong quantity: one keystroke can trigger arbitrarily large machine computation through the shared codebook, so raw symbol rate understates what the uplink accomplishes, and the "narrow human" could be an artifact of counting symbols instead of consequences. Second, the modern sensor stack (camera, microphone, biometrics, background telemetry) may already falsify 3 and 4, which are my highest-stakes claims. Those are non-symbolic return paths. I am least sure whether to score telemetry as an open return channel or as data exhaust the human never authored as communication, and the two scorings give opposite verdicts on whether the architecture is frozen or already shifting.

**C. DISAGREEMENT WITH THIS BRIEF.** Two points.

First, the question asks for "the relationship" (singular) where the system is a bundle of independent channels with incompatible properties: different directions, rates, loss, and initiation rights. Aggregating them into one relationship is the move that hides the finding. The brief's own point 5 pulls the channels apart, then the question re-collapses them. The real object is a set of per-channel relationships, most of which are empty.

Second, the drift-versus-shift metaphor misassigns change. In influenza the pathogen mutates against a fixed immune system, so mapped onto this problem it says the interface changes while the human holds still. Yet the brief applies "drift" to both sides uniformly. Structurally the uplink was frozen and the downlink scaled by orders of magnitude. That is not one continuous drift; it is two different histories running on two different wires, and the single word buries exactly the asymmetry the inquiry is trying to find.
