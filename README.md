# 桌面图标台球

一款 Windows 桌面小游戏：台球落在桌面图标之间，用鼠标拖住母球瞄准、松手击球，按清台数与用时结算成绩。

## 特性

- 单文件、免安装，双击即玩（Windows 10 / 11 x64）
- 击球、停位、清台结算，自动计时与记分
- 辅助线开关、台面开关、随时重新开局
- 深空墨蓝 + 香槟金配色；完全离线运行，不联网、不上传任何数据

## 下载

在 [Releases](../../releases) 里下载 `DesktopIconBilliards-0.3.0-win-x64.exe`（约 20 MB）。

首次运行若被 Windows SmartScreen 拦下，点「更多信息」→「仍要运行」即可。

## 自己打包

解压源码包后进入目录，执行：

```powershell
pwsh -File build_local.ps1
```

首次会自动创建 `.venv` 并安装依赖（需要联网），产物在 `dist\` 下。
环境要求：Windows + Python 3.11+（`python` 在 PATH 里）。

若打包时报「缺少 Tcl/Tk」，把 Releases 里的 `tcl_runtime.zip` 解压到工程根目录后再跑一次。
脚本打包完成后会自检 EXE 里是否真的带上 Tcl 数据，不会产出运行即闪退的坏包。

## 许可

MIT，详见 [LICENSE](LICENSE)。
