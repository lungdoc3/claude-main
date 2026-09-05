# Information Theory and the Presentation Problem

*Working note for the carbon-silicon inquiry. 1 September 2026.*
*The first concrete design consequence to fall out of the foundational reframe.*

---

## Why this thread opened

The original observation, from the chain of thought in `_START_HERE.md`:

> Every data output looks the same. A window filled with lots and lots of information streams, more than the carbon system can use effectively. The move runs backwards from the usual direction: study how the carbon system manages inputs, then gear the output to meet those input requirements.

Correct, and it had no theory under it. Information theory supplies one, along with several results that are proved rather than argued.

---

## What Shannon actually offered, and what he refused

The opening of *A Mathematical Theory of Communication* (1948):

> "The fundamental problem of communication is that of reproducing at one point either exactly or approximately a message selected at another point."

And then, immediately:

> "Frequently the messages have meaning; that is they refer to or are correlated according to some system with certain physical or conceptual entities. **These semantic aspects of communication are irrelevant to the engineering problem.**"

Shannon threw out meaning and built the most successful theory of communication ever written on what remained.

**That is the same constraint this project arrived at independently** when it killed silicon-as-interpreter. Shannon got there in 1948 and turned the restriction into a foundation rather than treating it as a limitation.

### Weaver's three levels

Warren Weaver's 1949 introduction, written for non-mathematicians, splits the problem:

- **Level A, technical.** How accurately can symbols be transmitted?
- **Level B, semantic.** How precisely do transmitted symbols convey the intended meaning?
- **Level C, effectiveness.** How effectively does received meaning change conduct?

Shannon solved A completely. B and C have been open for 77 years.

**This project lives entirely in B and C.** Worth knowing, because it locates the beautiful mathematics next door to the problem rather than inside it.

### The theorem that proves the correction

**The data processing inequality.** If X goes to Y goes to Z, then Z can never contain more information about X than Y does. Post-processing cannot create information.

A machine reading HRV and facial action units is downstream of the felt sense. It can never hold more information about that signal than the proxies carry, and never more than the person generating it.

"The silicon supplies no meaning" is a consequence of a proved result, not only a judgment call.

### Currency: the distinction that matters

**Entropy measures the capacity of a channel. Mutual information, I(X;Y), measures how much knowing one thing tells you about another.**

Mutual information is a measure of coupling between two systems and requires no semantics. Entropy is the currency of a channel. Mutual information is the currency of a *relationship*.

For the WAR question, which never had a denominator, this is the strongest candidate so far.

---

## Six design consequences

Each of these runs opposite to standard practice.

### 1. Send the surprise, not the state

Information is surprise. A value that has not changed carries zero information. Every dashboard re-renders everything on every refresh, spending the scarcest resource in the system on redundancy.

A display showing all current values transmits almost nothing while costing continuous attention.

The delta engine already had this instinct. **The delta is the information. The absolute readings are not.**

#### Surprise is computable per message

Self-information: **I(x) = -log2 p(x)**. The information carried by a specific message is the negative log of its probability. Unlike entropy, which is an average over a distribution, this is a number for a single event. Every possible reading can therefore be ranked by how much it would actually tell this receiver, and attention allocated against that ranking.

#### The log shape, and what it forecloses

Halving a probability adds exactly one bit, whether the move is from 0.5 to 0.25 or from 0.001 to 0.0005.

So the informational distance between *expected* and *unusual* is enormous, and the distance between *unusual* and *very unusual* is close to nothing.

**Almost all available information sits in the first departure from expectation.** Every gradation after that is rounding error dressed as urgency.

#### Worked example: alarm fatigue is a coding failure

A clinical monitor encodes many tiers of urgency into a channel where the informational difference between the eighth tier and the twelfth is under a bit. Meanwhile the commonly cited false-alarm range in clinical monitoring runs from roughly 70 percent to well above 90, varying by unit and study.

Run the arithmetic. If an alarm fires and nothing is wrong nine times in ten, p(alarm) is high, so I(alarm) is near zero. The alarm carries almost no information at the moment it sounds.

**A clinician who stops responding is computing correctly.** That is accurate Bayesian updating performed on a channel that misrepresented its own probabilities.

This reframes the standard account. Alarm fatigue is usually described as a human failure calling for training, vigilance or discipline. It is a coding failure, and the receiver is the only component of the system behaving properly.

It also rules out most of what gets tried. Volume, color, urgency styling, an additional escalation tier: each attempts to add information to a message that has none. **The only repair is changing p**, which means changing the conditions under which the thing fires.

#### And this is why the felt sense works without an alphabet

The felt sense is a surprisal detector. It does not identify a state, it registers a departure from an expected one.

That is precisely why it operates where Shannon's framework struggles. **An enumerable message set is required to measure information about *which* message arrived. It is not required to notice that something is not as it was.**

Which makes "something is here," with meaning left to the carbon system, the correct division rather than a compromise. Departure is the part a machine can compute. Identity is not.

### 2. The channel-payload mismatch

The output of a degradation monitor is roughly one bit. Something changed, or it did not.

That one bit is currently delivered through a megabit visual channel requiring foveal attention, which blocks everything else while it is being read.

A screen for one bit is couriering a postcard by freight train.

The haptic channel carries a few bits per second, needs no gaze, and is almost exactly matched to the payload. It is idle. So are the proprioceptive and interoceptive channels, in both directions.

**Total capacity is the sum across channels. A saturated channel is not fixed by compressing harder. It is fixed by opening another one.**

### 3. Match the code to the source

Shannon's source coding theorem: optimal codes assign short codewords to frequent messages and long ones to rare messages.

Interfaces do the reverse, or more often nothing at all, granting equal weight to the thing that is always true and the thing that has never happened before.

Huffman coding, applied to attention. The usually-true should cost almost nothing to perceive. The rare should be unmissable.

### 4. The receiver's prior is part of the channel

Information is not a property of the signal. It is a property of the signal relative to what the receiver already expects.

The same display carries different information to different people, and to the same person on different days.

**This makes personalization a bandwidth calculation rather than a preference setting.** A system that models your prior can send less and convey more.

### 5. Redundancy belongs where the stakes are

Shannon's noisy channel coding theorem: reliable transmission over a noisy channel is possible given the right redundancy.

Human attention is a noisy channel. So critical messages should be redundantly encoded across modalities, and trivial ones should not be. Current practice applies redundancy uniformly or at random.

### 6. Rate-distortion dissolves the summary problem

Rate-distortion theory: if compression is unavoidable, the optimal compression depends entirely on the chosen distortion measure.

Standard summarization optimizes for preserving topics, which is exactly why it destroys what this project values.

**Name nuance as the distortion measure and a different compression falls out.** The "index, do not compress" rule in `RULES-OF-ENGAGEMENT.md` was the right instinct with the wrong reason available.

---

## The line underneath all six

**Every interface built since 1968 transmits the sender's state rather than the receiver's uncertainty.**

Here is everything we have, rather than here is what you did not already know.

That is a candidate for the foundational assumption Brief 01 is hunting, and it is testable in a way most candidates are not.

---

## Where information theory will not serve

Three fences. Stated now, with the location of each one marked, so nobody walks into them in month four.

### 1. No enumerable alphabet

Entropy is a sum: **H = -Σ p(x) log p(x)**. The sum runs over the set of possible messages. No set, no sum, no number.

Shannon can price a drawn card because there are 52 and the odds are known. Say "I drew something from a collection of unknown size and composition" and there is no calculation to perform. Not a hard one. None.

The felt sense has no such set. Gendlin insisted each one is unique to its situation and that a borrowed category word papers over it rather than matching it. The alphabet is not merely undiscovered. **Enumerating it would destroy the thing**, since a felt sense that fits neatly into a predefined category was a category all along.

**Where the fence actually sits:** the information content of a given felt sense is not computable. That a departure occurred is. Detection survives, identification does not.

Which is the same line this project drew for unrelated reasons. Two independent constraints landing in one place is worth noticing.

### 2. No shared codebook

Shannon assumes both ends agree in advance what the symbols mean. Morse works because both ends hold the same table. Without a shared table, transmission is noise arriving on schedule.

Carbon and silicon do share one at the symbol level: text, ASCII, English, pixels. That is why **Level A works fine**. Characters arrive intact.

That codebook was built for the machine's convenience and handed to the human as a condition of entry. The human learned it. The machine never learned the human's. Every exchange pays an encode tax and a decode tax, and the losses compound in both directions.

**The opportunity inside this one:** the idle channels have no codebook yet. Haptic, proprioceptive, interoceptive. Nothing has to inherit the 1965 table for a channel that has never had one, which means those could be negotiated rather than imposed. See `negotiated-codebook.md`.

### 3. Surprise is not value

Maximum entropy means maximum unpredictability, which means random. **A random string is maximally informative by Shannon's measure and worth nothing.**

A smoke detector firing at random times is highly surprising and useless. One firing only during fires is far less surprising in aggregate and infinitely more valuable. A currency built on entropy would rank the noise generator above the instrument.

**The failure mode already exists at scale.** Optimize an interface for surprise with no truth constraint and the result is the attention economy. Engagement maximization is surprise maximization without accuracy, and the output is well documented.

So "send the surprise" is a rule for allocating attention **among messages already known to be true**. As a standalone objective it is catastrophic, because the cheapest route to surprise is to lie.

### The synthesis

The three fences collapse into one instruction:

- **Mutual information** for value. It measures how much a signal tells you about the thing you care about, and a random signal has zero of it with anything.
- **Self-information** for allocation. Given true messages, spend attention in proportion to surprisal.
- **Entropy alone** for neither.

---

## Reading, in order

1. **Weaver's introductory essay** in Shannon & Weaver, *The Mathematical Theory of Communication* (1949). Written for non-mathematicians. Source of the three levels.
2. **Shannon 1948**, first five pages. Readable by anyone. Where both quoted passages live.
3. Then, only if the appetite holds, the noisy channel coding theorem and rate-distortion.

---

## Status

Candidate vocabulary for Brief 01, alongside symbiosis taxonomy and bandwidth analysis. **It is the only one of the three with theorems.**

Nothing here is tested. Six design consequences, one candidate foundational assumption, and three stated limits.
