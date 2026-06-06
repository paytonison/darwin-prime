# Darwin Prime Scope

Darwin Prime is a research environment for studying and extending the open
Darwin/XNU substrate.

## Non-goals

- It is not a macOS clone.
- It is not a desktop skin.
- It does not vendor SDKs, KDKs, private Apple files, or generated build output.
- It does not rewrite XNU source casually.

## Working Model

The `darwin-prime` repository holds coordination material: documentation,
manifests, scripts, experiments, notes, and patch staging. The
`darwin-prime-xnu` repository remains an upstream-tracked XNU fork.

Prefer small, auditable changes:

1. Document the intent here.
2. Prototype outside upstream source where possible.
3. Keep XNU patches isolated under `patches/xnu/`.
4. Apply source changes only on purpose-built branches in `darwin-prime-xnu`.
