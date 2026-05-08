# Public Publication Policy

## Decision

NoveaCockpit uses a private-source/public-mirror model.

Last updated: 2026-05-08. Latest validated public mirror baseline before this docs refresh: `b51566b`.

The implementation stays local or private. Public Git content is limited to sanitized product documentation, roadmap material, architecture summaries, and small non-sensitive interface examples.

The public mirror remote is public. Do not push the private source tree there.

## Public Allowlist

The public mirror may include:

- `public/**`
- `sample-gui/**`
- `docs/publication-policy.md`
- `License.md`
- Sanitized product overview, roadmap, architecture, and coordination notes
- Small examples that do not reveal proprietary runtime logic, credentials, operational defaults, or customer data
- Reviewed screenshots under `sample-gui/images/` after private paths, prompts, transcripts, logs, tokens tied to real sessions, and local runtime details are redacted

The public mirror must not include the live app implementation.

## Private-Only Denylist

The following stay local or private:

- `apps/**`
- `packages/**`
- `db/**`
- `tests/**`
- `finops/**`
- `infra/**`
- `scripts/**`
- `instructions/**`
- `.noveacockpit/**`
- `.ollama-agent-bridge/**`
- local databases, logs, reports, transcripts, model outputs, artifacts, lockfiles generated only for local tooling, keys, tokens, and environment files

## Publishing Flow

1. Export from the allowlist into a clean mirror folder or a dedicated public branch.
2. Run `git ls-files` or equivalent in the mirror and confirm every path is allowlisted.
3. Run a secret scan before any public push.
4. Push only the sanitized mirror.
5. Keep private development commits on a confirmed private remote.

Do not use `.gitignore` as the only protection. Already tracked files remain tracked until removed from the mirror index.

## Ollama Bridge Boundary

The local Ollama bridge remains a decoupled proving ground for local Ollama execution, safe tool wrappers, audit UX, model inventory history, and packaging defaults.

NoveaCockpit may copy reviewed patterns from that bridge later, but it must not depend on that project at runtime. Future fusion requires parity tests and an explicit acceptance milestone.
