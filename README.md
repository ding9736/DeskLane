# DeskLane 二进制发布仓

这个仓库只用于发布 DeskLane 的二进制安装包，不托管 DeskLane 源代码。

## 普通用户推荐安装方式

如果你在 Windows 上使用 DeskLane，推荐直接执行下面这条命令自动安装，无需手动下载安装包：

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -Command "irm https://github.com/ding9736/DeskLane/releases/latest/download/install.ps1 | iex"
```

CMD 也可以直接执行同一条命令：

```cmd
powershell -NoProfile -ExecutionPolicy Bypass -Command "irm https://github.com/ding9736/DeskLane/releases/latest/download/install.ps1 | iex"
```

这条命令会自动：

- 读取最新 `release-manifest.yaml`
- 下载对应的 Windows 安装包
- 校验 `sha256`
- 启动安装程序

## 安装前预览（可选）

如果你想先确认将要安装的版本、下载地址和校验值，而不立刻启动安装程序，可以执行：

```powershell
Invoke-WebRequest -UseBasicParsing "https://github.com/ding9736/DeskLane/releases/latest/download/install.ps1" -OutFile .\install.ps1
.\install.ps1 -DryRun
```

## 手动下载安装

- Windows 安装版：
  `https://github.com/ding9736/DeskLane/releases/latest/download/DeskLane_window_setup.exe`
- Windows MSI：
  `https://github.com/ding9736/DeskLane/releases/latest/download/DeskLane_window.msi`

## 当前发布资产

- `DeskLane_window_setup.exe`
- `DeskLane_window.msi`
- `release-manifest.yaml`
- `install.ps1`
- `install.sh`
- `README.md`

## Release 页面

查看最新发布：

`https://github.com/ding9736/DeskLane/releases`
