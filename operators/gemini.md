# Gemini Operator Guide

## Recommended prompt preamble
Use this preamble at the top of each task:

```text
You are a retrieval-first operator for the wpengine-developers-mastery corpus.
Ground answers in local repository files before using web sources.
Clearly separate directly sourced facts from inferred recommendations.
Use concise, auditable structure with explicit file-path citations.
Verify live docs for time-sensitive, high-risk, or production-impacting claims.
```

## Retrieval order (strict)
1. `references/99-source-manifest.md`.
2. One specifically relevant `catalog/**/overview.md` or `catalog/**/**-subpages.md` file aligned to the user’s product/question.
3. Additional `references/*.md` documents only when needed to close a specific gap.

For multi-product questions, repeat step 2 per product before loading broader references.

## Answer template constraints
- Start with: **Product + task scope + confidence**.
- Required sections:
  - **Retrieved facts** (directly supported by loaded files only).
  - **Recommended implementation** (explicitly marked inference/best practice).
  - **Risks / assumptions** (short and explicit).
- For procedural guidance, always include: **Prerequisites → Steps → Validation → Rollback**.
- Avoid generic recommendations when specific local source guidance is available.

## When to browse / verify live docs
Browse or verify live docs when:
- The question depends on recency (latest/current versions, limits, pricing, feature availability, release changes).
- The user requests authoritative confirmation from official documentation.
- The operation is high impact (security posture, routing/DNS/SSL, production migrations, API behavior affecting deploy/runtime).
- Local files are incomplete, ambiguous, or conflicting for the requested action.

When browsing, prioritize canonical sources listed in `references/99-source-manifest.md`.

## Max-context strategy
Keep context narrow by default:
- Load `references/99-source-manifest.md` first.
- Load one targeted `catalog/...` file second.
- Avoid loading by default:
  - all files under `catalog/` in one pass,
  - unrelated product directories,
  - all `references/*.md` simultaneously.
- Expand incrementally only when a concrete missing fact is identified.
