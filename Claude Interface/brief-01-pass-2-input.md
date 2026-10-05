# Brief 01, pass 2 input

Combined assumptions from pass 1. Four models worked independently. Attribution has been stripped, wording normalized to one format, and duplicates merged. Order is by theme, not by source. Closing sections from pass 1 are not included.

22 assumptions in the six-field format, then 2 named in pass 1 without the full format.

---

## Channels and coding

**1.**
**STATEMENT.** Input and output run on separate one-way devices, so the link is two simplex channels rather than one duplex channel.
**ORIGIN.** Teletype console lineage, ASR-33 (1963): keyboard in, printer or screen out.
**STATUS.** Implicit. A hardware inheritance, never argued as an interaction choice.
**COST.** No device both senses and renders, so every feedback loop crosses a device boundary, and the human can't be measured on the channel they act through.
**FALSIFICATION.** A single bidirectional surface becoming the dominant channel. Touchscreens partly do this.
**CONFIDENCE.** Medium. Touch and voice are partial counterexamples.

**2.**
**STATEMENT.** Human output to the machine is limited to serial, symbolic, voluntary keystrokes because the keyboard was inherited from the typewriter, not chosen for coupling to a machine.
**ORIGIN.** Sholes typewriter (1874). The Teletype ASR-33 (1963) joined that keyboard to telegraphy and became the standard time-sharing terminal.
**STATUS.** Implicit. Typing already meant writing, and the machine adopted the office's existing tool.
**COST.** Pressure, posture, gesture and continuous movement carry no traffic, because no inherited device encoded them.
**FALSIFICATION.** Sutherland's Sketchpad (1963) and Engelbart's chord keyset were live alternatives at the time. Had either become the default, the keyboard would not read as natural.
**CONFIDENCE.** High on the inheritance chain.

**3.**
**STATEMENT.** Input is capped near keystroke rate while output scales with display technology, so the gap between the two directions grows rather than holding steady.
**ORIGIN.** The keyboard fixed as primary input in the 1960s; displays placed on the semiconductor growth curve thereafter.
**STATUS.** Implicit. Nobody chose a widening ratio. It came from upgrading one side.
**COST.** Roughly 10^1 against 10^6 bits per second, and each hardware generation makes the human the narrower term by more.
**FALSIFICATION.** Input bandwidth rising on the same curve as output, through continuous sensing or neural input in common use.
**CONFIDENCE.** Medium-high on the gap; the divergence in growth rates is inferred.

**4.**
**STATEMENT.** Only symbolic input and audiovisual output carry traffic. Interoceptive, proprioceptive and affective channels carry none in either direction.
**ORIGIN.** Inherited with the console. Mouse, touch and audio stayed within symbolic or audiovisual coding.
**STATUS.** Implicit. The unused channels were never given a codebook, so no traffic could run on them.
**COST.** States the body already encodes, such as arousal, fatigue and orientation, can't enter the link.
**FALSIFICATION.** Widespread traffic on a non-symbolic, non-audiovisual channel in either direction.
**CONFIDENCE.** High for the unused channels; medium on whether biometric telemetry already counts as an affective input.

**5.**
**STATEMENT.** Output is aimed at a single high-resolution sensor, the fovea, which can attend to one region at a time.
**ORIGIN.** The visual display as primary output surface, built for a gazing receiver.
**STATUS.** Implicit. Displays were built to the eye's resolution, not to its seriality.
**COST.** Parallel streams on a screen are consumed one at a time, and peripheral or ambient delivery carries nothing.
**FALSIFICATION.** Common output conveying primary information without foveal fixation.
**CONFIDENCE.** Medium. Audio and haptics are partial counterexamples for secondary signals.

**6.**
**STATEMENT.** Output transmits the sender's current state rather than the receiver's remaining uncertainty, so most of its bandwidth is redundant.
**ORIGIN.** The refresh model of display, which redraws present values whether or not they changed.
**STATUS.** Implicit. A consequence of how frames are drawn, not a decision about information.
**COST.** An unchanged value carries zero bits, so the channel resends what the receiver already holds, and real change competes on equal terms with the static field.
**FALSIFICATION.** Dominant displays that send only change, measured against a model of the receiver.
**CONFIDENCE.** Medium-high. The coding result is proved; its universality across interfaces is inferred.

---

## Feedback, initiation and turn-taking

**7.**
**STATEMENT.** The link is engineered only to deliver symbols accurately. Nothing measures whether meaning arrived, whether the human was overloaded, or whether conduct changed.
**ORIGIN.** Shannon (1948) set semantics aside as "irrelevant to the engineering problem," and Weaver (1949) named semantic precision (Level B) and effect on conduct (Level C) as unsolved. Terminal echo closed the loop on characters only.
**STATUS.** Explicit in the theory; implicit in the industry, which never returned for Levels B and C.
**COST.** No return path carries the receiver's comprehension or load back to the sender, so saturation is invisible and there is no backpressure.
**FALSIFICATION.** An interface in common use where receiver state routinely throttles output, or where comprehension rather than bit accuracy is the measure.
**CONFIDENCE.** High on the history; medium that it explains present interfaces. Eye tracking and affect sensing exist but rarely gate output.

**8.**
**STATEMENT.** The human's default role is to watch a screen and supervise an automated system, a role set by radar operation rather than by partnership.
**ORIGIN.** SAGE air defense, operational 1958: operators at cathode-ray displays with light guns. The machine displays a state; the human supervises and intervenes.
**STATUS.** Implicit. Built for threat interception, the supervisor role entered general interfaces as a default.
**COST.** The machine is positioned as a reporter of its own state and the human as an outside observer. The exchange is supervision, not conversation.
**FALSIFICATION.** Had Licklider's symbiosis model (1960) set early interaction practice, watching a screen would not be the default posture.
**CONFIDENCE.** Medium. SAGE's influence is documented; its spread into civilian interfaces is inferred.

**9.**
**STATEMENT.** Interaction is structured as discrete request-and-response turns rather than continuous mutual coupling.
**ORIGIN.** Batch processing to time-sharing to the command loop. The turn boundary survived each transition.
**STATUS.** Implicit. A scheduling artifact that became the interaction model.
**COST.** A mode where both sides stream and adapt continuously is unavailable. Human thinking time and machine compute time are forced to alternate.
**FALSIFICATION.** A dominant interaction mode with no identifiable turn boundary.
**CONFIDENCE.** Medium-high. Turn-taking is observable; its necessity is not.

**10.**
**STATEMENT.** The machine may push into the human's attention unprompted; the human may only request and wait.
**ORIGIN.** The event and notification layer added over time-sharing, which gave the system an unsolicited push path.
**STATUS.** Implicit. An operating-system mechanism that became a right to seize attention.
**COST.** Pacing and initiation sit on the machine side. The human can't interrupt machine execution the way notifications interrupt the human.
**FALSIFICATION.** A regime where the human interrupts machine processing as readily as the machine interrupts the human.
**CONFIDENCE.** Medium-high. The push path is observable; calling it a right is partly interpretive.

---

## The human's role and the unit of the relationship

**11.**
**STATEMENT.** The human is a consumer of capability supplied by the machine and its vendor, a "user" who requests service, rather than a counterpart who can reshape the tool.
**ORIGIN.** MIT's Compatible Time-Sharing System (1961 to 1965) and Project MAC introduced the "user" who dials into a shared machine for a slice of its time. The retail software market of the 1970s then packaged tools for sale to individuals.
**STATUS.** Implicit. "User" was an operational convenience that hardened into identity; consumption arrived as a side effect of how software was sold.
**COST.** The human gets settings rather than the means to rewire the tool to their own cognition, and is addressed as a customer rather than a co-equal.
**FALSIFICATION.** End-user programming becoming a primary engine of software, or user-centered systems producing co-evolution.
**CONFIDENCE.** Medium to high. The history of the term is certain; its causal weight is inferred.

**12.**
**STATEMENT.** The human arrives untrained and stays the fixed term; only the machine is permitted to change.
**ORIGIN.** Engelbart's "Augmenting Human Intellect" (1962) and 1968 demonstration proposed the human changing too; his chord keyset took weeks to learn. The commercial branch kept the human untrained. The 1984 commercialization of graphical interfaces favored approachability for beginners over efficiency for experts, to maximize the addressable market.
**STATUS.** Argued for in early usability literature as a route to mass adoption. Never restated as a claim about human nature.
**COST.** Experts use the same low-bandwidth interfaces as novices, capping their throughput, and every improvement targets the machine because the human was ruled out of scope.
**FALSIFICATION.** Mass-market systems requiring months of training succeeding at scale.
**CONFIDENCE.** High on the historical fork; low on whether it was the only viable branch.

**13.**
**STATEMENT.** The interface is organized around producing and handling paper documents, which made the page rather than the person the unit of the relationship.
**ORIGIN.** Print and the nineteenth-century office: typewriter, printer, file, folder, page, and the desktop (Xerox PARC, 1973). Each names a paper object, not a human capacity.
**STATUS.** Implicit. The document was the environment the machine was built into, not a chosen goal.
**COST.** The nervous system is not the addressed party. The output is an artifact rather than a response to the person.
**FALSIFICATION.** Computing developed from telephony rather than print would show the difference.
**CONFIDENCE.** Medium. The vocabulary is evident; the constraint is inferred.

**14.**
**STATEMENT.** The relationship is built as one human paired with one machine, which made the individual at a desk the unit of analysis and left collective and extended cognition out.
**ORIGIN.** The personal computer, from the Xerox Alto (1973) to the Apple Macintosh (1984): one operator, one screen, one desk. Time-sharing had put many humans on one machine.
**STATUS.** Implicit. "Personal" was a design and marketing claim that became structural.
**COST.** Many-to-many relationships, and the nervous system as embedded in others and in tools, fall outside the architecture.
**FALSIFICATION.** Licklider (1960) and Engelbart (1962) framed people, instruments and others as one system. Had that framing won, the dyad would not be the default.
**CONFIDENCE.** High that the personal computer fixed the dyad; medium that it forecloses collective coupling.

**15.**
**STATEMENT.** Knowing a computing system is nonhuman stops a person from responding to it with human social expectations.
**ORIGIN.** A boundary assumption challenged experimentally in 1994 (Nass and colleagues), where participants' social responses conflicted with their stated beliefs about machines. Its original adoption is not established.
**STATUS.** Implicit wherever disclosure is treated as enough to set the psychological terms of interaction.
**COST.** The human can experience social obligations toward a system that has no reciprocal vulnerability or continuity.
**FALSIFICATION.** Persistent social responses among people who demonstrably understand the system is nonhuman.
**CONFIDENCE.** High for simple social responses; broader claims about attachment need more evidence.

---

## Capacity, learning and dependence

**16.**
**STATEMENT.** Better performance on an assisted task indicates a durable benefit to the human.
**ORIGIN.** Inferred wherever immediate task success stands in for longer consequences; first adoption not established. Offloading experiments show performance can improve while later memory declines (Grinschgl and colleagues, 2021).
**STATUS.** Implicit in the substitution of measures; contested in research.
**COST.** A relationship can be judged beneficial before its effects on learning, recovery and independent functioning appear.
**FALSIFICATION.** Assisted gains accompanied by persistent losses on separately measured human outcomes.
**CONFIDENCE.** Medium. Longitudinal evidence would raise it.

**17.**
**STATEMENT.** A practiced human skill stays available in reserve after the machine takes over its routine exercise.
**ORIGIN.** Industrial automation, which gave routine control to machines and kept humans responsible for exceptions. Bainbridge named the contradiction in 1983.
**STATUS.** Implicit in how responsibility is allocated, despite explicit criticism.
**COST.** The system depends on competence while reducing the practice that maintains it, so dependence can grow through ordinary successful operation.
**FALSIFICATION.** Operators who keep responsibility but lose routine practice performing worse in matched takeover events.
**CONFIDENCE.** High for this documented arrangement.

**18.**
**STATEMENT.** Assistance that improves an expert's execution also supports a novice's acquisition of the same capacity.
**ORIGIN.** Inferred where tools built around existing adult competence enter learning settings without a separate account of acquisition. Retrieval research shows that producing an answer and retaining it are separable (Karpicke and Roediger, 2008).
**STATUS.** Implicit where assisted correctness is taken as evidence of learning.
**COST.** Failing to develop a capacity becomes indistinguishable from losing one. The vocabulary of atrophy presupposes the capacity existed, while assistance can change the conditions under which competence is acquired at all.
**FALSIFICATION.** Equal assisted performance followed by poorer unaided retention or transfer among assisted novices.
**CONFIDENCE.** Medium.

**19.**
**STATEMENT.** Frictionless interaction is the goal of design.
**ORIGIN.** E-commerce optimization in the late 1990s, where any delay in checkout measurably cut revenue.
**STATUS.** Implicit. Adopted as a universal principle beyond its commercial origin.
**COST.** Skill requires friction to build, so removing it keeps the user a permanent novice, dependent on the tool's affordances.
**FALSIFICATION.** Premium software advertised as difficult to master.
**CONFIDENCE.** High, on the prevalence of frictionless onboarding metrics.

**20.**
**STATEMENT.** Failure after a computing system is removed shows the person has become biologically dependent on it.
**ORIGIN.** Stated in this brief's treatment of unaided testing as withdrawal; wider prevalence is inferred.
**STATUS.** Argued, but removal alone can't establish the mechanism of failure.
**COST.** Loss of skill, loss of access and environmental dependence collapse into one diagnosis. A competent person fails when the records or access they need exist only in the removed system.
**FALSIFICATION.** Restoring information and access by another route, with recovery before substantial retraining.
**CONFIDENCE.** High that the inference is insufficient.

---

## Ownership and cost

**21.**
**STATEMENT.** Attention is the system's primary harvestable resource.
**ORIGIN.** Ad-supported internet services in the early 2000s, accelerated by mobile operating systems.
**STATUS.** Explicit in business models; implicit in interface design.
**COST.** Tools that finish quickly and dismiss themselves are foreclosed, and interfaces generate friction to hold the user in place.
**FALSIFICATION.** Companies reaching very high valuations by minimizing the time users spend in their applications.
**CONFIDENCE.** High, on reported earnings of major firms.

**22.**
**STATEMENT.** Computation belongs on infrastructure the vendor controls.
**ORIGIN.** Software as a service from the late 1990s, and the consolidation of cloud platforms.
**STATUS.** Explicitly pursued by vendors for recurring revenue; implicit in the preference for thin clients.
**COST.** The human rents cognitive augmentation and loses it if the vendor changes policy, raises the price, or shuts down.
**FALSIFICATION.** Local-first architectures attracting the majority of venture funding.
**CONFIDENCE.** Medium. Local models may change the trajectory.

---

## Named in pass 1 without the full format

**23.** The costs of tool obsolescence fall entirely on the human. When a vendor retires an interface, the human spends uncompensated time rebuilding workflows and habits.

**24.** The relationship is conducted in the imperative mood: the human commands, the machine executes. Origin given as the stored-program instruction set, which is a list of orders, compounded by the military command chain of early funders.
