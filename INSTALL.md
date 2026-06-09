# Install VIXAL In Claude And Codex

## Claude For Normal Users

1. Connect VIXAL in Claude:

```text
Customize > Connectors > Add custom connector
URL: https://www.vixal.art/api/mcp
```

2. Install the VIXAL plugin:

```text
Customize > Plugins > Create plugin
```

Upload:

```text
dist/vixal-claude-plugin.zip
```

3. Start a new Claude chat and use:

```text
/vixal:story
```

Example prompt:

```text
Use /vixal:story to turn my idea into a VIXAL project plan, then use my VIXAL connector to create the project and characters.
```

## Claude Code / Claude Desktop

Add this marketplace:

```text
/plugin marketplace add ABelcaid/vixal-skills
```

Install:

```text
/plugin install vixal@vixal
```

Use:

```text
/vixal:story
```

## Codex

Add this marketplace:

```bash
codex plugin marketplace add ABelcaid/vixal-skills
```

Then install **Vixal Skills** from `/plugins`.

## What The Plugin Does

The VIXAL plugin gives Claude story-direction and prompt-writing behavior. The VIXAL connector gives Claude permission to create projects, characters, chapters, and generation jobs inside VIXAL.
