# Plugin-Indexed RAG Harness

Architecture blueprint for multi-brand, multi-product, multilingual and multichannel content systems.

The central proposal is to treat enterprise capabilities as an addressable plugin index graph over a replaceable Agent Harness runtime, with hierarchical retrieval, evidence contracts, policy verification and auditable execution.

## Status

This repository is an early public research draft. It is not a production deployment, vendor performance guarantee, or security certification. Examples are illustrative and must be adapted and independently verified. Business names and internal identifiers have been replaced with neutral placeholders.

## Contents

- [`docs/deep-research-report.md`](docs/deep-research-report.md) — complete architecture and implementation research draft
- The report includes an implementation-grounded revision covering registry/index, deterministic workflow orchestration, site packs, evidence receipts, candidate-only publication and fail-closed acceptance.
- [`architecture/`](architecture/) — Mermaid system and lifecycle diagrams
- [`schemas/`](schemas/) — JSON Schemas for manifests, plans and evidence
- [`interfaces/`](interfaces/) — plugin and HTTP/API contracts
- [`agent-instructions/`](agent-instructions/) — implementation and review instructions
- [`backlog/`](backlog/) — phased implementation backlog
- [`evaluations/`](evaluations/) — golden-set and evaluation protocol templates
- [`playbooks/`](playbooks/) — routing, retrieval and candidate-publication failure procedures
- [`examples/`](examples/) — neutral manifests and workflow examples
- `docs/` — future topic-specific documents
- `schemas/` — future contract and manifest schemas
- `examples/` — future generic examples

## Reading path

1. Start with the executive summary in the research report.
2. Review the plugin index, routing, evidence and verifier contracts.
3. Treat deployment, cost and vendor-specific claims as configuration-dependent.
4. Do not place secrets, customer data, private URLs or internal business records in this repository.

## Contributing

Issues and pull requests are welcome for corrections, clearer contracts, implementation examples and reproducible evaluations. Please do not submit confidential data or credentials.

## License

MIT. See [`LICENSE`](LICENSE).
