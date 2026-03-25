# WP Engine Developer Ops Runbook (Cross-Product)

## 1) Standard troubleshooting funnel

1. **Scope**: Which product area? (Headless, AI Toolkit, plugin/tooling) [source:wpengine-docs-hub]
2. **Environment**: Dev/staging/prod; identify exact target.
3. **Change event**: What changed (deploy, DNS, config, index, plugin)?
4. **Signals**: Logs, errors, request traces, behavior differences.
5. **Mitigation**: Rollback, hotfix, or config correction.
6. **Prevention**: Add checks/automation.

## 2) Build/deploy failure matrix

- Build fails:
  - Dependency or lockfile drift
  - Wrong Node version
  - Wrong build command
- Build succeeds, app fails:
  - Wrong start command
  - Missing runtime env vars
  - Code path depending on unavailable services

## 3) Domain/DNS issue matrix

- Domain unresolved: DNS record absent or not propagated
- TLS/cert pending: incomplete domain verification path
- Wrong site shows: domain mapped to incorrect environment
- Redirect loops: conflicting redirect policy across layers

## 4) Search quality issue matrix (AI Toolkit) [source:smart-search-find-api]

- Low precision: add filters, boost exact fields
- Low recall: widen tolerance and semantic support
- Ranking mismatch: rebalance weighting/time decay/promotions
- Slow responses: reduce payload fields and facet breadth

## 5) Change management checklist

Before making changes:
- Record baseline behavior.
- Confirm rollback method.
- Time-box validation window.

After making changes:
- Smoke test critical paths.
- Verify logs are clean.
- Confirm expected user-facing behavior.

## 6) Escalation payload template

When escalating internally, include:
- Product area and environment
- Exact URL(s) and timestamp(s)
- Deployment/version identifier
- Error snippet(s) and log context
- Reproduction steps
- Impact scope and urgency

## Source Links

- [source:wpengine-docs-hub] https://developers.wpengine.com/docs/ — Retrieved: 2026-03-25 (UTC) — Title: WP Engine Developers Docs Hub
- [source:atlas-runtime-logs] https://developers.wpengine.com/docs/atlas/platform-guides/runtime-logs/ — Retrieved: 2026-03-25 (UTC) — Title: Atlas runtime logs guide
- [source:smart-search-find-api] https://developers.wpengine.com/docs/wp-engine-ai-toolkit/smart-search/find-api/ — Retrieved: 2026-03-25 (UTC) — Title: Smart Search Find API docs
