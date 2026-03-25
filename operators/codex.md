# Codex Operator Guide

## Recommended prompt preamble
Use this preamble at task start:

```text
Operate as a retrieval-first agent over wpengine-developers-mastery.
Use local repository sources before web lookup.
State what is directly sourced versus inferred.
Keep context tight: load only files necessary for the current question.
Verify live documentation for time-sensitive or high-risk claims.
```

## Retrieval order (strict)
1. `references/99-source-manifest.md`.
2. A specific product file in `catalog/` that matches the question (prefer `overview.md`, then relevant `*-subpages.md`).
3. Additional `references/` documents only if step 2 does not fully answer the request.

Do not jump straight to broad multi-file loading.

## Answer template constraints
- Header line: **Product | Task | Confidence**.
- Mandatory sections:
  - **What the sources say** (directly grounded statements).
  - **Action plan** (clear, ordered, executable).
  - **Assumptions / inferences** (explicitly labeled).
- If giving runbook-style guidance, include **Prereqs, Execution, Verify, Backout**.
- Include precise file citations or paths for key assertions.

## When to browse / verify live docs
Perform live verification when:
- Recency matters (versions, feature availability, limits, pricing, changelog-like info).
- The user requests authoritative confirmation.
- The task is sensitive/high impact (security, production outages, traffic routing, data safety).
- Local corpus lacks the exact detail required to safely proceed.

Prefer source domains present in `references/99-source-manifest.md`.

## Max-context strategy
To stay within context limits:
- Start with `references/99-source-manifest.md` only.
- Add one narrowly relevant `catalog/...` file.
- Avoid default loading of:
  - all `catalog/platforms/**` files,
  - all `catalog/extensions/**` files,
  - all `references/*.md` files simultaneously.
- Load additional files one-by-one only when a specific missing fact is identified.
