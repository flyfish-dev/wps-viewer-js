# Flyfish WPS Viewer 浏览器构建产物

本仓库发布 [wps.file-viewer.app](https://wps.file-viewer.app) 使用的浏览器构建产物，
用于评估 WPS/WPT、ET/ETT、DPS/DPT 文件的纯前端预览能力。

[公开接入 SDK](https://github.com/flyfish-dev/wps-viewer-integration) · [商业授权](https://dev.flyfish.group/shop/detail/1016)

仓库只包含压缩后的浏览器脚本、Worker、优化后的 WASM 授权模块、仅允许正式体验域名的许可证和完整性校验值。
解析与版式源码、签名材料、私有测试文档及客户许可证均不在本仓库中。

随仓库提供的评估许可证永久限定于 `https://wps.file-viewer.app`。仅把这些文件复制到其他域名既不产生部署授权，也无法通过运行时门禁。
生产环境自托管需要购买商业授权，并使用覆盖生产 Origin 的签名许可证。

```bash
shasum -a 256 -c SHA256SUMS
```

在线 Demo 用于兼容性评估。厂商私有、加密或历史二进制变体应以实际文件验收为准。
