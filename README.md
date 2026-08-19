# DeepSeek Harness RAG Workflow Blueprint

Research paper and engineering blueprint for plugin-indexed, workflow-oriented RAG systems built around DeepSeek Harness.

The central proposal is to treat enterprise capabilities as an addressable plugin index graph over a replaceable Agent Harness runtime, with hierarchical retrieval, evidence contracts, policy verification and auditable execution.

This repository is primarily for reading, design reference and adaptation. It is not a turnkey production system or a drop-in plugin collection. Developers should adapt the concepts, contracts and examples to their own runtime, data boundaries, policies and deployment environment.

## Status

This repository is an early public research draft. It is not a production deployment, vendor performance guarantee, security certification or complete runnable implementation. Examples are illustrative and must be adapted and independently verified. Business names and internal identifiers have been replaced with neutral placeholders.

## Contents

- [`docs/deep-research-report.md`](docs/deep-research-report.md) — complete architecture and implementation research draft
- The report includes an implementation-grounded revision covering registry/index, deterministic workflow orchestration, site packs, evidence receipts, candidate-only publication and fail-closed acceptance.
- [`architecture/`](architecture/) — Mermaid system and lifecycle diagrams
- [`schemas/`](schemas/) — JSON Schemas for manifests, plans and evidence
- [`interfaces/`](interfaces/) — plugin and HTTP/API contracts
- [`agent-instructions/`](agent-instructions/) — implementation and review instructions
- [`backlog/`](backlog/) — future reference-implementation roadmap
- [`evaluations/`](evaluations/) — golden-set and evaluation protocol templates
- [`playbooks/`](playbooks/) — routing, retrieval and candidate-publication failure procedures
- [`examples/`](examples/) — neutral manifests and workflow examples
- `docs/` — future topic-specific documents
- `schemas/` — future contract and manifest schemas
- `examples/` — future generic examples

## How developers can use this repository

1. Read the executive summary and architecture sections.
2. Use the diagrams to understand the control-plane and workflow boundaries.
3. Reuse or adapt the schemas, interface contracts, evaluation templates and failure playbooks.
4. Implement the concepts in your own Harness, agent framework or service runtime.
5. Treat deployment, cost and vendor-specific claims as configuration-dependent.
6. Do not place secrets, customer data, private URLs or internal business records in this repository.

## Contributing

Issues and pull requests are welcome for corrections, clearer contracts, implementation examples and reproducible evaluations. Please do not submit confidential data or credentials.

## License

MIT. See [`LICENSE`](LICENSE).
