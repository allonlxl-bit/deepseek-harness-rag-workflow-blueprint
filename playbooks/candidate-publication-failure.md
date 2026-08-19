# Candidate Publication Failure

If a candidate post exists but the Live URL cannot be independently verified:

1. Mark `HOLD_LIVE_URL_UNVERIFIED`.
2. Do not report publication success.
3. Execute only the configured candidate compensation action.
4. Record post reference, verification result and compensation receipt.
5. Keep production untouched and request human review if cleanup is not provable.
