# The Language Instrument

*Working note. 1 September 2026.*
*The only instrument in this project that needs no hardware.*

---

## The premise

Language is expensive. The brain is efficient. People say things for a reason, always.

**And the expense goes almost entirely to content.** That is what gets monitored, revised, and checked for accuracy and honesty. Function words are produced at high rate, largely automatically, and are close to impossible to control deliberately.

So the channel worth reading is the one nobody attends to. The monitored channel is the one to discount.

---

## Why this beats faces

The micro-expression instrument has a baseline problem that never got solved. Almost no calibrated within-person facial data exists, so every read is against a population average that describes nobody.

Language does not have that problem. **Thousands of words per person are available, cheaply, across time and context.** A person can be compared to themselves.

Person as own control, arriving from a third direction after BrainAdvantage and the granularity method.

And the comparison class is unflattering. Human deception detection sits near 54 percent across large meta-analyses. Professionals paid to do it, including police, judges and customs officers, perform about the same as undergraduates, sometimes worse, and are considerably more confident. That is the high-confidence low-accuracy quadrant occupied at industrial scale by people making decisions about other people's freedom.

---

## What is readable, with evidence behind it

**Pronoun distribution.** First-person singular frequency tracking depressive states is among the sturdier findings in the area. Pronoun use also shifts with relative status.

**Agent deletion.** Passive voice and nominalization systematically remove the actor. "There was a delay" rather than "I delayed." Rarely a deliberate choice, usually informative about where responsibility is being placed.

**Disfluency location.** Pauses, restarts and self-repairs mark the points where processing became expensive. The honesty check leaving a footprint.

**Within-person shifts** in sentence length variance, hedging density, cohesion and register.

Effect sizes in this literature are modest. Better than chance, not dramatic.

---

## The correction that makes it buildable

**Claude cannot be taught this.** Nothing persists between sessions. Whatever calibration happens in a conversation is gone when it ends, and memory files carry facts rather than a trained model.

**So the instrument lives in the files. Claude operates it.**

That reframe is the whole design.

---

## Design

**Corpus.** Randy's writing, already accumulating in this repository, across several registers.

**Labels.** Only Randy has these. "That one I was tired." "That one was a test." "That one my gut was tight." Retrospective is acceptable.

**Ground truth about interior state, paired with the text produced in it, does not exist anywhere at within-person scale**, because nobody generating the text is also willing to label it. Randy generates both halves.

**Features computed in code, not by impression.** This matters more than it sounds. A model reporting that it noticed a shift in pronoun distribution may be confabulating a method after the fact. Claude cannot verify its own mechanism and is a documented over-reader. So the numbers get computed where they can be checked, and any read becomes a hypothesis rather than a finding.

**Predict, then reveal.** The state is estimated from the text before the label is seen. Same architecture as the rest of the project.

**Scored.** Does the feature set beat chance on the labels. If not, that was learned cheaply.

---

## Why this is the strongest instrument here

No sensors. No wearable. No ceremony. No lab.

The text already exists. The labeling costs a sentence. The whole thing runs on files that are already in the repository and already syncing.

Compare with felt-shift detection, which needs instrumentation nobody has built, or the get-home MVP, which needs two subjects and a screening protocol.

**This one could start tonight and cost nothing.**

---

## Limits

**Reading language formation well is not the same as reading it correctly.** Beating a human is a low bar. Whether a feature set predicts Randy's states specifically is unproven and may simply fail.

**Confirmation is the failure mode.** A system looking for signal will find it. Predict-then-reveal exists precisely to make that visible.

**Modest effect sizes throughout.** Nothing in this literature is a strong effect, and a within-person design does not automatically fix that.

**And the interpretation problem from 1 September stands.** Function and intent are not cleanly separable. Any read of why a sentence took the shape it did is a hypothesis about a generating process nobody has direct access to, including the person who produced it.

---

## Status

Untested. Cheapest thing in the project to try, and the only one requiring nothing that does not already exist.
