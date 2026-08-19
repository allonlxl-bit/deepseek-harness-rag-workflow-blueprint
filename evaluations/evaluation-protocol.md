# Evaluation Protocol

Measure separately:

| Area | Example metric | Minimum evidence |
|---|---|---|
| Routing | correct workflow/site-pack selection | plan + expected case |
| Isolation | cross-scope leakage rate | negative cases + evidence refs |
| Retrieval | recall/precision/faithfulness | approved golden set |
| Workflow | dependency/order/state correctness | transition receipt |
| Safety | unauthorized effect rate | denied permission cases |
| Recovery | duplicate/compensation rate | replay and failure drills |

Never merge mock, deterministic unit, real candidate receipt and production capability into one score. Report unavailable evaluations as `PENDING` or `HOLD`.
