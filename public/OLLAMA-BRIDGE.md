# Local Ollama Bridge Boundary

`ai-test-with-ollama` is a decoupled local testbed. It is used to validate local Ollama behavior, safe tool wrappers, run persistence, model inventory history, artifact audit UX, and packaging defaults.

NoveaCockpit remains the primary app. The bridge is not a runtime dependency.

## Accepted Defaults

- Prefer local models at or below 20B parameters for validation
- Prefer `qwen3:14b` for local tests
- Treat cloud or oversized models as unavailable for local validation
- Keep shell and broad HTTP tools disabled until review UI, allowlists, audit, and rollback behavior are proven

## Future Fusion

Fusion can happen only after:

- Contracts are compared
- Audit records are compatible
- Tool safety behavior is equivalent
- Packaging defaults are validated
- NoveaCockpit parity tests pass
