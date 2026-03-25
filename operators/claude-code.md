# Claude Code Operator Guide

## Recommended prompt preamble
Use this preamble at the top of each task:

```text
You are operating inside the wpengine-developers-mastery corpus.
Prioritize exact retrieval from local markdown files before answering.
Distinguish clearly between (1) directly retrieved facts and (2) inferred guidance.
Cite file paths used for every non-trivial claim.
If a claim can be stale or high-risk, verify live docs before finalizing.
```

## Retrieval order (strict)
1. `references/99-source-manifest.md` (discover canonical source URLs and document map).
2. The single most relevant `catalog/**/overview.md` or `catalog/**/**-subpages.md` file for the requested product/topic.
3. Supporting `references/*.md` files only as needed to fill gaps or confirm constraints.

If multiple products are involved, repeat step 2 per product before broad reference loading.

## Answer template constraints
- Open with: **Product + scope + confidence**.
- Split sections:
  - **Retrieved facts** (only what is directly supported by loaded files).
  - **Recommended approach** (explicitly marked as inference/best practice).
- For any procedure, include: **Prerequisites → Steps → Validation → Rollback**.
- Keep responses implementation-ready and avoid vague “check docs” phrasing; point to exact local files first.

## When to browse / verify live docs
Browse or verify live docs when:
- The user asks for “latest”, “current”, “recent”, pricing, limits, versions, release behavior, or availability.
- The action is production-impacting (migrations, routing, DNS/SSL, security settings, API behavior relied on for deploys).
- Local files conflict, appear incomplete, or omit a required operational detail.

When browsing, prefer canonical URLs listed in `references/99-source-manifest.md`.

## Max-context strategy
Default to minimal loading:
- **Always load first:** `references/99-source-manifest.md`.
- **Then load one targeted catalog file** for the active product/topic.
- **Avoid loading by default:** entire `catalog/` tree, unrelated product folders, and all `references/*.md` files at once.
- Expand context incrementally only when a concrete unanswered question remains.
