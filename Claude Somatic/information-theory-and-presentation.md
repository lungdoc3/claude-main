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

Stated now, so it does not have to be discovered later.

**No enumerable alphabet.** Shannon's measure requires a known set of possible messages. The felt sense has no such set, and defining it is the entire problem rather than a preliminary to it.

**No shared codebook.** Shannon assumes sender and receiver share one. Carbon and silicon do not. What exists is a translation layer imposed on one party in 1965 and never negotiated.

That second one may be the finding underneath the whole brief.

**And information is not value.** A random string has maximum entropy and no worth. Surprise is not importance. Any currency built on entropy alone will rank noise above insight, which is why mutual information and not entropy is the candidate above.

---

## Reading, in order

1. **Weaver's introductory essay** in Shannon & Weaver, *The Mathematical Theory of Communication* (1949). Written for non-mathematicians. Source of the three levels.
2. **Shannon 1948**, first five pages. Readable by anyone. Where both quoted passages live.
3. Then, only if the appetite holds, the noisy channel coding theorem and rate-distortion.

---

## Status

Candidate vocabulary for Brief 01, alongside symbiosis taxonomy and bandwidth analysis. **It is the only one of the three with theorems.**

Nothing here is tested. Six design consequences, one candidate foundational assumption, and three stated limits.
