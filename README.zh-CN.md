# Flyfish WPS Viewer 浏览器构建产物

本仓库发布 [wps.file-viewer.app](https://wps.file-viewer.app) 使用的浏览器构建产物，
用于评估 WPS/WPT、ET/ETT、DPS/DPT 文件的纯前端预览能力。

产品首页与预览器使用独立入口。首页通过同源 iframe 嵌入单独维护的
[`/demo`](https://wps.file-viewer.app/demo) 预览页。

[公开接入 SDK](https://github.com/flyfish-dev/wps-viewer-integration) · [商业授权](https://dev.flyfish.group/shop/detail/1016)

## 当前版本

**0.4.5 / 2026-10-23**：同步最新已提交 Office 组件，落实到 WPS 预览链路。
DOC 减少重复渲染，采用协作排版和后台字体批量校准；现代文字包保留原始 File，
交给 Worker/Canvas 按需读取。兼容表格使用独立 Worker 和窗口化虚拟滚动，
现代演示按需加载幻灯片，使用有界缩略图和独立导航。

表格与现代演示引擎按需加载，Demo 主入口 gzip 体积较 0.4.4 约减少 32%。
切换文件取消旧任务，导航不再误计后台候选页，桌面与移动视口已验证。
这些是性能与生命周期改进，不代表所有私有变体均已达到原生版式一致。

两个 HTML 入口均通过 `application-version` 元信息标识版本。
校验值对应实际部署的浏览器产物。

## 授权版本更新

新增[旗舰版](https://dev.flyfish.group/shop/detail/1016?sku=56)，定价 **¥5,999**，
不限域名、项目和部署数量，提供永久商用运行授权与首年更新维护。
商业版和企业版继续提供；本仓库的评估许可证保持原有域名限制。

仓库只包含压缩后的浏览器脚本、Worker、优化后的 WASM 授权模块、仅允许正式体验域名的许可证和完整性校验值。
解析与版式源码、签名材料、私有测试文档及客户许可证均不在本仓库中。

随仓库提供的评估许可证永久限定于 `https://wps.file-viewer.app`。仅把这些文件复制到其他域名既不产生部署授权，也无法通过运行时门禁。
生产环境自托管需要购买商业授权，并使用覆盖生产 Origin 的签名许可证。

```bash
shasum -a 256 -c SHA256SUMS
```

在线 Demo 用于兼容性评估。厂商私有、加密或历史二进制变体应以实际文件验收为准。
