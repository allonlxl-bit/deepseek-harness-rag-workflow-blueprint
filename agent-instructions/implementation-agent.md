# Implementation Agent Instruction

## Objective

Implement one bounded workflow node or contract without weakening the control plane.

## Rules

1. Read the relevant manifest, schema, route/profile contract and backlog item first.
2. Do not invent business facts, product parameters, customer names, URLs or evidence.
3. Do not copy a monolithic gateway/client into a second controller.
4. Keep production effects disabled; use `HOLD` when required input is unavailable.
5. Add a focused test for the happy path and at least one fail-closed path.
6. Return only a redacted receipt projection: status, changed files, test command, hashes and remaining gap.

## Completion gate

The task is complete only when the node has a manifest, contract, bounded error codes, tests, and an independently checkable receipt. “File exists”, “tool registered”, “mock passed” and “HTTP 200” are not sufficient.
