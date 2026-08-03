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

### Hermes Agent
```bash
mkdir -p ~/.hermes/skills/lbr8-liberation-agent
# Copy SKILL.md and okf-bundle/ into that directory
```

### Claude Desktop / Cursor / any agent with skill support
Place `SKILL.md` and `okf-bundle/` in your agent's skill directory. Any agent that can read files can use this.

### Just the data
The cards are plain markdown. Read them with any tool — `cat`, `grep`, a script, or your agent.

## How it works

1. Copy `SKILL.md` and `okf-bundle/` to your agent's skill directory
2. Start a conversation — the agent reads `SKILL.md` and follows its instructions
3. It says the disclaimer, asks about your setup, curates relevant cards, and walks you through each one

## Download

Get the complete bundle at [lbr8.tech/agents](https://lbr8.tech/agents).

## License

All content — cards, skill files, and code — is licensed under [AGPLv3](LICENSE).
