# Strinova

Strinova is an extensible framework for Stravia. It provides a patched server that supports user-made plugins at the platform level. Currently, only the Linux x86-64 server version is supported.

## Scope and repository boundaries

This public repository is the clean build base and SDK surface for Strinova, anchored to upstream Stravia:

- Reference upstream: [StraviaPlatform](https://github.com/Stravia-AI/StraviaPlatform) (`v0.7.5`, commit `aa69767523da8010cbbbd306bded13f212ec52e2`)
- Upstream attribution: [UPSTREAM-ATTRIBUTION.md](UPSTREAM-ATTRIBUTION.md)
- Chinese overview: [README_CN.md](README_CN.md)

Private framework host patches and vendor overlays live in `MelodyAstro/Strinova` (`private`) and are applied only during CI builds using a read-only `STRINOVA_PRIVATE_TOKEN` secret.

## Platform plugin framework & installation

- SDK & runtime contract: [docs/strinova-sdk.md](docs/strinova-sdk.md)
  - `backend/crates/stravia-platform-plugin-sdk`
  - `backend/crates/stravia-platform-plugin-runtime`
- Component installation guide: [docs/inject-install.md](docs/inject-install.md)

## Public release contents

Public releases distribute only SDK crates, public platform-plugin WebAssembly components, and public inject/checksum metadata. Private vendor source code, vendor `.wasm` artifacts, and private patch bundles are not published to public release assets.
