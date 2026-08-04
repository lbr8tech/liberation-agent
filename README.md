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

### Claude.ai

1. Download the ZIP from [lbr8.tech/agent](https://lbr8.tech/agent) (click "Download skill bundle").
2. Go to **Settings > Capabilities** and enable **Code execution and file creation**.
3. Go to **Customize > Skills**, click **+**, then **Upload a skill**.
4. Select the ZIP file. Toggle the skill on.

### Claude Code, Hermes, Codex, Gemini CLI, and other CLI agents

```bash
git clone https://forgejo.lbr8.tech/lbr8/liberation-agent.git
cp -r liberation-agent ~/.claude/skills/liberation-agent
```

Adjust the destination for your agent (`~/.claude/skills/`, `~/.hermes/skills/`, `~/.gemini/skills/`, `~/.codex/skills/`, etc.). The skill is auto-discovered on next launch.

### ChatGPT, Gemini, and other web-based AI

1. Download the ZIP from [lbr8.tech/agent](https://lbr8.tech/agent) and unzip it.
2. Open `SKILL.md` and copy its contents.
3. Paste into your AI's custom instructions or a new Project / Gem.
4. Copy the contents of `onboarding.md` and add that too.

The coaching instructions live in `SKILL.md` and the onboarding quiz lives in `onboarding.md`. Your AI will follow them for the rest of the conversation.

### Or just ask your AI

```
Install the lbr8 liberation agent skill from https://forgejo.lbr8.tech/lbr8/liberation-agent — read SKILL.md and the cards/ directory, then follow the onboarding instructions.
```

If your agent can fetch URLs and install skills itself, paste this. Not all agents support this — Claude.ai and ChatGPT will refuse for security reasons, and that's expected. Use the methods above instead.

## How it works

1. The agent reads `SKILL.md` and follows its instructions
2. It says the disclaimer, asks about your setup, curates relevant cards
3. It walks you through each card — step by step, with sources

## Download

Get the complete bundle at [lbr8.tech/agent](https://lbr8.tech/agent).

## License

All content — cards, skill files, and code — is licensed under [AGPLv3](LICENSE).
