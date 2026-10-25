# VRDesktopHUB Releases

- **最新版本 [Alpha146](https://github.com/limelisest/VRDesktopHUB-Releases/releases/tag/Alpha146) (2026-10-25)**：紧急修复手部工作区配置重置问题。详见 [Alpha146 更新说明](docs/ALPHA146.md) 与 [配置恢复与保存指南](docs/配置恢复与保存.md)。

VRDesktopHUB 的官方发行与扩展开发文档仓库，提供安装包、签名更新清单、更新说明和公开扩展开发手册，不包含应用实现源码。

请从 [Releases](https://github.com/limelisest/VRDesktopHUB-Releases/releases) 下载完整版本。首次安装请解压全量 ZIP，运行 VRDesktopHUB.Overlay.exe；需要 .NET 10 Windows Desktop Runtime（x64），VR 功能需要 SteamVR。

应用内「偏好设置 → 升级」可以检查新版本。在线更新按发布基底选择差分或全量包；本地导入仅接受官方签名全量 ZIP。

## 扩展开发

- [VRDesktopHUB Alpha146 扩展 SDK](https://github.com/limelisest/VRDesktopHUB-Releases/releases/download/Alpha146/VRDesktopHUB-Alpha146-ExtensionSDK.zip) | [SHA256 校验和](https://github.com/limelisest/VRDesktopHUB-Releases/releases/download/Alpha146/VRDesktopHUB-Alpha146-ExtensionSDK.zip.sha256) - 接口版本 API 1.12，宿主版本 Alpha146

从[扩展开发手册](docs/扩展开发手册.md)开始，当前文档对应 Alpha145、扩展 API1.12（含 1.11 能力），包含包结构、生命周期、UI、数据保存、宿主联动、独立后端及验收方法。

仓库中也保留[HTML 文件](docs/扩展开发手册.html)。Alpha145 不提供单独的手册附件，离线 HTML 与 Markdown 手册随上方 SDK 完整内附。
