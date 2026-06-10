# VIXAL Plugin

VIXAL Plugin helps Claude, Claude Code, and Codex plan visual stories and work inside your VIXAL account.

Use it to create story bibles, character sheets, chapter plans, page scripts, panel breakdowns, continuity checks, and VIXAL-ready generation prompts for manga, manhwa, webtoon, and comics projects.

Step-by-step setup guide: https://www.vixal.art/plugins

## How It Works

The plugin ships two things together:

- **VIXAL story skill**: teaches the assistant the VIXAL story workflow (`/vixal:story` in Claude Code, `$vixal-story` in Codex).
- **Bundled VIXAL MCP server**: the plugin includes the VIXAL MCP connector configuration, so there is no manual connector setup. You only sign in with OAuth on first use.

The bundled MCP endpoint is:

```text
https://www.vixal.art/api/mcp
```

No manual API token is required. Generation actions use your VIXAL credits, and generated images stay in your VIXAL canvas.

## Install In Claude Code

Add the marketplace and install the plugin:

```text
/plugin marketplace add ABelcaid/vixal-plugin
/plugin install vixal@vixal-plugin
```

Approve the bundled `vixal` MCP server when prompted, then authenticate:

```text
/mcp
```

Select `vixal` and choose **Authenticate** to sign in with your VIXAL account in the browser.

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

Install **VIXAL Plugin**. The VIXAL MCP server ships with the plugin, so no `config.toml` edit is needed.

Sign in with OAuth:

```bash
codex mcp login vixal
```

## Install In Claude (web and desktop)

1. Open Claude and go to:

```text
Customize > Plugins > Add marketplace > Add from a repository
```

2. Paste the repository:

```text
ABelcaid/vixal-plugin
```

3. Install **VIXAL Plugin** from the marketplace.

4. Connect the VIXAL connector when prompted and sign in with your VIXAL account.

5. Start a new chat and use:

```text
/vixal:story
```

If your Claude client does not support marketplaces, upload `dist/vixal-plugin.zip` via `Customize > Plugins > Create plugin`, then add the connector manually under `Customize > Connectors > Add custom connector` with the URL `https://www.vixal.art/api/mcp` and connect.

## First Prompt

After the plugin is installed and you are signed in, start with:

```text
Use Vixal Story to turn my idea into a VIXAL project plan, then create the project and characters in VIXAL.
```

## Permissions

After OAuth sign-in, the VIXAL connector can create and update projects, characters, and chapters, read your credit balance, start generation jobs, cancel generation jobs, and spend VIXAL credits when generation is requested.

You can revoke the connection from your VIXAL profile at any time.
