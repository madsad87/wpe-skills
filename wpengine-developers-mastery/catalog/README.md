# Product & Subpage Catalog

This catalog is organized by the same top-level product taxonomy shown in WP Engine Developer docs.

## Platforms

- `platforms/managed-hosting/`
  - `overview.md`
  - `onboarding-and-environments.md`
  - `domains-ssl-and-routing.md`
  - `operations-observability-and-security.md`
- `platforms/headless/`
  - `overview.md`
  - `getting-started-subpages.md`
  - `platform-guides-subpages.md`
  - `framework-guides-subpages.md`
  - `api-reference-subpages.md`

## Product Extensions

- `extensions/ai-toolkit/`
  - `overview.md`
  - `smart-search-subpages.md`
  - `recommendations-subpages.md`
  - `vector-database-subpages.md`
  - `plugin-developer-subpages.md`
- `extensions/nitropack/`
  - `overview.md`

## Plugins

- `plugins/advanced-custom-fields/`
  - `overview.md`
  - `key-concepts-subpages.md`
- `plugins/delicious-brains-suite/`
  - `overview.md`

## Tools

- `tools/local/`
  - `overview.md`
  - `workflow-capabilities-subpages.md`
- `tools/faust-js/`
  - `overview.md`

## How to use with an agent

1. Open `manifest.json` and filter by `product`, `subproduct`, and `topics`.
2. Detect product scope from the user request.
3. Open the product `overview.md`.
4. Open the corresponding `*-subpages.md` file for granular knowledge clusters.
5. Produce answer using templates in `references/40-agent-response-templates.md`.
