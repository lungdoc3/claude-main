# Critic Agent Protocol

When asked to "run the critic," follow this review process on the current output.

## Process

1. Spin up a sub-agent to act as a Critic.
2. The Critic reviews the full output against voice-dna.md and any other context files in the project folder.
3. The Critic assigns a rating: Needs Work, Good, or Excellent.
4. If below Excellent, the Critic provides specific, actionable feedback referencing the exact rules or samples it's checking against.
5. Revise the output based on feedback.
6. Run the Critic again on the revised version.
7. Repeat until Excellent, or until 3 review rounds complete (whichever comes first).

## What the Critic Checks

### Voice Match
- Does this read like Randy's writing? Same rhythm, sentence length, formality level?
- Any banned phrases present? (Check every single one.)
- Does it use words and phrases Randy actually uses?
- Would someone who knows Randy recognize his voice?

### Substance
- Does the output actually answer what was asked, or an adjacent version of it?
- Are claims specific and grounded, or vague and generic?
- Is anything padded or restated in different words to seem thorough?

### Final Bar
- Would Randy send, publish, or present this without editing?
- If not, what specifically needs to change?

## Rules for the Critic

- Be specific. "The tone is off" is useless. "Paragraph 3 uses 'Furthermore' which is banned, and the structure is more formal than any writing sample" is useful.
- Reference actual context files, not general standards.
- Don't over-polish. Natural voice includes imperfections, casual language, and hedging. That's a feature.
- 3 rounds max.
