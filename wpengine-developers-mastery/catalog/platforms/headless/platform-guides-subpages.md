# Headless Platform — Platform Guides Subpages Catalog

## Subpage cluster: Domain Mapping

### Knowledge contained

- Mapping custom domains to app environments. [source:atlas-domain-mapping]
- Primary domain assignment and redirect logic.
- Environment-specific domain strategy (dev/stage/prod).

### Agent runbook

1. Confirm target environment.
2. Validate DNS records and propagation.
3. Set primary domain.
4. Validate redirect behavior and robots policy.

## Subpage cluster: Runtime Logs

### Knowledge contained

- Accessing runtime application logs. [source:atlas-runtime-logs]
- Interpreting errors by deployment and timestamp.
- Correlating failures to specific release events.

### Agent runbook

1. Collect error timestamp and path.
2. Cross-reference most recent deploy.
3. Bucket root cause (config, dependency, code, upstream API).
4. Recommend rollback or patch.

## Additional platform-guide themes (common in Atlas docs)

- Build/start command overrides.
- Environment variable management.
- Performance and reliability hardening.

## Source Links

- [source:atlas-domain-mapping] https://developers.wpengine.com/docs/atlas/platform-guides/domain-mapping/ — Retrieved: 2026-03-25 (UTC) — Title: Atlas domain mapping guide
- [source:atlas-runtime-logs] https://developers.wpengine.com/docs/atlas/platform-guides/runtime-logs/ — Retrieved: 2026-03-25 (UTC) — Title: Atlas runtime logs guide
