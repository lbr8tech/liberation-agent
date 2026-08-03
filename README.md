# lbr8 Liberation Agent

An OKF knowledge bundle + skill file that turns the [lbr8 protocol card deck](https://lbr8.tech/cards) into an interactive liberation coach. Any AI agent that can read files can use this — no server, no API, no dependencies.

## What's in here

```
okf-bundle/
  SKILL.md              # Agent instructions: methodology, workflow, safety rules
  onboarding.md         # Onboarding quiz protocol (agent curates cards)
  index.md             # Card deck index with links to all cards
  cards/
    notification-audit.md
    password-manager.md
    ... (66 card files total)
```

Cards are in [Open Knowledge Format](https://github.com/GoogleCloudPlatform/knowledge-catalog/blob/main/okf/SPEC.md) — plain markdown with YAML frontmatter. Any tool, script, or agent can read them.

## Install

Paste this into your AI agent (Claude Code, Cursor, Codex, Hermes, or any agent that supports skills):

```
Clone and install the lbr8 liberation agent skill from https://forgejo.lbr8.tech/lbr8/liberation-agent — read SKILL.md and the okf-bundle/ directory, then copy them into your skill directory.
```

The agent will fetch the repo, inspect the skill file, and install it. No manual setup needed.

### Manual install

If you'd rather do it yourself:

```bash
git clone https://forgejo.lbr8.tech/lbr8/liberation-agent.git
cp -r liberation-agent/okf-bundle ~/.claude/skills/lbr8-liberation-agent
```

Adjust the destination for your agent (`~/.claude/skills/`, `~/.hermes/skills/`, `.cursor/skills/`, etc.).

## How it works

1. The agent reads `SKILL.md` and follows its instructions
2. It says the disclaimer, asks about your setup, curates relevant cards
3. It walks you through each card — step by step, with sources

## Download

Get the complete bundle at [lbr8.tech/agents](https://lbr8.tech/agents).

## License

All content — cards, skill files, and code — is licensed under [AGPLv3](LICENSE).
