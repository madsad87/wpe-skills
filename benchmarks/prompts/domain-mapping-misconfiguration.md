# Domain mapping misconfiguration

## Scenario
A site is reachable on its temporary platform URL but fails on the primary custom domain. The user reports intermittent TLS warnings and occasional redirects to an unexpected host. They need a concise diagnosis and recovery plan.

The assistant should cover DNS, certificate state, routing rules, and cache/propagation effects without conflating them.

## Expected answer rubric

### 1) Correctness
- Separates DNS resolution issues from application-level redirects.
- Correctly sequences checks: domain records, platform mapping, TLS/certificate status, and redirect policy.
- Includes realistic propagation and caching caveats with verification commands or checks.

### 2) Citations
- DNS, TLS, and hosting behavior claims are supported by citations.
- Any platform-specific constraints are cited from authoritative docs.
- Citations are attached to the exact claims they support.

### 3) Rollback guidance
- Offers a reversible fallback (e.g., restore previous DNS target or disable risky redirect rule).
- Defines when to pause changes and revert to last-known stable mapping.
- Includes a rollback validation checklist (HTTP status, host header behavior, certificate presentation).

### 4) Uncertainty handling
- Notes uncertainty introduced by global DNS propagation and regional cache variance.
- Explicitly identifies which observations are time-sensitive.
- Provides next diagnostic step for each unresolved branch.
