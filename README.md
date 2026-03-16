# DeskLane Windows 发布说明

<div align="center">

**下一代跨平台远程桌面解决方案**

**极速 · 安全 · 智能**

</div>

---

DeskLane 是一款远程桌面软件，帮助你随时随地连接和控制其他电脑。无论是远程办公、技术支持，还是设备管理，都能让你像操作本地电脑一样流畅地操作远程设备。

---

## 🔥 关键问题

| 问题 | 答案 |
| --- | --- |
| **DeskLane 是做什么的？** | 远程桌面控制 — 在一台电脑上操作另一台电脑 |
| **是直连还是中转？** | **点对点直连优先，中转仅作回退** — 主打直连，极致低延迟 |
| **用什么协议？** | **自研直连传输协议** — 针对远程桌面场景深度优化 |

---

## 💎 核心技术优势

### 自研直连传输协议

DeskLane 采用自研的 **Direct Transport** 传输技术栈，专为远程桌面场景深度优化：

| 特性 | 说明 |
| --- | --- |
| 🚀 **极致低延迟** | 直连优先，避开服务器中转，响应速度大幅提升 |
| 📡 **智能路径选择** | 自动探测最佳传输路径，根据网络环境动态调整 |
| 🔄 **自适应优化** | 针对丢包、抖动等网络状况自动优化传输策略 |
| 🔒 **端到端加密** | 直连传输全程加密，无需担心中间人攻击 |

### 安全第一

- **设备身份认证** — 基于长期公钥，确保每次连接都是可信设备
- **端到端加密** — 传输数据全程加密，隐私安全有保障
- **持续身份验证** — 首次配对后持续验证，防止会话劫持
- **完整审计日志** — 所有连接事件可追溯

---

## ✨ 产品特色

| 特性 | 说明 |
| --- | --- |
| ⚡ **开箱即用** | 无需复杂配置，安装即连接 |
| 🌐 **跨平台** | Windows / macOS / Linux 全平台支持 |
| 📊 **实时监控** | 连接状态、网络质量、帧率一目了然 |
| 🔌 **智能回退** | 直连失败时自动切换中转模式，确保连接稳定 |

---

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
