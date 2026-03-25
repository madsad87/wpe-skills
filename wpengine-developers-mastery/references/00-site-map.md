# WP Engine Developers — Deep Site Map & Routing Index

_Last synthesized: 2026-03-25 (UTC). [source:source-manifest]_

## Canonical top-level taxonomy (from docs hub) [source:wpengine-docs-hub]

- Platforms
  - Managed Hosting Platform
  - Headless Platform
- Product Extensions
  - AI Toolkit
  - NitroPack
- Plugins
  - Advanced Custom Fields
  - WP Migrate
  - WP Offload Media
  - WP Offload SES
  - Better Search Replace
- Tools
  - Faust.js
  - Local

## Product-to-folder routing

- Managed Hosting Platform → `catalog/platforms/managed-hosting/`
- Headless Platform (Atlas) → `catalog/platforms/headless/`
- AI Toolkit → `catalog/extensions/ai-toolkit/`
- NitroPack → `catalog/extensions/nitropack/`
- Advanced Custom Fields → `catalog/plugins/advanced-custom-fields/`
- WP Migrate/WP Offload*/Better Search Replace → `catalog/plugins/delicious-brains-suite/`
- Local → `catalog/tools/local/`
- Faust.js → `catalog/tools/faust-js/`

## Headless subpage catalog (knowledge clusters)

- Getting Started:
  - Create App
  - Deploy from Existing Repo
  - Connect to Headless WordPress
- Platform Guides:
  - Domain Mapping
  - Runtime Logs
  - Build/start/runtime operations themes
- Framework Guides:
  - Framework-specific deployment and runtime behavior
- API Reference:
  - Programmatic app/environment/deploy interactions

## AI Toolkit subpage catalog (knowledge clusters)

- Smart Search:
  - Find API (GraphQL query + relevance controls)
  - Indexing/settings themes
- Recommendations:
  - Related-content and suggestion flows
- Vector Database:
  - Embeddings, chunking, vector retrieval
- Plugin Developer docs:
  - Customization/extension patterns

## Agent operating protocol

1. Check `manifest.json` first to find candidate files by product/subproduct/topics.
2. Identify product bucket first.
3. Load product `overview.md`.
4. Load matching `*-subpages.md` file.
5. Answer with procedural structure + risk controls.
6. Validate precise API details against live docs before production.
1. Identify product bucket first.
2. Load product `overview.md`.
3. Load matching `*-subpages.md` file.
4. Answer with procedural structure + risk controls.
5. Validate precise API details against live docs before production.

## Source Links

- [source:wpengine-docs-hub] https://developers.wpengine.com/docs/ — Retrieved: 2026-03-25 (UTC) — Title: WP Engine Developers Docs Hub
- [source:source-manifest] ./99-source-manifest.md — Retrieved: 2026-03-25 (UTC) — Title: Internal source manifest
