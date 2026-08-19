# HTTP/API Contract (Illustrative)

These endpoints define the boundary between an ingress adapter and the workflow control plane. They are contracts, not a claim that a production server is already deployed.

| Method | Path | Input | Output | Safety rule |
|---|---|---|---|---|
| POST | `/v1/plans` | Query profile | Workflow plan | Must fail closed on missing scope or route |
| POST | `/v1/workflows` | Workflow plan + idempotency key | Session ID | Candidate mode only |
| POST | `/v1/workflows/{id}/resume` | Checkpoint + approved repair | Receipt projection | Must verify dependency state |
| GET | `/v1/workflows/{id}` | Session ID | Redacted status | Never returns prompt or secret |
| POST | `/v1/evidence` | Evidence record | Evidence ID | Hash and scope required |

All write-like actions require explicit environment mode. Public examples use `candidate`; `production` must be separately authorized and gated.
