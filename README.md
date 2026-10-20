# Lindo AI — Claude Code Plugin Marketplace

Official plugin marketplace for [Lindo AI](https://lindo.ai). Install the Lindo AI plugin in Claude Code to create websites, pages, and blog posts with AI.

## Quick Start

### Claude Desktop (Cowork)

1. Open **Customize** → **Personal plugins** → **Browse plugins**
2. Click the **+** button next to "Personal plugins"
3. In the "Add marketplace" dialog, enter:

```
lindoai/lindoai-claude-marketplace
```

4. Click **Sync**
5. Browse and install the `lindo-ai` plugin

### Claude Code (CLI)

Add the marketplace:

```bash
claude plugin marketplace add lindoai/lindoai-claude-marketplace
```

Install the plugin:

```bash
claude plugin install lindo-ai@lindo-marketplace
```

## Setup

You need a Lindo AI API key. Get one from your workspace settings at [app.lindo.ai](https://app.lindo.ai).

Set your API key:

```bash
export LINDO_API_KEY=lindo_sk_live_...
```

Or the plugin will open a browser login flow on first use.

## Available Plugins

### lindo-ai

Create websites, pages, and blog posts with AI. Manage clients, credits, and domains — all through conversation.

**Skills included:**

| Skill | Description |
|-------|-------------|
| create-website | Create a new website with AI |
| edit-website | Edit an existing website using AI |
| create-blog | Generate a blog post with AI |
| manage-clients | Create, list, assign, and manage clients |
| manage-websites | View, update, and configure websites |
| manage-content | Publish, edit, and manage pages and blogs |

## What you can do

- **Create websites** — "Build a portfolio website for a photographer"
- **Add pages** — "Add a pricing page to my website"
- **Write blog posts** — "Write a blog post about SEO tips"
- **Manage clients** — "Create a client for Acme Corp"
- **Allocate credits** — "Give 500 credits to my client"
- **Custom domains** — "Add example.com to my website"
- **Analytics** — "Show me traffic for my website"

## Requirements

- [Claude Code](https://code.claude.com) CLI or Claude Desktop (Team/Enterprise plan)
- [Lindo AI](https://lindo.ai) account with Business or Whitelabel plan
- Node.js 18+

## For Teams

Add this marketplace to your project's `.claude/settings.json` to share with your team:

```json
{
  "extraKnownMarketplaces": {
    "lindo-marketplace": {
      "source": {
        "source": "github",
        "repo": "lindoai/lindoai-claude-marketplace"
      }
    }
  },
  "enabledPlugins": {
    "lindo-ai@lindo-marketplace": true
  }
}
```

## Links

- [Lindo AI](https://lindo.ai)
- [Documentation](https://lindo.ai/docs)
- [API Reference](https://api.lindo.ai/docs)
- [Claude Code Plugin](https://github.com/lindoai/claude-plugin)
- [MCP Server](https://github.com/lindoai/mcp-server)

## License

MIT
