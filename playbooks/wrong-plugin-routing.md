# Wrong Plugin Routing

Symptoms: wrong Site Pack, missing route, or cross-domain material selected.

1. Freeze the workflow; do not continue to renderer or publication.
2. Inspect the redacted Query Profile, registry version and route hash.
3. Re-run deterministic scope and dependency validation.
4. If the correct route cannot be proven, record `HOLD_ROUTE_SCOPE_UNVERIFIED`.
5. Add the case to the golden dataset before changing routing rules.
