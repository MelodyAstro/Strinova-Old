# Public Strinova SDK

Strinova extends Stravia with a sandboxed WebAssembly platform-plugin runtime
using the WIT interface `stravia:platform-plugin@1.0.0`.

Use the public crates under `backend/crates/stravia-platform-plugin-sdk` and
`backend/crates/stravia-platform-plugin-runtime` from the matching release. Keep
plugin IDs, schema versions, and exported capability names stable across upgrades.

Platform plugins execute within bounded fuel, memory, and timeout budgets inside
the gateway and do not receive direct network, filesystem, database, or vendor
credential access. Private host/vendor overlays are applied only in CI from the
private patch repository (`MelodyAstro/Strinova`).
