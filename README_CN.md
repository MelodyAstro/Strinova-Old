# Strinova

Strinova 是基于 Stravia 的可扩展框架，提供支持用户自定义平台级插件的补丁服务端。当前仅支持 Linux x86-64 Server 版本。

## 定位与公开边界

本公开仓库作为 Strinova 的清理后构建基线与插件 SDK 入口，对应上游 Stravia 版本：

- 上游参考：[StraviaPlatform](https://github.com/Stravia-AI/StraviaPlatform)（`v0.7.6`，commit `b9e0171453dc30f46b1febc0657fe409e08b625c`）
- 上游归属说明：[UPSTREAM-ATTRIBUTION.md](UPSTREAM-ATTRIBUTION.md)
- English documentation: [README.md](README.md)

私有宿主框架 patch 与供应商适配维护在私有仓库 `MelodyAstro/Strinova`，仅在 GitHub Actions CI 中通过只读的 `STRINOVA_PRIVATE_TOKEN` secret 应用。

## 平台插件开发与安装

- 插件 SDK 与运行时契约：[docs/strinova-sdk.md](docs/strinova-sdk.md)
  - `backend/crates/stravia-platform-plugin-sdk`
  - `backend/crates/stravia-platform-plugin-runtime`
- 组件安装说明：[docs/inject-install.md](docs/inject-install.md)

## 公开 Release 内容

公开 release 仅发布 SDK、可公开的平台插件 WebAssembly 组件及公开 inject/校验元数据；供应商源码、供应商 `.wasm` 成品与私有 patch 包不进入公开分发资产。
