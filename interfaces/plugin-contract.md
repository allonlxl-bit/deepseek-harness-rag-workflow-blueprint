# Plugin Contract

Every executable capability is a typed workflow node and must expose:

- `manifest`: immutable identity, version, scope, permissions and dependencies;
- `apply(ctx)`: registers services, tools or events and returns a disposer;
- input/output schema and pre/postconditions;
- bounded retry policy and explicit `HOLD_*` codes;
- candidate effect boundary (`production_write=false` in this public blueprint);
- safe receipt projection containing IDs, hashes, status and artifact references, never secrets or full prompts.

The Task Index Router selects nodes. The Workflow Orchestrator executes them. The Agent Loop may reason inside a node or choose a bounded repair, but it may not bypass the plan, policy or verifier.

## Required node result

```json
{
  "status": "PASS_NODE",
  "node_id": "material_read",
  "production_write": false,
  "artifacts": [{"kind": "manifest", "ref": "sha256:..."}],
  "next_actions": []
}
```

Allowed terminal states are `PASS_NODE`, `HOLD`, `RETRYABLE_FAILED` and `COMPENSATED`.
