# Local-to-hosting promotion workflow

## Scenario
A team wants to promote a locally validated WordPress change set to managed hosting across non-production and production environments. They need a robust workflow that minimizes downtime and configuration drift.

The assistant should address data, code, environment config, and release orchestration.

## Expected answer rubric

### 1) Correctness
- Outlines an end-to-end promotion flow: local validation, integration checks, staged deploy, production cutover.
- Accounts for environment-specific settings (secrets, domain URLs, caching, cron, third-party integrations).
- Includes preflight and post-deploy verification steps with clear success criteria.

### 2) Citations
- Workflow guidance and platform-specific operations are cited.
- Citations support critical safety steps (backups, DB handling, environment config controls).
- Claims about deployment semantics are not left uncited.

### 3) Rollback guidance
- Defines rollback artifacts and ownership (backup snapshot, previous release package, DB restore point).
- Provides explicit rollback trigger conditions.
- Includes rollback drill or smoke-test recommendations.

### 4) Uncertainty handling
- Flags assumptions that commonly break across environments.
- Identifies unknowns requiring confirmation before production promotion.
- Proposes phased rollout when system behavior is uncertain.
