# Comparative Evaluation Plan

The project should demonstrate a bounded advantage with evidence, not with a feature checklist alone.

## Systems to compare

1. Single undifferentiated RAG baseline.
2. Top-1 plugin router + local RAG.
3. Proposed confidence-aware plugin router + local RAG + verifier.
4. Proposed router + deterministic workflow orchestrator + receipts.
5. Optional provider variants using the same contract (local, OpenViking, RAGFlow or R2R adapter).

## Dataset dimensions

The redacted golden set should include:

- clear single-domain queries;
- ambiguous domain queries;
- cross-domain queries requiring controlled multi-route retrieval;
- product/brand scope collision negatives;
- stale or conflicting evidence;
- missing material and missing layout cases;
- candidate publication and resume failures.

## Metrics

| Dimension | Metric | Desired interpretation |
|---|---|---|
| Routing | domain accuracy, top-k recall, abstention precision | wrong-domain selection decreases without hiding uncertainty |
| Isolation | cross-scope leakage rate | must be zero on negative authorization cases |
| Evidence | supported-claim rate, citation completeness, stale-source rate | claims are traceable and current enough for policy |
| Workflow | dependency violation rate, invalid transition rate | execution follows the plan |
| Reliability | duplicate-effect rate, compensation success, resume success | failures are bounded and recoverable |
| Operations | p95 latency, token cost, tool calls | quality gains are visible against cost |

Every result must identify the runtime, provider, dataset version, policy version and receipt IDs. A missing measurement is `PENDING`, not a zero.
