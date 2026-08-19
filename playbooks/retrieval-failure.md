# Retrieval Failure

1. Preserve the query, filters, index alias and evidence references.
2. Distinguish no result, stale source, scope mismatch and conflict.
3. Do not fill the gap with model memory or another brand's source.
4. Retry only within the workflow budget; otherwise emit `HOLD_EVIDENCE_INSUFFICIENT`.
5. Record the missing source as a backlog item.
