# Inject and platform plugin installation

Public releases publish the platform plugin SDK crates, public platform-plugin
Wasm component packages (`policy-tools`, `model-mapping`), and public host
inject/checksum metadata (`SHA256SUMS`, `build-manifest.json`).

Install platform-plugin components through the patched server's Platform Plugins
management API or WebUI, verify the component digest against `SHA256SUMS`, and
enable them for the intended scope.

Private server binaries and vendor components are built and retained privately in
protected CI / private distribution channels and are not included in public
release assets. Never copy vendor source or deployment credentials into a
public checkout.
