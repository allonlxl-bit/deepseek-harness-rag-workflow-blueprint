# Implementation Backlog

## P0 — control plane

- [ ] Implement manifest validation and immutable registry lifecycle.
- [ ] Implement deterministic Task Index Router with brand/task/product scope checks.
- [ ] Implement typed DAG compiler and bounded executor.
- [ ] Add redacted session, audit and workflow receipt projections.

## P1 — standard workflows

- [ ] Define `technical_solution_workflow`.
- [ ] Define `blog_workflow`.
- [ ] Define `product_detail_workflow`.
- [ ] Add route, material, traffic, media, layout, renderer and verifier node contracts.
- [ ] Add candidate publication and Live URL acceptance adapter.

## P2 — knowledge and safety

- [ ] Add evidence ledger with SHA-256 and scope validation.
- [ ] Add policy checks for unsupported claims, cross-brand retrieval and unsafe permissions.
- [ ] Add retry budget, checkpoint resume and candidate compensation.
- [ ] Add dependency and secret scanning to CI.

## P3 — evaluation and operations

- [ ] Populate the golden dataset from approved, redacted examples.
- [ ] Run routing, retrieval, evidence, isolation and workflow-state evaluations.
- [ ] Add failure drills from `playbooks/`.
- [ ] Establish release gates for candidate receipt and production authorization.
