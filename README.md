# Vixal Skills

Installable Vixal skills and plugin packaging for AI-assisted manga, manhwa, webtoon, and comics creation.

See [INSTALL.md](./INSTALL.md) for user-facing setup steps.

## What Is Included

- `claude-plugins/vixal`: Claude plugin package for non-technical users.
- `vixal-skills`: Codex plugin package for developers and power users.
- `vixal-story` / `story`: Skill for story planning, character sheets, page scripts, panel breakdowns, continuity checks, and Vixal-ready generation prompts.

## Recommended Claude Setup

Normal users should use the VIXAL connector plus the VIXAL Claude plugin:

1. In Claude, connect the VIXAL MCP connector:

```text
https://www.vixal.art/api/mcp
```

2. Install the VIXAL plugin from Claude's plugin UI.
3. Start with:

```text
Use /vixal:story to turn my idea into a VIXAL project plan, then use my VIXAL connector to create the project and characters.
```

The connector controls VIXAL. The plugin teaches Claude how to plan stories, characters, chapters, page prompts, and generation steps.

## Install In Claude Code From This Marketplace

Add this repository as a Claude plugin marketplace:

```text
/plugin marketplace add ABelcaid/vixal-skills
```

Then install:

```text
/plugin install vixal@vixal
```

After installation, use:

```text
/vixal:story
```

## Install In Claude From ZIP

The Claude plugin folder is:

```text
claude-plugins/vixal
```

Zip that folder and upload it through Claude's personal plugin flow. The ZIP must contain the `.claude-plugin/plugin.json` file and the `skills/story/SKILL.md` file.

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

Claude and Claude Code can still use the standalone skill folder if you do not want the plugin wrapper:

```text
vixal-skills/skills/vixal-story
```

For Claude Code, copy it to:

```text
~/.claude/skills/vixal-story
```

For Claude.ai, the plugin route above is preferred.

## Vixal MCP

This repository does not include a Vixal MCP token. For Claude, connect the OAuth MCP connector with:

```text
https://www.vixal.art/api/mcp
```

For Codex or other clients that still use manual tokens, create a scoped token from your Vixal profile. Keep tokens private and revoke exposed tokens immediately.
