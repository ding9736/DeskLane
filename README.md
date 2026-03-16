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

## 手动下载安装

- Windows 安装版：
  `https://github.com/ding9736/DeskLane/releases/latest/download/DeskLane_window_setup.exe`
- Windows MSI：
  `https://github.com/ding9736/DeskLane/releases/latest/download/DeskLane_window.msi`

## Release 页面

查看最新发布：

`https://github.com/ding9736/DeskLane/releases`
