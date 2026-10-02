# Ledger

*Running state across all sessions. What is live, what is dead, what was decided.*
*Points at `_archive/index/` for detail and `_archive/raw/` for the words themselves.*

---

## Live

- Brief 01 drafted, not issued. Brief 00 (naming) transmits first and has not gone out either. Pass 2 pre-registered. Corrected 2 Oct 2026: the earlier entry here claimed Brief 01 was issued and awaiting four responses. It was not.
- `Claude Somatic/` MVP: primary hypothesis logged (a step, not a slope). Untested.
- First subjects named (Del, Randy's son). Screen not yet run.
- Rules of engagement established 31 Aug 2026. Untested against a real multi-agent session.
- ccb blackboard installed and dormant. Initialization not yet attempted. Blind debate with 4 participants unverified (API reads as a 2-model call).
- Information theory adopted as candidate vocabulary for Brief 01. Mutual information is the leading WAR denominator, still unchosen.
- Negotiated codebook proposed for the idle channels. Load-bearing open question: does the felt shift fire for an arbitrary symbol pairing, or only for symbolizations of a pre-existing interior state? Untested, and a negative answer invalidates the approach.
- **Step versus slope is now load-bearing.** An edge detector is blind to slow drift by construction rather than by tuning. If degradation in the get-home MVP is a slope, the instrument fails structurally. The hypothesis was pre-registered before this consequence was understood.
- Edge detectors also invent edges (Mach bands, the Cornsweet illusion). The confirmation failure mode in `language-instrument.md` and Claude's documented over-reading are the same artifact of the same architecture. Not tunable out. It is the price of the filter.

## Killed, and why

- **Silicon as interpreter of the felt sense.** Killed 30 Aug 2026. A machine deriving meaning from external proxies, then teaching it back to the only system with direct interior access. Later found to have a hard empirical basis: no autonomic fingerprints for discrete emotion across 202 studies.
- **Scaffold-and-fade as a frequency prescription.** Killed 31 Aug 2026. Rested on the guidance hypothesis, which failed meta-analysis in 2022 across 75 effect sizes. The probe-first ordering survived on different grounds.
- **Heartbeat counting as an outcome measure.** Killed 31 Aug 2026. 133 studies, null on every psychological construct, significant on heart rate, BMI, sex and age.
- **The Helen Keller framing.** Killed 31 Aug 2026 by Randy. Imports the wrong problem: Helen was acquiring a channel she lacked, the target population is disinhibiting one they have.
- **The assumption that the group is reachable only through one agent's chat window.** Killed 1 Sep 2026 by reading the harness. Four independent panes, plus a dormant blackboard with a broadcast primitive restricted to Claude or the cofounder.
- **Google Drive as the sync mechanism.** Killed 31 Aug 2026. Rejected on his history with it, and because the documents are 1 MB while the folder is 275 MB.

## Decided

- `~/Claude MAIN` is the single parent for AI workspaces. Del's world stays partitioned as `~/.ccb` and `ccb-*`.
- Sync is a private git repo, `github.com/lungdoc3/claude-main`. Media and archived source excluded.
- Claude runs the git. Randy does not.
- Synthesis of multi-agent output stays with Randy and Claude, never with a participant.
- Archive principle: do not compress, index.
- The carbon-silicon inquiry split from Claude Somatic into Claude Interface on 5 Sep 2026. It began as the Somatic premise and outgrew it. Somatic keeps the felt sense work; Interface takes the relationship, the briefs, information theory, the negotiated codebook and the language instrument.
- Surprisal allocates attention among true messages. It is never an objective function, since the cheapest route to surprise is to lie, and optimizing for it produces the attention economy.
- The machine proposes symbols and reads physiological verdicts. It never decides what anything means. This now has three independent supports: the correction of 30 Aug, the absence of autonomic fingerprints across 202 studies, and the data processing inequality.
- ccb is upstream open-source software (bfly123/claude_code_bridge v5.2.6), not Del's build. Corrected in the record 1 Sep 2026.
- **The contrast requirement and edge detection are one finding.** 29 Sep to 2 Oct 2026. A constant carries zero information and is undetectable in principle, so the felt sense is invisible because it is always on, not because it is subtle. Recognizing a state proves the alphabet already held two symbols. Every sensory system is a differentiator: the retina transmits gradients and largely discards absolute luminance. Supports: Barlow's efficient coding hypothesis (1961), lateral inhibition (Hartline, Nobel 1967), oriented edge detectors in V1 (Hubel and Wiesel, Nobel 1981), Marr and Hildreth's theory of edge detection (1980). Consequence: the teaching target is not the state but the edge, which makes the engineering job manufacturing a gradient. Randy arrived at it from writing image-editing convolution kernels. "Send the surprise, not the state" is the same result, read off biology 65 years earlier.
- `Claude Interface/` is its own ccb project anchor. A `.ccb/` directory there gives the House of Del project id `2b250d5d`, separate from the home-directory sessions at `6e7d70c8`: separate session files, separate spool, separate memory. The anchor is gitignored, because session state carries machine-specific temp paths and would conflict across the two Macs.
