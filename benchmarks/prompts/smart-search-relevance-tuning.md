# Smart Search relevance tuning

## Scenario
Search results quality regressed after a content and plugin update. Users report that high-intent queries now surface outdated or low-value pages. The team wants recommendations for relevance tuning with minimal risk.

The assistant should propose a measurable tuning workflow rather than one-off tweaks.

## Expected answer rubric

### 1) Correctness
- Recommends a repeatable relevance process (baseline metrics, hypothesis, change, evaluation).
- Distinguishes indexing issues from ranking/scoring issues.
- Suggests safe, high-impact levers first (field weights, synonym controls, stopwords, boosting rules, recency handling).

### 2) Citations
- Search behavior and configuration guidance is supported with citations.
- Metrics recommendations are grounded in cited best practices or product docs.
- Cited material aligns with the proposed tuning levers.

### 3) Rollback guidance
- Specifies how to revert tuning changes quickly (versioned config, staged rollout, feature flag).
- Defines guardrail thresholds that trigger rollback.
- Includes post-rollback validation to confirm relevance recovery.

### 4) Uncertainty handling
- Calls out data quality gaps (query logs, click data, zero-result rates).
- Uses confidence language proportional to available evidence.
- Provides an incremental experiment plan when certainty is low.
