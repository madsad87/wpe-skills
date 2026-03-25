# WPEngine Developers Mastery

## 1) Purpose

This knowledge base (KB) is a compact, navigable guide for people and AI agents who need to work quickly inside the WP Engine developer ecosystem. It is designed for platform engineers, WordPress developers, support/operations responders, solutions architects, and automation agents that need reliable routing to the right docs and runbooks. It is intentionally **not** a full mirror of documentation; it is a synthesized, agent-oriented map of [developers.wpengine.com](https://developers.wpengine.com) that prioritizes actionability, source traceability, and fast issue triage.

## 2) Quick Start (Human + Agent)

### Human path

1. Open [`catalog/README.md`](./catalog/README.md).
2. Pick the product family (Platforms, Tools, Plugins, Extensions).
3. Open the relevant product folder and start with `overview.md`.
4. Follow linked `*-subpages.md` files for deeper workflows.

### Agent path

1. Open [`SKILL.md`](./SKILL.md) to load operating instructions.
2. Read [`references/00-site-map.md`](./references/00-site-map.md) for high-level URL topology.
3. Route to the matching `catalog/**` entries for task-specific details.
4. Cross-check provenance in [`references/99-source-manifest.md`](./references/99-source-manifest.md).

## 3) Repository Structure

```text
wpengine-developers-mastery/
├─ SKILL.md
├─ manifest.json
├─ README.md
├─ catalog/
│  ├─ README.md
│  ├─ platforms/
│  │  ├─ headless/
│  │  └─ managed-hosting/
│  ├─ tools/
│  │  ├─ local/
│  │  └─ faust-js/
│  ├─ plugins/
│  │  ├─ advanced-custom-fields/
│  │  └─ delicious-brains-suite/
│  └─ extensions/
│     ├─ ai-toolkit/
│     └─ nitropack/
└─ references/
   ├─ 00-site-map.md
   ├─ 10-headless-platform.md
   ├─ 20-ai-toolkit-smart-search.md
   ├─ 30-api-ops-runbook.md
   ├─ 40-agent-response-templates.md
   └─ 99-source-manifest.md
```

### Major folder guide

- `catalog/` — Product-oriented navigation and synthesized operating knowledge.
- `catalog/platforms/` — Platform-level behaviors (Headless + Managed Hosting).
- `catalog/tools/` — Developer tools and local/dev workflow material.
- `catalog/plugins/` — Plugin-specific concepts and implementation guidance.
- `catalog/extensions/` — Extension integrations, AI Toolkit, and ecosystem add-ons.
- `references/` — Cross-cutting maps, runbooks, response templates, and source metadata.

## 4) Source of Truth & Freshness

- Primary provenance is tracked in [`references/99-source-manifest.md`](./references/99-source-manifest.md).
- Every synthesized section should map back to one or more source URLs listed there.
- Treat freshness fields as explicit time semantics:
  - **`last verified`** = when a human/agent re-checked that summarized guidance still matches the source.
  - **`retrieved`** = when the raw source content was pulled for this KB.
- When dates drift or confidence drops, refresh summaries before relying on details for production decisions.

## 5) How to Contribute

Use this lightweight workflow whenever you add or update a page:

1. **Identify source URL(s)**
   - Choose canonical docs from `developers.wpengine.com` (or clearly documented related official pages).
2. **Summarize by subpage cluster**
   - Group notes by workflow/task area, not by random page order.
   - Prefer concise operational summaries over copy-paste prose.
3. **Add or refresh source links**
   - Ensure each summary block has clear source attribution.
   - Update `references/99-source-manifest.md` if URLs, sections, or retrieval dates changed.
4. **Mark confidence**
   - Label claims as `high`, `medium`, `low`, or `inferred` when direct confirmation is incomplete.
   - Keep uncertainty explicit rather than implied.

## 6) Quality Bar

Contributions should meet all of the following:

- **Product routing clarity**
  - A reader/agent can quickly identify the right product path from symptoms or goals.
- **Actionable runbooks**
  - Include concrete steps, decisions, and escalation paths (not only conceptual summaries).
- **Citation links**
  - Tie claims to source URLs or internal reference files.
- **Uncertainty labeling**
  - Explicitly mark assumptions, inferred behavior, and stale/unverified sections.

If any criterion is missing, treat the update as incomplete.

## 7) Usage Examples

Use prompts like these to activate this KB effectively:

1. **Atlas deploy issues**
   - "Diagnose an Atlas deploy failure where build succeeds but runtime errors on environment variables; give a triage checklist and likely root causes."
2. **Smart Search tuning**
   - "Tune Smart Search relevance for a product catalog with synonym-heavy queries; propose settings, validation steps, and rollback plan."
3. **Local workflow**
   - "Provide a Local-to-WP Engine promotion workflow with preflight checks, DB/media handling, and post-deploy verification tasks."
4. **ACF schema planning**
   - "Plan an ACF schema migration across environments with field group versioning, risk controls, and deployment sequencing."
5. **Cross-product routing**
   - "Given symptoms around API auth, SSL redirects, and headless preview breakage, map me to the correct sections of this KB and recommended first checks."

---

### Keep this README lean

- Use this file for orientation and contribution expectations.
- Put detailed workflows in `catalog/` and cross-cutting operational references in `references/`.
- Prefer linking over duplicating long-form detail.
