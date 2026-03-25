---
name: wpengine-developers-mastery
description: Exhaustive, folderized knowledge skill for developers.wpengine.com products and subpages. Use when answering implementation, architecture, troubleshooting, and API questions across WP Engine Managed Hosting Platform, Headless Platform (Atlas), AI Toolkit, NitroPack, Advanced Custom Fields, Local, and related ecosystem tools.
---

# WP Engine Developers Mastery Skill

Use this skill to answer WP Engine developer questions with product-aware routing and subpage-level context.

## Load order

1. Read `manifest.json` first and use it as the primary lookup index for file selection.
2. Read `references/00-site-map.md` for global navigation and routing rules.
3. Read `catalog/README.md` to select product + subpage knowledge files.
4. Read only relevant product folder contents.
5. Validate critical details against live docs before production changes.

## Folder map

- `catalog/platforms/managed-hosting/`
- `catalog/platforms/headless/`
- `catalog/extensions/ai-toolkit/`
- `catalog/extensions/nitropack/`
- `catalog/plugins/advanced-custom-fields/`
- `catalog/plugins/delicious-brains-suite/`
- `catalog/tools/local/`
- `catalog/tools/faust-js/`

## Output rules for agents

- Start with product identification and confidence level.
- Separate factual summary vs inferred best practice.
- For procedures, include prerequisites, steps, validation, and rollback path.
- Link source URLs from `references/99-source-manifest.md` when citing.
