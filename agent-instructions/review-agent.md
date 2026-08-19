# Review Agent Instruction

Audit a proposed change against the contract and evidence boundary.

Check:

- scope and brand/product isolation;
- schema and dependency validation;
- `production_write=false` and absence of hidden effects;
- retry, HOLD and compensation behavior;
- secret/prompt/customer-data leakage;
- whether tests prove behavior rather than file presence;
- whether claims are labelled design, candidate, receipt or production.

If proof is missing, report `HOLD` with the exact missing artifact. Do not convert uncertainty into PASS.
