# lbr8 Liberation Agent

An [Agent Skills](https://agentskills.io)-compatible skill that turns the [lbr8 protocol card deck](https://lbr8.tech/cards) into an interactive liberation coach. Any AI agent that supports the open SKILL.md standard can use this — Claude Code, OpenAI Codex, Gemini CLI, GitHub Copilot, Cursor, Hermes, and 20+ others. No server, no API, no dependencies.

## What's in here

```
liberation-agent/
  SKILL.md              # Agent instructions: methodology, workflow, safety rules
  onboarding.md         # Onboarding quiz protocol (agent curates cards)
  index.md              # Card deck index with links to all cards
  cards/                # 66 protocol cards (plain markdown + YAML frontmatter)
    notification-audit.md
    password-manager.md
    ...
  marketplace.json      # Plugin marketplace manifest for one-command install
  LICENSE               # AGPLv3
```

Cards are in [Open Knowledge Format](https://github.com/GoogleCloudPlatform/knowledge-catalog/blob/main/okf/SPEC.md) — plain markdown with YAML frontmatter. Any tool, script, or agent can read them.

## Install

### One-command (Claude Code)

```
/plugins marketplace add https://forgejo.lbr8.tech/lbr8/liberation-agent
/plugins install liberation-agent@lbr8
```

### One-command (GitHub Copilot)

```
copilot plugin marketplace add lbr8/liberation-agent
copilot plugin install liberation-agent@lbr8
```

### Any agent (paste this)

```
Clone and install the lbr8 liberation agent skill from https://forgejo.lbr8.tech/lbr8/liberation-agent — read SKILL.md and the cards/ directory, then copy them into your skill directory.
```

The agent will fetch the repo, inspect the skill file, and install it. No manual setup needed.

### Manual install

If you'd rather do it yourself:

```bash
git clone https://forgejo.lbr8.tech/lbr8/liberation-agent.git
cp -r liberation-agent ~/.claude/skills/liberation-agent
```

Adjust the destination for your agent (`~/.claude/skills/`, `~/.hermes/skills/`, `.cursor/skills/`, `~/.gemini/skills/`, etc.).

## How it works

1. The agent reads `SKILL.md` and follows its instructions
2. It says the disclaimer, asks about your setup, curates relevant cards
3. It walks you through each card — step by step, with sources

## Download

Get the complete bundle at [lbr8.tech/agents](https://lbr8.tech/agents).

## License

All content — cards, skill files, and code — is licensed under [AGPLv3](LICENSE).
