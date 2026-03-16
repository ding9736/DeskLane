# DeskLane Windows 发布说明

DeskLane 是一款面向远程桌面连接场景的桌面客户端，当前提供 Windows 正式安装版。

## 推荐安装方式

如果你是普通用户，推荐直接使用下面这条命令自动安装，无需手动下载任何安装包：

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -Command "irm https://github.com/ding9736/DeskLane/releases/latest/download/install.ps1 | iex"
```

适用环境：

- Windows PowerShell
- PowerShell 7
- CMD 中同样可直接执行上面的命令

## 安装包下载

如果你更习惯手动下载安装包，可使用以下文件：

- Windows 安装版：`DeskLane_window_setup.exe`
- Windows MSI：`DeskLane_window.msi`

下载地址：

- 安装版：https://github.com/ding9736/DeskLane/releases/latest/download/DeskLane_window_setup.exe
- MSI：https://github.com/ding9736/DeskLane/releases/latest/download/DeskLane_window.msi

## 适合谁使用

- 想快速连接和控制远程设备的普通用户
- 希望优先使用图形安装向导的桌面用户
- 需要 MSI 进行批量部署或静默安装的企业运维人员

## 当前发布内容

本次发布包含以下资产：

- `DeskLane_window_setup.exe`
- `DeskLane_window.msi`
- `release-manifest.yaml`
- `install.ps1`
- `install.sh`
- `README.md`

## 一键安装命令

PowerShell：

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -Command "irm https://github.com/ding9736/DeskLane/releases/latest/download/install.ps1 | iex"
```

CMD：

```cmd
powershell -NoProfile -ExecutionPolicy Bypass -Command "irm https://github.com/ding9736/DeskLane/releases/latest/download/install.ps1 | iex"
```

说明：

- 上述命令会自动读取最新发布清单
- 自动下载适用的 Windows 安装包
- 自动校验文件完整性
- 然后启动安装程序

## 安装前预览（可选）

如果你想先确认将要安装的版本和下载地址，而不立刻启动安装程序，可以先下载 `install.ps1` 再执行 `-DryRun`：

```powershell
Invoke-WebRequest -UseBasicParsing "https://github.com/ding9736/DeskLane/releases/latest/download/install.ps1" -OutFile .\install.ps1
.\install.ps1 -DryRun
```

这会输出：

- 将要使用的安装包文件名
- 对应的下载地址
- 对应的 `sha256` 校验值

## 安装完成后如何启动

安装完成后，推荐按下面任一方式启动：

- 双击桌面上的 `DeskLane 远程桌面` 快捷方式
- 在开始菜单中搜索 `DeskLane`
- 如果安装向导最后一页勾选了立即启动，可直接点击完成进入程序

## 已知说明

- Windows 当前推荐使用 `setup.exe`
- `MSI` 仍保留，便于运维部署
- Linux 与 macOS 的正式安装产物后续再发布

## GitHub 发布页

GitHub Releases：

https://github.com/ding9736/DeskLane/releases

