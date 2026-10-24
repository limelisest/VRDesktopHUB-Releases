# VRDesktopHUB Releases

VRDesktopHUB 的官方发行与扩展开发文档仓库，提供安装包、签名更新清单、更新说明和公开扩展开发手册，不包含应用实现源码。

请从 [Releases](https://github.com/limelisest/VRDesktopHUB-Releases/releases) 下载完整版本。首次安装请解压全量 ZIP，运行 VRDesktopHUB.Overlay.exe；需要 .NET 10 Windows Desktop Runtime（x64），VR 功能需要 SteamVR。

应用内「偏好设置 → 升级」可以检查新版本。在线更新按发布基底选择差分或全量包；本地导入仅接受官方签名全量 ZIP。

## 扩展开发

下载 [Alpha145 完整扩展 SDK](https://github.com/limelisest/VRDesktopHUB-Releases/releases/download/Alpha145/VRDesktopHUB-Alpha145-ExtensionSDK.zip)（[SHA256](https://github.com/limelisest/VRDesktopHUB-Releases/releases/download/Alpha145/VRDesktopHUB-Alpha145-ExtensionSDK.zip.sha256)），解压后从包内 `README.md` 开始。需要 Windows x64 和 .NET 10 SDK；内含项目生成器、公开契约、编译/校验/打包工具、独立工作器、三个高级示例以及离线 HTML 与 Markdown 手册，无需主程序源码。已验证项目生成、移动 SDK 后编译、打包及发行真实独立工作器。

从[扩展开发手册](docs/扩展开发手册.md)开始，当前文档对应 Alpha145、扩展 API1.12（含 1.11 能力），包含包结构、生命周期、UI、数据保存、宿主联动、独立后端及验收方法。

仓库中也保留[HTML 文件](docs/扩展开发手册.html)。Alpha145 不提供单独的手册附件，离线 HTML 与 Markdown 手册随上方 SDK 完整内附。
