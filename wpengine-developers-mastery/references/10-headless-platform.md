# Headless Platform (Atlas) — Deep Knowledge Notes

## 1) Platform purpose

Headless Platform supports deploying and operating Node.js-based frontends backed by WordPress as a content source. [source:atlas-create-app]

Typical use cases:
- Decoupled WordPress + frontend app architecture
- Multi-environment deployment pipelines
- Managed domain mapping and observability for runtime behavior

## 2) Core lifecycle flow

### Step 1: Create app

- Provision a Headless app and environment(s).
- Establish code source and runtime defaults.

### Step 2: Connect WordPress backend

- Convert backend to headless-ready posture.
- Common plugin stack references include WPGraphQL/Faust integration components.

### Step 3: Deploy code

- Deploy from existing repository.
- Validate build and start command behavior.
- Tune custom build/start commands if project framework requires it.

### Step 4: Map domains

- Attach custom domain(s) to target environment. [source:atlas-domain-mapping]
- Define primary domain and redirect behavior.
- Review robots behavior and backend-domain strategy.

### Step 5: Observe runtime logs

- Use runtime logs to inspect startup, requests, errors, and stack traces. [source:atlas-runtime-logs]
- Triage by environment and deployment version.

## 3) Domain mapping model

### Why it matters

- Production trust and discoverability require custom domains.
- Non-production subdomains enable predictable QA and release promotion.

### Design pattern

- `production`: apex or canonical host (e.g., `mydomain.com`)
- `staging`: subdomain (e.g., `staging.mydomain.com`)
- `dev`: subdomain (e.g., `dev.mydomain.com`)
- Optional CMS/backend hostname (e.g., `cms.mydomain.com`)

### Common pitfalls

- DNS record mismatch / propagation delays
- Wrong environment bound as primary
- Redirect loops due to mixed app + proxy rules
- robots directives unintentionally blocking production indexing

## 4) Runtime logs triage playbook

When incidents occur:

1. Identify failing request path and timestamp window.
2. Correlate with last deployment.
3. Classify error family:
   - Build-time artifact mismatch
   - Missing env var or secret
   - Upstream API/network failure
   - App code exception
4. Validate fix in non-production.
5. Promote with rollback guardrails.

## 5) Deployment hardening checklist

- Pin Node.js and package manager versions.
- Make build command explicit.
- Make start command explicit.
- Validate all required env vars in CI preflight.
- Add health endpoint and smoke test after deploy.
- Capture standard log markers for tracing.

## 6) Agent-ready Q&A shortcuts

### “My deploy succeeded but app fails at runtime.”

- Check runtime logs first.
- Confirm start command and runtime assumptions.
- Verify environment variables loaded in target environment.

### “Can I use different domains per environment?”

- Yes; map separate hostnames/subdomains to each environment.
- Keep one primary per environment and configure redirects deliberately.

### “How do I productionize headless WP setup?”

- Domain mapping + robots review
- Structured release promotion
- Log-driven monitoring + rollback path

## Source Links

- [source:atlas-create-app] https://developers.wpengine.com/docs/atlas/getting-started/create-app/ — Retrieved: 2026-03-25 (UTC) — Title: Atlas create app guide
- [source:atlas-deploy-repo] https://developers.wpengine.com/docs/atlas/getting-started/deploy-from-existing-repo/ — Retrieved: 2026-03-25 (UTC) — Title: Atlas deploy from existing repo guide
- [source:atlas-domain-mapping] https://developers.wpengine.com/docs/atlas/platform-guides/domain-mapping/ — Retrieved: 2026-03-25 (UTC) — Title: Atlas domain mapping guide
- [source:atlas-runtime-logs] https://developers.wpengine.com/docs/atlas/platform-guides/runtime-logs/ — Retrieved: 2026-03-25 (UTC) — Title: Atlas runtime logs guide
