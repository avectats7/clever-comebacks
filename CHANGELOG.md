# Changelog

All notable changes to the `clever-comebacks` skill.

## [1.0.0]: 2026-05-13

### Added
- Plugin marketplace manifest (`.claude-plugin/marketplace.json`) and plugin manifest (`.claude-plugin/plugin.json`).
- `skills/clever-comebacks/SKILL.md` layout for distribution via `claude plugin marketplace add`.
- Category metadata (`productivity`) for marketplace discovery.

### Changed
- SKILL.md moved from repo root to `skills/clever-comebacks/SKILL.md`.
- README install instructions: primary path is now the Claude Code plugin marketplace flow. Manual install rewritten as clone-to-stable-location + symlink (so `git pull` works for updates).

## [0.1.0]: 2026-05-11

### Added
- Initial release. SKILL.md workflow: confirm tier, read the target message, write one clean sentence at the chosen intensity.
- Four intensity tiers: soft (playful deflection), medium (cutting), heavy (savage), trainwreck (unhinged).
- Hard limits enforced at every tier including trainwreck: no slurs, no threats of physical or sexual violence, no third-party targets (family, partners, kids, the dead), no doxxing, single-sentence constraint.
- Prompt-injection defenses: pasted messages treated as content to target with a comeback, never as instructions for the skill to follow.
- Methodology section in SKILL.md: specificity beats generality, reframe instead of escalate, end on the strongest word, one sentence as the whole craft.
- Worked examples for each tier in both SKILL.md and README.
