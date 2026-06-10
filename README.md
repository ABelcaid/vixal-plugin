# VIXAL Plugin

VIXAL Plugin helps Claude, Claude Code, and Codex plan visual stories and work with VIXAL projects through the VIXAL OAuth MCP connector.

Use it to create story bibles, character sheets, chapter plans, page scripts, panel breakdowns, continuity checks, and VIXAL-ready generation prompts for manga, manhwa, webtoon, and comics projects.

## How It Works

VIXAL uses two pieces together:

- **VIXAL Plugin**: teaches the assistant the VIXAL story workflow.
- **VIXAL MCP connector**: gives the assistant permission to work inside your VIXAL account after OAuth sign-in.

The connector uses:

```text
https://www.vixal.art/api/mcp
```

No manual API token is required. Generation actions use your VIXAL credits, and generated images stay in your VIXAL canvas.

## Install In Claude

1. Open Claude and go to:

```text
Customize > Connectors > Add custom connector
```

2. Name the connector `VIXAL` and paste:

```text
https://www.vixal.art/api/mcp
```

3. Click **Add**, then **Connect**, and sign in with your VIXAL Google account.

4. Install the VIXAL Plugin from Claude's plugin UI:

```text
Customize > Plugins > Create plugin
```

5. Upload:

```text
dist/vixal-plugin.zip
```

6. Start a new chat and use:

```text
/vixal:story
```

## Install In Claude Code

Add the marketplace:

```text
/plugin marketplace add ABelcaid/vixal-plugin
```

Install the plugin:

```text
/plugin install vixal@vixal-plugin
```

Use the VIXAL story workflow:

```text
/vixal:story
```

The plugin name is `vixal`. The marketplace name is `vixal-plugin`.

## Install In Codex

Add the marketplace:

```bash
codex plugin marketplace add ABelcaid/vixal-plugin
```

Open Codex, go to:

```text
/plugins
```

Install **VIXAL Plugin**.

Add the VIXAL MCP server:

```toml
[mcp_servers.vixal]
url = "https://www.vixal.art/api/mcp"
```

Sign in with OAuth:

```bash
codex mcp login vixal
```

## First Prompt

After the plugin and connector are installed, start with:

```text
Use Vixal Story to turn my idea into a VIXAL project plan, then use my VIXAL connector to create the project and characters.
```

## Permissions

After OAuth sign-in, the VIXAL connector can create and update projects, characters, and chapters, read your credit balance, start generation jobs, cancel generation jobs, and spend VIXAL credits when generation is requested.

You can revoke the connection from your VIXAL profile at any time.
