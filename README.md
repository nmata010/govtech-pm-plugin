# GovTech PM Plugin Marketplace

A Claude Code plugin marketplace containing product management tools for federal government technology teams.

## Installation

### Add the marketplace

```
/plugin marketplace add <YOUR_GITHUB_ORG/REPO>
```

### Install the plugin

```
/plugin install govtech-product-management@govtech-pm
```

### Auto-install for your team

Add this to your project's `.claude/settings.json` so team members are prompted to install automatically:

```json
{
  "extraKnownMarketplaces": {
    "govtech-pm": {
      "source": {
        "source": "github",
        "repo": "<YOUR_GITHUB_ORG/REPO>"
      }
    }
  },
  "enabledPlugins": {
    "govtech-product-management@govtech-pm": true
  }
}
```

## Plugins

### govtech-product-management

Product management for federal digital services. Covers the full PM workflow within the federal acquisition lifecycle: writing specs mapped to contract scope, managing roadmaps around periods of performance, communicating with government stakeholders, synthesizing user research under PRA constraints, analyzing competitors using federal procurement data, and tracking metrics against QASP targets.

See the [plugin README](govtech-product-management/README.md) for full documentation including commands, skills, example workflows, and data source connectors.
