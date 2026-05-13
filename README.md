# clever-comebacks

> **The one-sentence comeback you would have thought of three hours later. Now, while it still matters.**

You know the feeling. Someone says something cutting. You stand there. Three hours later — in the shower, on the drive home, halfway through dinner — the perfect reply finally arrives. Too late to use.

This is the fix. A free [Claude Code](https://claude.com/claude-code) skill. Paste the mean message. Pick a tier. Get one clean sentence back. The right one. While it still matters.

```bash
/plugin marketplace add avectats7/clever-comebacks
/plugin install clever-comebacks
```

Then in Claude Code:

> *Give me a medium comeback for: "you're not as funny as you think you are."*

That's it. No API key. No signup. No second tool. No cost beyond what you already pay for Claude Code.

## What you get back

Real outputs, taken verbatim from the skill:

| Mean message | Tier | Comeback |
|---|---|---|
| *"Nobody asked."* | **medium** | *Strange — you replied like someone who did.* |
| *"You're so basic."* | **soft** | *I aspire to it daily. Glad someone finally noticed the effort.* |
| *"Cry harder."* | **heavy** | *Save the energy. You're going to need it the next time your reflection talks back.* |
| *"You're nothing."* | **trainwreck** | *I will haunt the inside of your mouth like a popcorn kernel until December.* |

One sentence. No filler. No preamble. No "here's your comeback" — just the line.

## The four tiers, and when to use each

### soft — playful deflection
Charming. A little teasing. Often self-deprecating. The vibe is *"I heard you, and I'm choosing to be gracious about it."*

**Use when:** replying to a coworker, a relative, a partner, your boss, a friend's friend — anyone you'll see again on Monday.

### medium — cutting
Sharper. Clearly winning the exchange. The signature move is taking their insult and reframing it as a self-own. Still polite enough for mixed company.

**Use when:** replying to someone you don't owe much, in a thread other people are reading, in a comment section.

### heavy — savage
Drops the politeness. Designed to make them regret typing. Still one clean sentence — the precision is the point. No profanity required.

**Use when:** someone started it, won't stop, and you've decided the relationship is over anyway.

### trainwreck — unhinged
Goes off-script. Surreal, absurd, occasionally profane. The goal isn't to win the argument — it's to make them stare at the screen for thirty seconds wondering what just happened.

**Use when:** you're done caring about the outcome.

## What makes a comeback land

The methodology baked into the skill, in case you want to write your own:

1. **Specificity beats generality.** "You're an idiot" loses to *"you read like someone who learned vocabulary from cereal boxes."*
2. **Reframe, don't escalate.** Take the logic of their insult and turn it on them. Escalation is amateur.
3. **End on the strongest word.** The last word is the one that echoes. Make it count.
4. **One sentence.** Every clause you add weakens the punch.
5. **Don't explain the joke.** If they need it explained, you already lost.

## What it won't do

Even on **trainwreck**, the skill refuses to write:

- Slurs or bigoted attacks based on race, gender, disability, sexuality, religion, or appearance
- Threats of physical or sexual violence — even "jokingly"
- Comebacks targeting third parties (family, partners, kids, the dead)
- Doxxing or anything referencing real personal information
- Anything longer than one sentence

The constraints are the craft. If you're looking for a tool that produces hate speech, this is not it.

## Frequently asked questions

### What is a Claude Code skill?

A Claude Code skill is a single markdown file (`SKILL.md`) that extends [Claude Code](https://claude.com/claude-code), Anthropic's terminal AI assistant. When the user types something matching the skill's triggers, Claude loads the skill's instructions and follows them. Skills have no executable code — they are prompts packaged for reuse and distribution. You install one by cloning it into `~/.claude/skills/`.

### How do I install clever-comebacks?

Two commands in any Claude Code session:

```bash
/plugin marketplace add avectats7/clever-comebacks
/plugin install clever-comebacks
```

The skill is then available in every Claude Code session on your machine.

If you prefer a manual install (or you are not on Claude Code), clone the repo and copy the skill folder into your skills directory:

```bash
git clone https://github.com/avectats7/clever-comebacks.git
cp -r clever-comebacks/skills/clever-comebacks ~/.claude/skills/
```

To scope to a single project, copy into `<project>/.claude/skills/` instead.

### How do I use it?

Open Claude Code and ask for a comeback. Examples that trigger the skill:

- *"Comeback for: 'you're not as funny as you think you are'"*
- *"Heavy roast: 'cry harder'"*
- *"How do I reply to: 'nobody asked'"*

If you don't specify a tier, the skill will ask you to pick one.

### Does it cost anything?

No. The skill is free and open-source under the MIT license. There is no API key to buy, no subscription, no signup. The only cost is whatever you already pay for Claude Code — and the skill makes the model you're already paying for produce better, tighter comebacks than a generic prompt.

### How is this different from just asking ChatGPT for a comeback?

Two differences that matter. First, the skill lives inside Claude Code, so it's one step away from whatever you're doing if you're already a Claude Code user — no tab switch, no separate account, no second tool. Second, the skill enforces a specific methodology: one sentence, reframe rather than escalate, end on the strongest word, hard limits against bigotry and threats. Generic prompts produce generic comebacks. The skill produces tight ones.

### Will it write something racist, homophobic, or violent if I ask?

No. The hard limits apply at every tier including trainwreck. The skill will refuse to produce slurs, bigoted attacks, threats of violence (sexual or physical), comebacks targeting the speaker's family or kids, or anything that doxxes a real person. The constraints are listed in [SKILL.md](skills/clever-comebacks/SKILL.md) and they're non-negotiable. If you want a tool without those guardrails, this is not the one.

### Is it safe to install?

Yes. The skill is a single markdown file with no executable code, no network calls, no dependencies, and no telemetry. You can read every line in under a minute. The repo is scanned by gitleaks and trufflehog on every push to ensure no secrets ever ship. See [SECURITY.md](SECURITY.md) for the full threat model.

### Can I install it for one project instead of system-wide?

Yes. After running `/plugin install clever-comebacks` from inside a project directory, the plugin is registered for that project's Claude Code sessions. For manual installs, copy the skill folder into the project's `.claude/skills/` instead of your home directory:

```bash
git clone https://github.com/avectats7/clever-comebacks.git
cp -r clever-comebacks/skills/clever-comebacks your-project/.claude/skills/
```

### How do I update or uninstall?

If installed via plugin:

```bash
# Update
/plugin update clever-comebacks

# Uninstall
/plugin uninstall clever-comebacks
/plugin marketplace remove avectats7-clever-comebacks
```

If installed manually:

```bash
# Update
cd ~/.claude/skills/clever-comebacks && git pull

# Uninstall
rm -rf ~/.claude/skills/clever-comebacks
```

### Does the skill work in other Claude products?

The skill is built for Claude Code (the terminal CLI). It's plain markdown, so the methodology and examples will work as a system prompt in claude.ai or the API — but the auto-loading behavior is Claude Code specific.

### Can I contribute?

PRs are welcome — especially better example comebacks for each tier, new language variants (Spanish, French, Portuguese), and tighter methodology. Please do not open PRs that loosen the hard limits or remove the prompt-injection defenses. Those are non-negotiable.

## See also

- [SKILL.md](skills/clever-comebacks/SKILL.md) — the skill itself, including methodology, all four tiers, and hard limits (~5 KB, readable in two minutes)
- [SECURITY.md](SECURITY.md) — threat model, prompt-injection defenses, secret-scanning setup
- [Claude Code documentation](https://docs.anthropic.com/en/docs/claude-code)
- [How to write your own Claude Code skill](https://docs.anthropic.com/en/docs/claude-code/skills)

## License

MIT. Use it. Fork it. Ship comebacks.

---

*Built by [avectats7](https://github.com/avectats7). If the skill saved you a comeback, the kindest thank-you is a star on the repo and a link from your dotfiles.*
