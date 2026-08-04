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

### Claude.ai (Free / Pro / Max)

1. Download the ZIP from [lbr8.tech/agent](https://lbr8.tech/agent) (click "Download skill bundle").
2. Go to **Settings > Capabilities** and enable **Code execution and file creation**.
3. Go to **Customize > Skills**, click **+**, then **Upload a skill**.
4. Select the ZIP file. Toggle the skill on.

### ChatGPT Plus / Pro (Paid)

1. Download the ZIP from [lbr8.tech/agent](https://lbr8.tech/agent) and unzip it.
2. Create a new **Project** in ChatGPT.
3. Upload `SKILL.md` and `onboarding.md` as reference files.
4. Set the project instructions to: *"Read the uploaded SKILL.md and onboarding.md files. Follow the instructions in SKILL.md. Start by conducting the onboarding quiz from onboarding.md."*

Start new chats inside the project. The uploaded files give ChatGPT the full skill context.

### ChatGPT Free (Limited)

1. Download the ZIP from [lbr8.tech/agent](https://lbr8.tech/agent) and unzip it.
2. Open `SKILL.md` and copy the full contents.
3. Start a new chat and paste: *"Follow the instructions below for this conversation"* — then paste the SKILL.md content.
4. Do the same with `onboarding.md` in a follow-up message.

This only lasts for one conversation — you'll need to re-paste for each new chat. For a persistent setup, upgrade to Plus and use Projects (above), or use Claude.ai which supports skills on the free tier.

### Gemini (Free / Paid)

1. Download the ZIP from [lbr8.tech/agent](https://lbr8.tech/agent) and unzip it.
2. Go to [gemini.google.com](https://gemini.google.com) → **Gems** → **New Gem**.
3. Upload `SKILL.md` and `onboarding.md` as **Knowledge** files.
4. Set the Gem instructions to: *"Read the uploaded SKILL.md and onboarding.md files. Follow the instructions in SKILL.md. Start by conducting the onboarding quiz from onboarding.md."*

### Claude Code, Hermes, Codex, Gemini CLI (CLI)

```bash
git clone https://github.com/lbr8tech/liberation-agent.git
cp -r liberation-agent ~/.claude/skills/liberation-agent
```

Adjust the destination for your agent: `~/.claude/skills/` (Claude Code), `~/.hermes/skills/` (Hermes), `~/.codex/skills/` (Codex), `~/.gemini/skills/` (Gemini CLI). The skill is auto-discovered on next launch.

### Other AI that can fetch URLs

```
Install the lbr8 liberation agent skill from https://github.com/lbr8tech/liberation-agent — read SKILL.md and the cards/ directory, then follow the onboarding instructions.
```

Some agents can fetch URLs and install skills themselves. Claude.ai and ChatGPT will refuse this for security reasons — that's expected. Use the manual methods above instead.

## How it works

1. The agent reads `SKILL.md` and follows its instructions
2. It says the disclaimer, asks about your setup, curates relevant cards
3. It walks you through each card — step by step, with sources

## Download

Get the complete bundle at [lbr8.tech/agent](https://lbr8.tech/agent).

## License

All content — cards, skill files, and code — is licensed under [AGPLv3](LICENSE).
