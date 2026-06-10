# Install VIXAL Plugin

VIXAL Plugin adds story planning, character creation, page scripting, panel breakdowns, continuity checks, and VIXAL-ready prompt workflows to Claude, Claude Code, and Codex.

The plugin bundles the VIXAL MCP connector, so you do not need to add a connector manually. On first use you sign in with OAuth:

```text
https://www.vixal.art/api/mcp
```

Generated images stay in VIXAL. Generation actions use your VIXAL credits.

Step-by-step setup guide: https://www.vixal.art/plugins

## Claude Code

Add the marketplace:

```text
/plugin marketplace add ABelcaid/vixal-plugin
```

Install the plugin:

```text
/plugin install vixal@vixal-plugin
```

Approve the bundled `vixal` MCP server when prompted, then sign in:

```text
/mcp
```

Select `vixal`, choose **Authenticate**, and sign in with your VIXAL account in the browser.

Start the workflow:

```text
/vixal:story
```

## Codex

Add the marketplace:

```bash
codex plugin marketplace add ABelcaid/vixal-plugin
```

Open Codex and install **VIXAL Plugin** from:

```text
/plugins
```

The VIXAL MCP server ships with the plugin. Sign in:

```bash
codex mcp login vixal
```

## Claude (web and desktop)

1. Open Claude and go to:

```text
Customize > Plugins > Add marketplace > Add from a repository
```

2. Paste the repository:

```text
ABelcaid/vixal-plugin
```

3. Install **VIXAL Plugin** from the marketplace.

4. Connect the VIXAL connector when prompted and sign in with your VIXAL Google account.

5. Start a new chat with:

```text
/vixal:story
```

If your Claude client does not support marketplaces, upload `dist/vixal-plugin.zip` via `Customize > Plugins > Create plugin`, then add the connector manually:

```text
Customize > Connectors > Add custom connector
Name: VIXAL
URL: https://www.vixal.art/api/mcp
OAuth Client ID: leave empty
OAuth Client Secret: leave empty
```

## Recommended First Request

```text
Use Vixal Story to turn my idea into a VIXAL project plan, then create the project and characters in VIXAL.
```

## Revoke Access

Open your VIXAL profile and revoke the connected app. The assistant will no longer be able to use VIXAL tools until you connect again.
