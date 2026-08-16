# scoop-tubatools

**图吧工具箱 WinUI3** 的 [Scoop](https://scoop.sh) 安装源（bucket）。

图吧工具箱 WinUI3（TubaWinUi3）是一款免费、开源的硬件检测与系统维护工具箱，内置 CPU-Z、GPU-Z、AIDA64、CrystalDiskMark 等大量便携版检测工具，支持实时硬件监控与 FPS 悬浮窗。官方网站：<https://tubawinui3.cn>

---

## 安装

本 bucket 提供 **便携版**（含全部检测工具），scoop 会根据系统架构自动选择 x64 或 arm64 版本。

```powershell
# 1. 添加本 bucket
scoop bucket add tubatools https://github.com/luolangaga/scoop-tubatools

# 2. 安装
scoop install tubatools/tubatool
```

## 使用

| 操作 | 命令 |
|------|------|
| 启动软件 | 开始菜单 **图吧工具箱WinUI3**，或命令行输入 `tubatool` |
| 更新到最新版 | `scoop update tubatool` |
| 更新所有软件 | `scoop update *` |
| 卸载 | `scoop uninstall tubatool` |
| 移除本 bucket | `scoop bucket rm tubatools` |

## 说明

- **管理员权限**：软件运行硬件检测/驱动功能需要管理员权限，启动时会自动触发 UAC 提权，属正常现象。
- **系统要求**：需要 Windows 10 及以上；便携包内附兼容版，旧系统会自动回退到兼容版程序。
- **数据目录**：便携版数据默认保存在 `%LocalAppData%\TubaWinUi3\`（设置、收藏、启动历史等）。`scoop uninstall` 不会删除该目录，如需彻底清除请卸载后手动删除。
- **首次安装哈希**：首次安装时 Scoop 会自动下载并计算文件校验值（本地网络较差时无需手动核对）；后续每次发布新版，本仓库的 GitHub Actions（Excavator）会自动更新清单的版本号、下载地址与 SHA256。
## 清单结构

- `bucket/tubatool.json` —— scoop manifest（含 `checkver` / `autoupdate`）
- 更新由 `.github/workflows/excavator.yml` 自动执行

## 官方信息

| 项目 | 地址 |
|------|------|
| 官方网站 | <https://tubawinui3.cn> |
| 官方下载页 | <https://tubawinui3.cn/download> |
| 源码仓库 | <https://github.com/luolangaga/tubatools> |