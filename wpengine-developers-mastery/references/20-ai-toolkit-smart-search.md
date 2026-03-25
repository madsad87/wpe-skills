# AI Toolkit — Smart Search / Find API Knowledge Base

## 1) Product mental model

Smart Search exposes a query interface for searching indexed content with relevance controls and advanced retrieval features.

At a high level:
- Content is indexed into searchable documents.
- Clients query using GraphQL.
- Response returns matching docs, scores, and selected fields.

## 2) Find API capability map

Key capability areas represented in docs:

- Full-text search over indexed fields
- Structured filtering (narrow by metadata constraints)
- Sorting and ranking control
- Relevance tuning (field weighting, tolerance)
- Time-aware scoring (decay functions)
- Query re-scoring and promoted documents
- Advanced retrieval modes
  - Semantic or hybrid search
  - Geographic constraints (where configured)
  - Facets / aggregations
- Response shaping
  - Include/exclude fields

## 3) Query design workflow

1. Define user intent class (keyword, semantic intent, filtered browse, geospatial).
2. Select query operator mix (text + filter + sort + boosts).
3. Apply ranking strategy:
   - Weight important fields higher.
   - Promote known-high-value documents.
   - Apply time decay when freshness matters.
4. Minimize payload with field inclusion.
5. Evaluate relevance and iterate.

## 4) Relevance tuning playbook

### Symptoms and fixes

- **Too many weak matches** → tighten tolerance / filters.
- **Important docs buried** → increase field weighting or promotions.
- **Old docs outranking recent content** → use time decay.
- **Good recall but poor precision** → combine semantic with strict filters.

## 5) Agent implementation pattern

For an AI agent that uses Smart Search:

- Build a retrieval adapter that maps user intent to query template.
- Keep templates by use case:
  - FAQ lookup
  - Content discovery with facets
  - Latest update search
  - Category-limited semantic search
- Log query + result metrics for tuning loop.

## 6) Safety and reliability notes

- Treat API beta notices seriously if present in docs.
- Implement graceful fallbacks when result sets are empty.
- Use deterministic filter clauses for policy-sensitive retrieval.
- Separate “exploration search” from “citation-grade search”.

## 7) Agent answer pattern

When responding with Smart Search derived content:

1. State search strategy used.
2. Provide top findings grouped by confidence.
3. Call out uncertainty or sparse-index cases.
4. Recommend next query refinement when confidence is low.

