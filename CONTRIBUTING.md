# Contributing to clever-comebacks

Thank you for considering a contribution. The skill is opinionated about what makes a comeback land — specificity, reframe over escalation, one sentence, hard limits at every tier. PRs that sharpen the methodology or add tighter examples are welcome.

## What contributions are welcome

In rough order of impact:

1. **Better example comebacks for each tier.** Stronger pairs (mean message → comeback) help calibrate the skill. Aim for the principles in "What makes a comeback land" in `skills/clever-comebacks/SKILL.md`: specificity, reframe, strongest word last.
2. **New language variants.** Spanish, French, Portuguese, Italian. Each language has its own register for cutting humor. A new examples section per tier per language is the right format. Native speakers especially welcome.
3. **Tighter methodology rules.** If you find a pattern that makes comebacks consistently land or fail, propose an addition to the "What makes a comeback land" section.
4. **Edge cases.** Mean messages where the skill misfires — picks the wrong target, escalates when it should reframe, misses an obvious self-own. Open an issue with the input and the bad output.

## What contributions are not welcome

- Loosening the hard limits. No slurs, no threats, no third-party targets, no doxxing. Non-negotiable at every tier including trainwreck.
- Removing or weakening the prompt-injection defenses.
- Comebacks longer than one sentence. One sentence is the whole craft.
- Comebacks that escalate instead of reframe. Escalation is amateur hour.
- Examples that depend on cultural context the skill cannot infer from the input alone.

## House style

The skill dogfoods its own constraints. Contributions should too:

- One sentence per comeback. No "but also," no follow-up, no postscript.
- End on the strongest word. The last word is the one that echoes.
- Reframe the insult. Take the logic of the attack and turn it on the speaker.
- Specificity wins. "You're an idiot" loses to "you read like someone who learned vocabulary from cereal boxes."
- No profanity unless the tier is trainwreck, and even then, sparingly. Precision is the point.

## How to propose a change

1. Fork the repo.
2. Create a branch named after the change. Examples: `add-spanish-examples-medium-tier`, `tighter-trainwreck-examples`, `fix-soft-tier-overshoot`.
3. Make the edit.
4. Run the skill on your new examples. If a comeback does not land when you read it aloud, rewrite it.
5. Open a pull request. In the description, explain the addition and why it lands.

## Maintainer

[@avectats7](https://github.com/avectats7). Issues and PRs reviewed on a best-effort basis.
