# AI Toolkit — Smart Search Subpages Catalog

## Subpage cluster: Find API

### Knowledge contained

- GraphQL query interface for document retrieval.
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

- Content ingestion/index-update behavior.
- Schema and metadata strategy for filterable search.
- Re-index/rebuild considerations after model/content changes.
