# Related Work and Positioning

This project does not claim to invent a new retrieval algorithm or to be the first DeepSeek Harness plus RAG integration. Its contribution is a control-plane reference architecture that composes existing runtime, memory, retrieval and evaluation capabilities into a governed multi-domain workflow.

## Public building blocks

| Project / line of work | What it provides | Where this blueprint uses it | Boundary that remains |
|---|---|---|---|
| [DeepSeek Harness](https://github.com/deepseek-ai/deepseek-harness) | Plugin runtime, Cordis composition, Agent Loop, sessions and tools | Runtime substrate and lifecycle seam | Does not by itself define enterprise knowledge-domain governance |
| [Harness examples](https://github.com/deepseek-ai/deepseek-harness/tree/master/examples) | Runnable demonstrations such as memory, headless and JSON-RPC agents | Extension-point references | Not a multi-brand evidence-governed RAG workflow |
| [MemOS](https://github.com/MemTensor/MemOS) | Long-term memory, hybrid retrieval, cross-task experience and Harness integration | User/session/agent memory candidate | Memory is not automatically authoritative product or brand knowledge |
| [OpenViking](https://github.com/volcengine/OpenViking) | Hierarchical context/resource organization and path-aware retrieval | Candidate hierarchical context provider | Does not by itself supply enterprise claims, policy and publication governance |
| [DSH plugin catalogue](https://github.com/awesome-dsh-plugin/awesome-dsh-plugin) | Community discovery of Harness plugins | Ecosystem inventory and integration candidates | A catalogue is not a registry with scope, policy and workflow guarantees |
| [RAGFlow](https://github.com/infiniflow/ragflow) | Document parsing, retrieval, reranking and agentic workflow features | Optional retrieval backend adapter | Backend retrieval does not decide enterprise task routing or approval |
| [R2R](https://github.com/SciPhi-AI/R2R) | Retrieval API, hybrid search, graph and agentic RAG capabilities | Optional RetrievalProvider adapter | Provider capability is not the complete control plane |
| [Modular RAG](https://arxiv.org/abs/2407.21059) | Modular routing, scheduling, fusion and execution patterns | Theory for composable retrieval | Does not define this Harness-specific enterprise contract |
| [RealRoute](https://arxiv.org/abs/2604.20860) | Retrieve-then-verify and dynamic multi-source routing | Evidence-aware routing fallback | This blueprint adapts the idea to plugin scopes and workflow gates |
| [RAGRouter](https://arxiv.org/abs/2505.23052) | Learned routing, thresholds and quality/latency/cost trade-offs | Future routing scorer/evaluation baseline | A scorer alone does not provide scope isolation or receipts |

The comparison is based on public project descriptions and is intentionally conservative. “Not covered” means not identified in the reviewed public material, not proof that a private fork or undocumented implementation does not exist.

## The proposed composition

```text
DeepSeek Harness / Cordis
  runtime, plugin lifecycle, tools, sessions, agent loop
        ↓
Plugin Registry + Task Index Router
  domain, brand, product, task, permission and dependency selection
        ↓
Workflow Orchestrator
  typed DAG, bounded retry, checkpoint, resume and compensation
        ↓
RetrievalProvider adapter
  OpenViking / RAGFlow / R2R / local hybrid retrieval
        ↓
Evidence Contract + Verifier
  source, version, scope, hash, claim support and policy checks
        ↓
Candidate task execution + audit receipt
```

MemOS, where used, belongs beside the authoritative knowledge plane for user preferences, session history and agent experience. It should not silently replace the evidence ledger for product claims, regulatory facts or brand rules.

## Why the proposal can be stronger

The claim is not “better retrieval on every dataset.” The testable claim is narrower:

> For multi-domain enterprise tasks, a system that separates global plugin routing, local retrieval, evidence verification and deterministic workflow execution should reduce scope errors and make failures more diagnosable than a single undifferentiated RAG or an unconstrained agent loop.

The differentiators to test are:

1. addressable plugin/domain index instead of domain × task plugin multiplication;
2. namespace and permission isolation across brands, products and markets;
3. confidence-aware single-route, multi-route and broad-retrieval fallback;
4. evidence contracts before business execution;
5. deterministic workflow boundaries around agentic steps;
6. redacted, replayable receipts and explicit `HOLD`/compensation states;
7. implementation and failure playbooks that connect architecture to delivery work.

## Routing correction: do not force Top-1

The router should emit candidates and confidence, not always one winner:

```text
high confidence
  → one plugin/domain

medium confidence
  → top-2/top-3 scoped retrieval
  → evidence comparison
  → verifier selects or holds

low confidence or conflicting evidence
  → retrieve domain summaries
  → query rewrite / clarification
  → HOLD if scope remains unresolved
```

This keeps “plugin as index entry” while avoiding the failure mode where an early classifier silently sends a query to the wrong knowledge domain.

## License and adoption notes

External projects remain external dependencies. Before adopting one, review its license, version stability, data residency, network behavior and extension contract. This repository provides adapters and evaluation criteria conceptually; it does not repackage third-party code or claim compatibility without a tested receipt.
