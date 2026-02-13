# GovTech PM Plugin Marketplace

A product management plugin customized to US Federal Government digital services workflows. Adapted from Anthropic's [knowledge-work-plugins](https://github.com/anthropics/knowledge-work-plugins). 

## Installation

### Cowork (Claude Desktop)

1. Open Claude for Desktop and switch to **Cowork**
2. Click **Customize with plugins**. From the dropdown select **Add marketplace from GitHub**
4. Enter URL: `https://github.com/nmata010/govtech-pm-plugin.git` and click **Sync** (this loads the available plugins)
5. Select **Govtech Product Management** from the list and click **Install**
6. Use any of the slash commands to get started

### Claude Code

1. **Add the marketplace:** `/plugin marketplace add https://github.com/nmata010/govtech-pm-plugin.git`
2. **Install the plugin:** `/plugin install govtech-product-management@govtech-pm`

### Auto-install for teams

Update your project's `.claude/settings.json` so team members are prompted to install automatically:

```json
{
  "extraKnownMarketplaces": {
    "govtech-pm": {
      "source": {
        "source": "github",
        "repo": "https://github.com/nmata010/govtech-pm-plugin.git"
      }
    }
  },
  "enabledPlugins": {
    "govtech-product-management@govtech-pm": true
  }
}
```

## Included Plugins

### Govtech Product Management

Product management for federal digital services. Covers the full PM workflow within the federal acquisition lifecycle: writing specs mapped to contract scope, managing roadmaps around periods of performance, communicating with government stakeholders, synthesizing user research under PRA constraints, analyzing competitors using federal procurement data, and tracking metrics against QASP targets.

See the [plugin README](govtech-product-management/README.md) for full documentation including commands, skills, example workflows, and data source connectors.
