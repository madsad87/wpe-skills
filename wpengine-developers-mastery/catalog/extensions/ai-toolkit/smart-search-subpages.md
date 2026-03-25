# AI Toolkit — Smart Search Subpages Catalog

## Subpage cluster: Find API

### Knowledge contained

- GraphQL query interface for document retrieval. [source:smart-search-find-api]
- Query operators for text matching, filters, ranking, and response shaping.
- Advanced retrieval options (semantic/hybrid modes where enabled).

### Tuning primitives

- Field weights
- Promotions/re-scoring
- Time decay
- Facets/aggregations
- Include/exclude field projection

### Agent troubleshooting map

- Low precision → tighten filters + exact field weighting.
- Low recall → broaden matching + semantic branch.
- Slow query → reduce payload/facets and narrow scope.

## Subpage cluster: Smart Search Settings / Indexing (expected area)

### Knowledge contained

- Content ingestion/index-update behavior. [source:ai-toolkit-overview]
- Schema and metadata strategy for filterable search.
- Re-index/rebuild considerations after model/content changes.

## Source Links

- [source:smart-search-find-api] https://developers.wpengine.com/docs/wp-engine-ai-toolkit/smart-search/find-api/ — Retrieved: 2026-03-25 (UTC) — Title: Smart Search Find API docs
- [source:ai-toolkit-overview] https://developers.wpengine.com/docs/wp-engine-ai-toolkit/ — Retrieved: 2026-03-25 (UTC) — Title: WP Engine AI Toolkit docs overview
