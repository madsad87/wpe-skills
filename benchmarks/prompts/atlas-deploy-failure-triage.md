# Atlas deploy failure triage

## Scenario
A production deployment on WP Engine Atlas failed during the release window. The user needs an actionable triage response that:

- identifies likely root causes from symptoms,
- prioritizes immediate stabilization,
- proposes a safe recovery sequence,
- and communicates what to verify before retrying deployment.

The assistant should avoid guessing undocumented facts and should separate confirmed signals from hypotheses.

## Expected answer rubric

### 1) Correctness
- Diagnoses are consistent with the presented failure symptoms.
- Triage sequence is ordered by impact and reversibility.
- Recommendations include concrete validation steps before and after remediation.

### 2) Citations
- Claims tied to platform behavior or runbooks are backed by citations.
- Citations point to relevant source material, not generic top-level docs.
- If a recommendation is inferential, the answer explicitly labels it as an inference.

### 3) Rollback guidance
- Includes a rollback decision point with clear trigger conditions.
- Provides a low-risk rollback path (e.g., last known good release, config restore, or traffic re-route).
- Notes post-rollback verification checks and stakeholder communication expectations.

### 4) Uncertainty handling
- Distinguishes known facts, unknowns, and assumptions.
- Requests the minimum additional evidence required to disambiguate root cause.
- Avoids overconfident language when logs/telemetry are incomplete.
