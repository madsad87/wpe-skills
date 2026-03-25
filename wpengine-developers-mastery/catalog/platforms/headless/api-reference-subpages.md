# Headless Platform — API Reference Subpages Catalog

## Purpose

Reference pages define programmatic interactions for platform automation.

## Knowledge categories to catalog per API subpage

- Authentication model and required credentials.
- Environment and app resource schemas.
- Deployment-trigger semantics.
- Pagination/filtering patterns.
- Error codes, retry behavior, and idempotency considerations.

## Agent-safe usage pattern

1. Identify exact endpoint and action.
2. Validate auth scope.
3. Build minimal request.
4. Parse response and assert success condition.
5. Add retry/backoff only where safe.
