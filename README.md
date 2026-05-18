# amlmarketplaces/huggingface

Claude Code marketplace federating all `@amlplugins/huggingface-*` plugins.

## Install

Add to your project's `.claude/settings.json`:

```json
{
  "extraKnownMarketplaces": {
    "aml-huggingface": {
      "source": { "source": "github", "repo": "amlmarketplaces/huggingface" }
    }
  },
  "enabledPlugins": {
      "huggingface-agents@aml-huggingface": true,
      "huggingface-hub@aml-huggingface": true,
      "huggingface-inference@aml-huggingface": true
    }
}
```

Then launch Claude Code in the project. The marketplace is fetched from `amlmarketplaces/huggingface`, cached under `~/.claude/plugins/cache/aml-huggingface/`, and each enabled plugin is loaded from its `amlplugins` source repo.

## Plugins (3 total)

- `huggingface-agents` — [@amlplugins/huggingface-agents](https://github.com/amlplugins/huggingface-agents)
- `huggingface-hub` — [@amlplugins/huggingface-hub](https://github.com/amlplugins/huggingface-hub)
- `huggingface-inference` — [@amlplugins/huggingface-inference](https://github.com/amlplugins/huggingface-inference)

## Related

- npm packages: `@amlplugins/huggingface-*` published to GitHub Packages (`https://npm.pkg.github.com`).
- Aggregating parent: [`amlmarketplaces/aml`](https://github.com/amlmarketplaces/aml) — federates every `@amlplugins/*` plugin under a single marketplace.
- AML topology: see `.claude/rules/definitions/ageni.md` § "GitHub Topology" — this repository is a Tier-4 HUB-INSTANCE under the `amlmarketplaces/` Tier-3 HUB-ORGANIZATION.

> Built by `.claude/skills/aml/metateam/marketplace/test/cross-org-amlmarketplaces-batch.mjs`.
