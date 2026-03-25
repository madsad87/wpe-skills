# ACF schema migration risk review

## Scenario
A proposed Advanced Custom Fields (ACF) schema migration introduces field restructuring, key renames, and content model changes. The team needs a risk review before rollout to avoid data loss and frontend regressions.

The assistant should provide a migration risk assessment and a pragmatic mitigation plan.

## Expected answer rubric

### 1) Correctness
- Identifies migration risk classes: data compatibility, field key/name mapping, template coupling, serialization impacts, and editor workflow changes.
- Recommends validation for both data integrity and rendered output.
- Includes backward-compatibility or dual-read strategy where appropriate.

### 2) Citations
- ACF and WordPress migration-related claims are backed by citations.
- Risk controls (backup, staging test, scripted migration, idempotency) are supported by sources.
- Citations are specific enough to verify technical assertions.

### 3) Rollback guidance
- Provides a concrete rollback strategy for schema and content state.
- Defines restoration order (code, schema definition, data) and verification after restore.
- Warns about partial rollback pitfalls and how to avoid them.

### 4) Uncertainty handling
- Explicitly labels assumptions about existing data shape and plugin versions.
- Recommends sampling strategy to uncover edge cases before full migration.
- States confidence limits and what additional evidence would increase confidence.
