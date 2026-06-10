# Install VIXAL Plugin

VIXAL Plugin adds story planning, character creation, page scripting, panel breakdowns, continuity checks, and VIXAL-ready prompt workflows to Claude, Claude Code, and Codex.

To let the assistant work inside your VIXAL account, connect the VIXAL MCP endpoint with OAuth:

```text
https://www.vixal.art/api/mcp
```

Generated images stay in VIXAL. Generation actions use your VIXAL credits.

## Claude

1. Open Claude and go to:

```text
Customize > Connectors > Add custom connector
```

2. Use:

```text
Name: VIXAL
URL: https://www.vixal.art/api/mcp
OAuth Client ID: leave empty
OAuth Client Secret: leave empty
```

3. Click **Add**, then **Connect**, and sign in with your VIXAL Google account.

4. Open:

```text
Customize > Plugins > Create plugin
```

5. Upload:

```text
dist/vixal-plugin.zip
```

6. Start a new chat with:

```text
/vixal:story
```

## Claude Code

Add the marketplace:

```text
/plugin marketplace add ABelcaid/vixal-plugin
```

Install the plugin:

```text
/plugin install vixal@vixal-plugin
```

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

Add the MCP server:

```toml
[mcp_servers.vixal]
url = "https://www.vixal.art/api/mcp"
```

Sign in:

```bash
codex mcp login vixal
```

## Recommended First Request

```text
Use Vixal Story to turn my idea into a VIXAL project plan, then use my VIXAL connector to create the project and characters.
```

## Revoke Access

Open your VIXAL profile and revoke the connected app. The assistant will no longer be able to use VIXAL tools until you connect again.
