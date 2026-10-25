# VRDesktopHUB Alpha146 更新说明

发布日期：2026-10-25

## 问题与修复
在 Alpha144 与 Alpha145 中，手部绑定或移动工作区并重启后可能导致项目配置重置。本次更新移除了工作区中未使用的普通窗口尺寸元数据，并优化了保存机制：新配置写入前经过隔离校验与临时文件原子替换，校验失败会保留原有项目；当配置与备份均损坏时，系统会停止 VR 初始化、重试与配置写入，但 Windows 恢复面板依然可用，且仅在无保存数据的全新首次运行时才会创建默认配置。

## 受影响用户恢复步骤
1. 安装并更新至 Alpha146。
2. 打开 Windows 主窗口，进入“偏好设置” → “配置与存储”。VR 未启动或离线时面板依然可用。
3. 在备份列表中根据记录时间、工作区名称以及屏幕与窗口数量，选取重置前的恢复点。不可读记录已自动禁用。
4. 点击“恢复备份”，核对快照信息后点击“确认恢复”。首次点击不修改配置；若需放弃可点击“取消恢复”。

详细机制与边界说明见 [配置恢复与保存指南](配置恢复与保存.md)。若本地未留存任何有效副本，系统无法保证找回数据。

## 下载与升级
- 版本发布页：[GitHub Release](https://github.com/limelisest/VRDesktopHUB-Releases/releases/tag/Alpha146)
- 扩展 SDK 下载：[VRDesktopHUB-Alpha146-ExtensionSDK.zip](https://github.com/limelisest/VRDesktopHUB-Releases/releases/download/Alpha146/VRDesktopHUB-Alpha146-ExtensionSDK.zip) | [SHA256 校验和](https://github.com/limelisest/VRDesktopHUB-Releases/releases/download/Alpha146/VRDesktopHUB-Alpha146-ExtensionSDK.zip.sha256)
- 升级说明：匹配 Alpha145 哈希可使用增量包升级，不匹配或其它版本请使用完整包。手动导入仅支持带签名的完整包。升级保留用户数据、MOD 业务数据、runtime-dev 与 SteamVR 开发入口。未捆绑 VRC Toolbox。SDK 保持 API1.12，宿主版本变更为 Alpha146。

## 验证边界
自动化测试覆盖离线 Runtime、真实独立 Worker 与 Owner IPC、原生 WPF 及混淆可执行文件，并通过了真实故障配置隔离副本在独立进程中的工作区与 4 个捕获窗口重开验证。测试未进行 SteamVR 启停与连接、物理头显实测及在线 VRChat 实测。
