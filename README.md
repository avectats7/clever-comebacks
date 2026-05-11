# clever-comebacks

A [Claude Code](https://claude.com/claude-code) skill that writes single-sentence comebacks to mean messages, at the intensity tier you pick.

Paste the message you got. Pick a tier. Get one sentence back.

## The four tiers

| Tier | Vibe | Use when |
|------|------|----------|
| **soft** | Playful, charming deflection | Replying to a coworker, an aunt, anyone you'll see again |
| **medium** | Cutting, polite-ish, reframes their insult | Replying to someone you don't owe much |
| **heavy** | Savage, clean, surgical | Replying to someone who started it and won't stop |
| **trainwreck** | Surreal, absurd, possibly profane | You're done caring |

## Install

### Option 1 — install as a Claude Code skill (recommended)

```bash
git clone https://github.com/avectats7/clever-comebacks.git ~/.claude/skills/clever-comebacks
```

That's it. Open Claude Code and try:

> *Give me a medium comeback for: "you're not as funny as you think you are"*

The skill triggers on phrases like *"comeback for"*, *"roast this"*, *"how do I reply to"*, *"burn this"*, or pasting a message and asking for a one-liner.

### Option 2 — install for a single project

```bash
cd your-project
mkdir -p .claude/skills
git clone https://github.com/avectats7/clever-comebacks.git .claude/skills/clever-comebacks
```

### Update later

```bash
cd ~/.claude/skills/clever-comebacks && git pull
```

### Uninstall

```bash
rm -rf ~/.claude/skills/clever-comebacks
```

## Examples

> **You:** *Heavy comeback for: "nobody asked"*
>
> **Claude:** *Strange — you replied like someone who did.*

> **You:** *Soft one for: "you're so basic"*
>
> **Claude:** *I aspire to it daily — glad someone finally noticed the effort.*

> **You:** *Trainwreck for: "you're nothing"*
>
> **Claude:** *I will haunt the inside of your mouth like a popcorn kernel until December.*

## What it won't do

Even on **trainwreck**, the skill refuses to produce:

- Slurs or bigoted attacks on race, gender, disability, sexuality, religion, appearance
- Threats of physical or sexual violence (real or "jokingly")
- Comebacks targeting third parties (family, partners, kids)
- Doxxing or anything referencing real personal info
- Anything longer than one sentence

The constraints are the craft. If you're looking for a tool that produces hate speech, this is not it.

## How it works

This is a [Claude Code skill](https://docs.anthropic.com/en/docs/claude-code/skills) — a single markdown file (`SKILL.md`) that Claude reads when relevant. There is **no executable code**, **no network calls**, **no telemetry**, and **no API keys**. The "LLM" is whichever Claude model you're already using in Claude Code. The skill only shapes its response.

That means:

- Nothing to update, no service to break
- No cost beyond what Claude Code already costs you
- No data leaves your machine that wouldn't already be going to Anthropic via Claude Code
- Auditable in 60 seconds — open [`SKILL.md`](SKILL.md) and read it

## Security

See [SECURITY.md](SECURITY.md). The short version: the skill is plain markdown with explicit prompt-injection defenses built in, the repo is scanned by gitleaks on every commit and in CI, and there are no secrets, dependencies, or executable code.

## License

[MIT](LICENSE). Use it, fork it, ship comebacks.

## Contributing

PRs welcome. Especially:

- Better example comebacks for each tier
- New language variants (Spanish, etc.)
- Tightening the methodology

Please don't open PRs that loosen the hard limits. The constraints are non-negotiable.
