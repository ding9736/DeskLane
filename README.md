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

### 自动安装（推荐）

复制以下命令到 PowerShell 中执行，即可自动下载并安装：

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -Command "irm https://github.com/ding9736/DeskLane/releases/latest/download/install.ps1 | iex"
```

### 安装步骤

| 步骤 | 操作 | 说明 |
| --- | --- | --- |
| **1** | 打开 PowerShell | 按 `Win` 键，输入 `PowerShell`，右键选择「以管理员身份运行」 |
| **2** | 复制命令 | 选中上方代码块中的命令，按 `Ctrl + C` |
| **3** | 粘贴执行 | 在 PowerShell 窗口中右键点击（自动粘贴），按 `Enter` |
| **4** | 等待完成 | 脚本会自动下载、校验并启动安装程序 |
| **5** | 启动程序 | 双击桌面「DeskLane 远程桌面」快捷方式 |

---

> **注意**：如果提示「无法加载文件，因为在此系统上禁止运行脚本」，请先执行：
>
> ```powershell
> Set-ExecutionPolicy -ExecutionPolicy Bypass -Scope Process
> ```

### 手动下载安装

如果需要手动下载安装包：

| 文件 | 说明 | 下载 |
| --- | --- | --- |
| `DeskLane_window_setup.exe` | 图形化安装向导 | [下载](https://github.com/ding9736/DeskLane/releases/latest/download/DeskLane_window_setup.exe) |
| `DeskLane_window.msi` | MSI 安装包（企业部署） | [下载](https://github.com/ding9736/DeskLane/releases/latest/download/DeskLane_window.msi) |

---

## 适用人群

| 用户类型 | 说明 |
| --- | --- |
| 普通用户 | 想快速连接和控制远程设备 |
| 桌面用户 | 希望使用图形化安装向导 |
| 企业运维 | 需要 MSI 进行批量部署或静默安装 |

## 当前发布内容

本次发布包含以下资产：

- `DeskLane_window_setup.exe` — 图形化安装程序
- `DeskLane_window.msi` — MSI 安装包
- `install.ps1` — PowerShell 安装脚本
- `install.sh` — Shell 安装脚本
- `README.md` — 本说明文档

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


