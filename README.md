# Vixal Skills

Installable Vixal skills and Codex plugin packaging for AI-assisted manga, manhwa, webtoon, and comics creation.

## What Is Included

- `vixal-skills`: Codex plugin package.
- `vixal-story`: Skill for story planning, character sheets, page scripts, panel breakdowns, continuity checks, and Vixal-ready generation prompts.

## Install In Codex

Add this repository as a Codex plugin marketplace:

```bash
codex plugin marketplace add ABelcaid/vixal-skills
```

Then open Codex and install **Vixal Skills**:

```text
/plugins
```

After installation, start a new thread and ask:

```text
Use Vixal Story to turn my manga idea into a Vixal project plan.
```

## Install As A Local Codex Skill

If you only want the skill without the plugin wrapper, copy:

```text
vixal-skills/skills/vixal-story
```

to:

```text
~/.codex/skills/vixal-story
```

Restart Codex after copying.

## Install In Claude

Claude and Claude Code can use the same skill folder:

```text
vixal-skills/skills/vixal-story
```

For Claude Code, copy it to:

```text
~/.claude/skills/vixal-story
```

For Claude.ai, zip the `vixal-story` folder and upload it from Claude's custom skills settings.

## Vixal MCP

This repository does not include a Vixal MCP token. Create a scoped MCP token from your Vixal profile, then configure your MCP client with:

```text
https://www.vixal.art/api/mcp
```

Keep tokens private and revoke exposed tokens immediately.
