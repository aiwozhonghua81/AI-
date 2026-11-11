<!-- 中文说明开始 -->

# 🇨🇳 中文详细说明 · AionUi

> **本节是给中文读者写的通俗版说明，面向完全没用过这类工具的朋友。**
> 下方「↓ 上游 README 原文开始 ↓」以下是上游 [iOfficeAI/AionUi](https://github.com/iOfficeAI/AionUi) 的原文，**一字未删**。
> 上游另有 9 个语言的 README（简体中文 `docs/readme/readme_ch.md`、繁体、日、韩、葡、西、俄、土、乌），也都保留。

---

## 一、这是什么（一句话说清）

**AionUi 是一个免费的、开源的「AI 员工桌面客户端」—— 它不只跟你聊天，而是让 AI 真正动手操作你电脑上的文件、跑命令、生成文档、爬网页、定时干活。**

### 换个说法

现在的 AI 聊天工具，你问它「帮我把这个文件夹整理一下」，它只能告诉你「你可以这样做...」，然后你自己动手。

**AionUi 是让 AI 真的去做。** 而且它不只接一个模型 —— 你电脑上装了什么 CLI Agent（Claude Code、Codex、Cursor Agent、Qwen Code、Gemini CLI……），它都能**自动发现**并统一调度。

### 三个关键词

| 关键词 | 大白话解释 |
| --- | --- |
| **Cowork（协同办公）** | 项目的自我定位 —— AI 不是聊天机器人，是「和你一起干活的同事」 |
| **Built-in Agent（内置 Agent）** | 装完就能用的 AI 引擎，**不需要你先去装 Claude Code / Gemini CLI** |
| **Multi-Agent（多 Agent）** | 一次可以开几十个 AI 会话，还能让一群 AI 分工合作 |

### 和 Claude Cowork 的关系

上游 README 里有一张对比表，说得很直白：

| 维度 | Claude Cowork | AionUi |
| --- | --- | --- |
| 系统 | 只有 macOS | macOS / Windows / Linux |
| 模型 | 只有 Claude | Gemini、Claude、DeepSeek、OpenAI、Ollama…… 30+ 平台 |
| 交互 | 桌面 GUI | 桌面 GUI + WebUI + Telegram / 飞书 / 钉钉 / 微信 |
| 自动化 | 只能手动 | **Cron 定时任务，7×24 无人值守** |
| 价格 | $100/月 | **免费开源**（只付你选的模型 API 费） |

---

## 二、适合谁用 / 能解决什么问题

### ✅ 适合你，如果你是

| 你是 | 你会得到什么 |
| --- | --- |
| **办公 / 行政 / 运营** | 让 AI 批量整理文件、做 PPT、生成 Excel 报表、每天定时发数据汇总 |
| **程序员** | 已有 Claude Code / Codex 的话，不用换终端 —— 一个界面管所有 Agent |
| **不想折腾命令行的人** | 装个 GUI 就能用 AI Agent，不用学 `bun` / `cargo` / 环境变量 |
| **想自托管 AI 工作台的人** | WebUI 模式跑在服务器上，手机浏览器就能连 |
| **经常出差 / 多设备** | Telegram、飞书、钉钉、微信都能直接跟自己的 AI 对话 |
| **AI Agent 开发者** | 一个功能完整、跨平台、开源的多 Agent 桌面端参考实现 |

### 🎯 能解决的具体问题

| 痛点 | AionUi 的解法 |
| --- | --- |
| **「下载文件夹太乱了」** | 说一句「按类型整理」，AI 自己判断内容并分类 |
| **「每周要手动汇总销售数据做报表」** | 建个定时任务，每周自动跑 |
| **「AI 生成的 PPT 要切出去才能看」** | 内置预览面板，10+ 格式直接看，还能实时编辑 Markdown / 代码 |
| **「每个 Agent 一个终端，窗口开一堆」** | 统一界面 + 并行会话，每个上下文独立 |
| **「我不在电脑前也想让它干活」** | WebUI + 聊天平台集成，手机上随时下达指令 |
| **「不想花钱买 Claude Cowork」** | 免费开源，只付你实际用的模型 API 费用 |

---

## 三、核心功能

### 3.1 内置 Agent —— 装完即用，零配置

- **不需要装任何 CLI 工具** —— Agent 引擎是内置的（基于 [aionrs](https://github.com/iOfficeAI/aionrs)）
- **不需要复杂配置** —— 粘贴任意一个 API Key 就能开始
- **完整 Agent 能力** —— 文件读写、网页搜索、图片生成、MCP 工具
- **21 个开箱即用的专业助手**（内置 assistants）：

| 分类 | 助手 |
| --- | --- |
| **通用** | 🤝 Cowork（自主任务执行）、📋 Planning with Files（Manus 风格文件规划）、🧭 AionUi Butler（产品引导） |
| **PPT** | 📊 PPT Creator、🎬 Morph PPT、🎬 Morph PPT 3D、📐 Pitch Deck Creator（融资路演稿）、📊 Dashboard Creator |
| **文档** | 📝 Word Creator、📋 Word Form Creator（合同/表单模板）、📚 Academic Paper Writer（学术论文）、💰 Financial Model Creator（财务模型） |
| **表格** | 📗 Excel Creator |
| **创意** | 🎮 3D Game（单文件 3D 游戏）、🎨 UI/UX Pro Max（57 种风格、95 套配色）、📈 Beautiful Mermaid（流程图/时序图）、📖 Story Roleplay（沉浸式角色扮演，兼容 SillyTavern） |
| **其他** | 🧭 HUMAN 3.0 Coach（个人成长教练）、📣 Social Job Publisher（招聘发布）、🦞 moltbook（零部署 AI Agent 社交）、🔧 OpenClaw Setup（OpenClaw 集成配置） |

> 内置 skill 包括 `pptx`、`docx`、`pdf`、`xlsx`、`mermaid` 等。

### 3.2 多 Agent 模式 —— 你已经有的 CLI Agent 全都接进来

**自动检测已安装的 CLI 工具**，包括：

> Built-in Agent、**Claude Code**、**Codex**、**Qwen Code**、**Gemini CLI**、**Goose**、**OpenClaw**、**Augment Code**、**CodeBuddy**、**Kimi CLI**、**OpenCode**、**Factory Droid**、**GitHub Copilot**、**Qoder**、**Mistral Vibe**、**Nanobot**、**Snow**、**Hermes**、**Cursor Agent**、**Pi**、**MiMo Code**、**omp**、**Antigravity**，等等。

- **统一界面** —— 一套 UI 管所有 Agent
- **并行会话** —— 同时跑多个 Agent，各自上下文独立
- **MCP 统一管理** —— 所有 MCP 工具在一处管理，按各 Agent 能力自动注入/同步传输方式
- **YOLO / 全自动模式** —— 支持的 Agent 可开启无人值守模式（具体模式和权限行为取决于所选 Agent）

### 3.3 Team Mode（团队模式）—— 让一群 AI 分工协作

```
你 ──► Leader（组长 Agent）
         ├─ 拆解成子任务
         ├─ 通过内置 Team MCP Server 派给 Teammate
         └─ 汇总结果
              ↓
        Teammate A / B / C  ←→  异步邮箱共享结果
              ↓
              共享任务看板（task board）
```

- **Leader 编排** —— 分配、跟踪、汇总结果
- **支持的 leader 后端**：Claude Code、Codex、Hermes Agent、Gemini、Snow CLI、Aion CLI (aionrs)
- **共享工作区** —— 所有 Agent 读写同一个文件夹，文件面板全程可见
- **动态扩缩** —— 运行时随时增减 Teammate；静默的 Agent 会自动升级为失败状态并可一键移除
- **细粒度权限** —— 每个 Agent 有**自己的**权限确认对话框，侧边栏徽标显示待审批数量
- **文件传递** —— Leader 可以把文件附件传给 Teammate

### 3.4 任意 API Key，全功能 Cowork Agent

| 你的 API Key | 你得到什么 |
| --- | --- |
| Gemini API Key | Gemini 驱动的 Cowork Agent |
| OpenAI API Key | GPT 驱动的 Cowork Agent |
| Anthropic API Key | Claude 驱动的 Cowork Agent |
| AWS Bedrock 凭据 | 通过 Aion CLI (aionrs) 的 Bedrock Agent |
| Ollama / LM Studio（本地） | 本地模型 Cowork Agent |
| NewAPI 网关 | 统一访问 20+ 模型 |

**支持 30+ AI 平台**：
- **官方**：Gemini、Gemini (Vertex AI)、Anthropic (Claude)、OpenAI
- **云厂商**：AWS Bedrock、New API
- **国内**：Dashscope (Qwen)、Dashscope Coding Plan、智谱、Moonshot (Kimi)、千帆 (百度)、混元 (腾讯)、零一、ModelScope、无问芯华、天翼、阶跃星辰、SiliconFlow-CN、PPIO
- **国际**：DeepSeek、MiniMax、Novita、OpenRouter、SiliconFlow、xAI、Ark (火山引擎)、Poe
- **本地**：Ollama、LM Studio（通过自定义平台填本地 API 端点）

### 3.5 定时任务（Cron）—— 7×24 无人值守

- **三种调度模式**
  - `Cron 表达式` —— 标准 5 段 cron，支持时区（如 `0 9 * * 1` + `Asia/Shanghai`）
  - `每 N 分钟/小时` —— 固定间隔，如每 30 分钟
  - `一次性` —— 指定时间触发一次后自动禁用
- **两种执行模式**
  - `继续已有会话` —— 追加到绑定的会话，AI 保留完整上下文历史
  - `每次新建会话` —— 每次触发开新会话，适合独立的周期报表
- **AI 自己创建任务** —— 代理可以在对话中自主创建定时任务
- **防休眠** —— 任务活动时 AionUi 自动阻止系统睡眠，唤醒后检测错过的触发
- **细粒度配置** —— 每个任务可单独设置模型、工作目录、推理强度

### 3.6 预览面板 —— 10+ 格式即时查看

| 类别 | 支持格式 |
| --- | --- |
| **文档** | PDF、Word (`.doc`/`.docx`/`.odt`)、Excel (`.xls`/`.xlsx`/`.ods`/`.csv`)、PowerPoint (`.ppt`/`.pptx`/`.odp`) |
| **代码** | JavaScript、TypeScript、Python、Java、Go、Rust、C/C++、CSS、JSON、XML、YAML、Shell 等 **30+ 种** |
| **标记** | Markdown (`.md`/`.markdown`)、HTML (`.html`/`.htm`) |
| **图片** | PNG、JPG、JPEG、GIF、SVG、WebP、BMP、ICO、TIFF、AVIF |
| **其他** | Diff (`.diff`/`.patch`) |

- **即时预览** —— AI 生成文件后直接看，不用切应用
- **实时跟踪 + 可编辑** —— 自动跟踪文件变化，支持实时编辑 Markdown / 代码 / HTML
- **多标签页** —— 同时打开多个文件

### 3.7 智能文件管理

- **自动整理** —— 智能识别内容并自动分类，文件夹保持整洁
- **高效批量** —— 一键重命名、合并文件
- **自动化执行** —— Agent 可独立执行文件操作、读写文件、自动完成任务

### 3.8 Excel 数据处理

- **智能分析** —— AI 分析数据模式并生成洞察
- **自动美化** —— 自动把凌乱的 Excel 报表改成专业样式
- **数据转换** —— 用自然语言命令转换、合并、重构数据
- **报表生成** —— 从原始数据生成综合报表

### 3.9 AI 图像生成与编辑

- **文生图** —— 自然语言描述生成图片
- **图像编辑** —— 修改和增强已有图片
- **图像识别** —— 分析并描述图片内容
- **批量处理** —— 一次生成多张图

### 3.10 文档生成（PPT / Word / Markdown）

- **PPTX 生成器** —— 从大纲或主题生成专业演示
- **Word 文档** —— 生成结构规范的 Word 文档
- **Markdown 文件** —— 创建并格式化 Markdown 文档
- **PDF 转换** —— 在各种文档格式之间转换

### 3.11 多处可达（Cowork from Anywhere）

- **WebUI 模式** —— 浏览器访问，手机 / 平板 / 任何电脑都可以。支持局域网、跨网、服务器部署，扫码或密码登录
- **聊天平台集成**
  - **Telegram** —— 直接在 Telegram 里跟自己的 Agent 对话
  - **飞书（Lark）** —— 通过飞书机器人做企业协作
  - **钉钉** —— AI Card 流式输出，自动降级
  - **微信** —— 个人微信账号集成
  - **企业微信、Slack、Discord** —— 更多平台即将支持

> 配置位置：**AionUi 设置 → WebUI 设置 → Channel**，填 Bot Token。

### 3.12 其他

- **界面自定义** —— 用自己的 CSS 代码自定义颜色、样式、布局
- **多任务并行** —— 多个对话同时开，各自上下文独立不串

---

## 四、怎么快速上手

### 4.1 先决条件（用官方安装包）

| 项目 | 要求 |
| --- | --- |
| **macOS** | 10.15 或更高 |
| **Windows** | Windows 10 或更高 |
| **Linux** | Ubuntu 18.04+ / Debian 10+ / Fedora 32+ |
| **内存** | 建议 4GB+ |
| **存储** | 500MB+ 可用空间 |

### 4.2 最简单的方式：下载安装包

去 [Releases 页面](https://github.com/iOfficeAI/AionUi/releases) 下载对应你系统的安装包（macOS / Windows / Linux），双击安装。

**macOS 也可以用 Homebrew：**

```bash
brew install aionui
```

### 4.3 三步开始用

1. **安装** AionUi
2. **填入任意一个 API Key**
3. **开始 Cowork** —— 内置 AI Agent 已经就绪

### 4.4 WebUI 模式（浏览器 / 服务器 / 手机访问）

#### 方式一：命令行启动

```cmd
# Windows
"C:\Program Files\AionUi\AionUi.exe" --webui

# macOS / Linux
AionUi --webui
```

默认访问 `http://localhost:3000`。

**远程访问**加 `--remote` 参数：

```bash
AionUi --webui --remote
```

#### 方式二：Linux 无头服务器部署

**安装 .deb 包：**

```bash
# 下载最新的 deb 包
wget https://github.com/iOfficeAI/AionUi/releases/latest/download/AionUi-linux-amd64.deb

# 安装
sudo dpkg -i AionUi-linux-amd64.deb
sudo apt-get install -f   # 修复缺失依赖
```

> **容器提示**：如果遇到 `libegl1` / `libgles2` 依赖错误（NVIDIA 容器里常见），用 `dpkg --force-all -i` 强制安装。

**服务管理脚本**（很多云环境没有 systemd，用 nohup 方案）：

```bash
#!/bin/bash
# AionUi WebUI 无头启动脚本
# 用法：./start-aionui.sh [start|stop|restart|status]

PIDFILE="/var/run/aionui.pid"
LOGFILE="/var/log/aionui.log"
WORKDIR="$HOME"   # 改成你的工作目录

start() {
    cd "$WORKDIR"
    nohup xvfb-run --auto-servernum --server-args="-screen 0 1920x1080x24" \
        /usr/bin/AionUi --webui --remote --no-sandbox \
        > "$LOGFILE" 2>&1 &
    echo $! > "$PIDFILE"
    sleep 3
    # ...
}
```

`Xvfb`（虚拟显示器）会由这个脚本通过 `xvfb-run` **自动启用**，你不用自己配。

#### 方式三：Docker

仓库根目录有 `Dockerfile`，构建产物是 Web 服务：

```bash
docker build -t aionui .
docker run -d -p 3000:3000 -v $(pwd)/data:/data aionui
```

镜像里的关键环境变量：

| 变量 | 值 |
| --- | --- |
| `PORT` | `3000` |
| `NODE_ENV` | `production` |
| `ALLOW_REMOTE` | `true` |
| `DATA_DIR` | `/data`（SQLite 数据卷） |

#### 方式四：一键安装脚本（WebUI）

```bash
curl -fsSL https://raw.githubusercontent.com/iOfficeAI/AionUi/main/scripts/install-web.sh | bash

# 指定版本
VERSION=1.0.0 bash install-web.sh

# 指定安装目录
INSTALL_DIR=/opt/aionui-web bash install-web.sh
```

脚本支持的参数：

| 参数 | 说明 | 默认值 |
| --- | --- | --- |
| `--version <ver>` | 安装指定版本 | latest 或 CI 内嵌版本 |
| `--mirror <url>` | 指定镜像源 | GitHub Releases |
| `--install-dir <path>` | 安装目录 | `~/.local/share/aionui-web` |
| `--bin-dir <path>` | 可执行文件目录 | `~/.local/bin` |
| `MIRROR` | 同 `--mirror` | — |
| `CREATE_SYMLINK` | 是否建软链接 | `1` |

### 4.5 开发者：从源码跑

**先决条件**（来自 `docs/contributing/development.md`）：

| 需要什么 | 版本 |
| --- | --- |
| **Node.js** | 22 或更高 |
| **bun** | 包管理器和运行时（[bun.sh](https://bun.sh)） |
| **Rust stable + Cargo** | 构建本地 AionCore 后端 |
| **Python** | 3.11+（编译原生模块用） |
| **prek** | PR 代码检查器（`npm install -g @j178/prek`） |

**重要：AionUi 的开发依赖两个仓库。**

```
workspace/
|-- AionCore/     ← Rust 后端，提供 aioncore 可执行文件
`-- AionUi/       ← Electron 桌面端，自动启动后端二进制
```

**第 1 步：克隆两个仓库**

```bash
git clone https://github.com/iOfficeAI/AionCore.git
git clone https://github.com/iOfficeAI/AionUi.git
```

**第 2 步：构建安装 AionCore**

macOS / Linux：
```bash
cd AionCore
cargo clean
cargo install --path crates/aionui-app --locked

# 让 Cargo 安装的二进制在当前 shell 可见
export PATH="$HOME/.cargo/bin:$PATH"

# 验证 AionUi 能找到后端
which aioncore
aioncore --help
```

Windows PowerShell：
```powershell
cd AionCore
cargo clean
cargo install --path crates/aionui-app --locked

$env:Path = "$env:USERPROFILE\.cargo\bin;$env:Path"

where.exe aioncore
aioncore --help
```

**第 3 步：启动 AionUi**

```bash
cd AionUi
bun install
bun run start
```

### 4.6 常用 npm 脚本

```bash
bun run dev        # Electron 开发模式（Vite HMR）
bun run start      # 同上
bun run start:multi # 多实例模式
bun run webui      # WebUI 开发模式
bun run webui:remote # WebUI + 远程访问
bun run webui:prod  # WebUI 生产模式
bun run cli        # CLI 模式
bun run package    # 构建（不打包）
bun run dist:mac   # 打包 macOS
bun run dist:win   # 打包 Windows
bun run dist:linux # 打包 Linux
bun run resetpass  # 重置密码
```

也有 `justfile` 提供更顺手的配方：

```bash
just dev           # 开发服务器
just webui         # WebUI 开发
just webui-remote  # WebUI 远程
just webui-prod    # WebUI 生产
just cli           # CLI 模式
```

---

## 五、常见问题 / 注意事项

### 坑 1：一定要先装 AionCore，桌面端才能跑

**症状**：`bun run start` 起来了但界面报错或一直转圈。

**原因**：AionUi 只是个 Electron 外壳，真正的后端是 `aioncore` 这个 Rust 二进制。桌面开发服务器通过 `bun run start` 继承的 `PATH` 找它。

**解法**：先在 AionCore 仓库 `cargo install`，再 `which aioncore` / `where.exe aioncore` 确认能找到。找不到就把 `~/.cargo/bin` 加进 PATH，**重开终端**（当前终端不生效）。

### 坑 2：Windows 上 Rust 编译报缺原生构建工具

**症状**：Rust 编译失败，提示缺 MSVC / build tools。

**解法**：装 **Microsoft C++ Build Tools**（Visual Studio 安装器里可选），然后**重开终端**。

### 坑 3：服务器上没显示器，Electron 起不来

**症状**：Linux 云服务器上跑 `--webui` 直接崩。

**解法**：用 `xvfb-run` 包一层。仓库给的脚本已经这么写了：

```bash
xvfb-run --auto-servernum --server-args="-screen 0 1920x1080x24" \
    /usr/bin/AionUi --webui --remote --no-sandbox
```

### 坑 4：容器里装不上 `libegl1` / `libgles2`

**症状**：`dpkg -i` 报缺这两个库。NVIDIA 容器里很常见。

**解法**：`dpkg --force-all -i AionUi-linux-amd64.deb`

### 坑 5：容器里 Office 预览组件启动就崩

**症状**：预览 `.docx` / `.xlsx` 报 ICU 相关错误。

**原因**：Office 预览组件 officecli 是 **.NET 二进制**，缺 ICU 库会在启动时 abort；而 Debian 基础镜像不带 ICU。

**解法**：仓库的 `Dockerfile` 已经处理了 —— 运行时镜像里装了 `libicu-dev`（版本无关，能一直匹配 `libicuNN`）。**自己构建镜像时别忘了加这一步。**

### 坑 6：数据存在哪？会不会上传？

**AionUi 的所有数据都存在本地 SQLite 数据库里，不上传到任何服务器。** 容器部署时数据在 `/data` 卷，记得挂出来：

```bash
-v $(pwd)/data:/data
```

### 坑 7：定时任务时电脑休眠了会不会漏跑

**不会漏掉**。AionUi 在任务活动时自动阻止系统睡眠，**唤醒后会检测错过的触发**。

但如果你强制关掉了应用，那当然不会跑 —— 定时任务需要应用在运行。

### 坑 8：多实例模式

默认一个实例。想同时开多个（比如不同工作区）：

```bash
bun run start:multi
# 或设置环境变量 AIONUI_MULTI_INSTANCE=1
```

### 坑 9：Team Mode 里某个 Agent 一直不吭声

**症状**：某个 Teammate 好像「静默」了。

**解法**：**静默的 Agent 会自动升级为失败状态**，可以一键移除。也检查一下是不是卡在权限确认对话框上 —— Team Mode 里**每个 Agent 有自己的权限对话框**，侧边栏徽标会显示待审批数量。

### 坑 10：内置助手列表在哪看

助手和内置 skill 的**权威定义在 AionCore 仓库里**：

- 助手目录：`AionCore/crates/aionui-app/assets/builtin-assistants/assistants.json`
- 内置 skill：`AionCore/crates/aionui-app/assets/builtin-skills`

AionUi 里助手规则本身是 **Markdown**，可以自定义。

### 坑 11：agent 到底支持哪些？

AionUi **自动检测**已安装的 CLI Agent。上游列了 23 个（Claude Code、Codex、Cursor Agent、Gemini CLI、Qwen Code、OpenCode、Kimi CLI、Goose、OpenClaw、Augment Code、CodeBuddy、Factory Droid、GitHub Copilot、Qoder、Mistral Vibe、Nanobot、Snow、Hermes、Pi、MiMo Code、omp、Antigravity……）。但**能不能真正用起来取决于该 Agent 自身的能力和你的配置**。

---

## 六、目录结构速览

```
AionUi/
├── packages/                  ← monorepo（bun workspaces）
│   ├── desktop/                Electron 桌面端
│   │   ├── src/
│   │   │   ├── main/            主进程
│   │   │   ├── preload/         预加载脚本
│   │   │   ├── renderer/        界面
│   │   │   ├── common/          前后端共用代码
│   │   │   └── sentry.ts        错误上报
│   │   ├── electron.vite.config.ts
│   │   └── electron-builder.yml  打包配置
│   ├── web-host/                Web 服务端（Docker 里跑的就是它）
│   ├── web-cli/                 CLI 模式（bin/ + src/）
│   └── shared-scripts/          各包共用的构建脚本
├── scripts/                   ← 30+ 个构建/发布/校验脚本
│   ├── install-web.sh            WebUI 一键安装脚本
│   ├── install-ubuntu.sh         Ubuntu 安装脚本
│   ├── build-with-builder.js     打包入口
│   ├── webui.ts                  WebUI 启动器
│   ├── prepareAioncore.js        准备 AionCore 后端
│   ├── resolveAioncoreVersion.js 解析 AionCore 版本
│   ├── check-i18n.js             i18n 校验
│   ├── generate-i18n-types.js    生成 i18n 类型
│   ├── smoke-test-install-web.sh  Web 安装冒烟测试
│   ├── smoke-test-web-cli.sh     Web CLI 冒烟测试
│   └── build-mcp-servers.js      MCP Server 构建
├── docs/                      ← 文档
│   ├── contributing/
│   │   ├── development.md          开发指南（本节主要依据）
│   │   └── file-structure.md       文件结构说明
│   ├── guides/
│   │   ├── webui.md                WebUI 启动指南（各平台）
│   │   ├── deploy-server.md        无头服务器部署指南
│   │   ├── custom-theme.md         自定义主题
│   │   ├── cdp.md                  CDP 相关
│   │   ├── hub-testing.md          Hub 测试
│   │   └── acp-image-output.zh-CN.md  ACP 图片输出（中文）
│   ├── readme/                 ← 9 个语言的 README
│   │   ├── readme_ch.md            简体中文
│   │   ├── readme_tw.md            繁体中文
│   │   ├── readme_jp.md / readme_ko.md
│   │   └── readme_es.md / readme_pt.md / readme_tr.md / readme_ru.md / readme_uk.md
│   ├── prds/                   ← 产品需求文档
│   └── theming/                ← 主题相关
├── mobile/                    ← 移动端相关
├── homebrew/                  ← Homebrew 打包配置
├── examples/                  ← 示例
├── resources/                 ← 图片、二维码等资源
├── public/                    ← 静态资源
├── patches/                   ← pnpm/bun 依赖补丁
├── tests/                     ← 测试
├── .github/                   ← CI 工作流
├── .gemini/ .claude/ .aionui/ ← 各 AI 工具的项目配置和 skill
├── package.json / bun.lock    ← 依赖（bun workspaces）
├── Dockerfile                 ← Web 服务镜像
├── justfile                   ← just 命令配方
├── Makefile                   ← 少量辅助 target
├── tsconfig.json / uno.config.ts / playwright.config.ts / vitest.config.ts
├── AGENTS.md / CLAUDE.md      ← 给 AI 编码助手看的项目约定
├── CONTRIBUTING.md / CONTRIBUTING.zh.md
├── CHANGELOG.md / LICENSE (Apache-2.0)
└── readme.md                  ← 你正在看的这个文件（默认首页）
```

### 关键文件一句话解释

| 文件/目录 | 一句话说明 |
| --- | --- |
| `packages/desktop/` | Electron 桌面端 —— 界面在这 |
| `packages/web-host/` | Web 服务端 —— Docker 部署跑的就是它 |
| `packages/web-cli/` | 命令行模式 |
| `scripts/install-web.sh` | WebUI 一键安装脚本（支持版本/镜像源/目录） |
| `scripts/prepareAioncore.js` | 下载/准备 AionCore 后端二进制 |
| `docs/contributing/development.md` | 开发环境搭建的权威文档 |
| `docs/guides/deploy-server.md` | 无头服务器部署（含 Xvfb、nohup 服务脚本） |
| `docs/readme/readme_ch.md` | 官方简体中文版 README |
| `justfile` | `just dev` / `just webui` 等便捷命令 |
| `AGENTS.md` / `CLAUDE.md` | 项目给 AI 编码助手（Claude Code 等）的约定文件 |

---

## 七、本仓库说明

| 项目 | 说明 |
| --- | --- |
| **本仓库** | `aiwozhonghua81/AI-` —— 一个 **fork（派生仓库）**。仓库名在 GitHub 上就是一个 `AI-`（Fork 名称被截断） |
| **上游项目** | **AionUi** —— Cowork with AI Agents |
| **上游地址** | https://github.com/iOfficeAI/AionUi |
| **官网** | https://www.aionui.com |
| **版本** | 2.2.2（package.json） |
| **技术栈** | Electron + React（桌面） / bun workspaces / Rust（AionCore 后端） |
| **许可证** | **Apache-2.0**（宽松，可商用闭源） |
| **本仓库改动** | 仅在 `readme.md` 顶部新增本中文说明区块；**未修改任何源码文件** |

### ⚠️ 关于文件名是小写的 `readme.md`

上游 AionUi 的默认 README 文件名是 **`readme.md`（全小写）**，不是 `README.md`。本仓库保持一致。GitHub 对大小写敏感，clone 下来就是 `readme.md`。

### 关于本仓库曾经「只有 1 个文件」

**排查结论：不是空仓库，也不是 gitlink/submodule。**

- 远端 `refs/heads/main` 指向 `11cd2a9a2`，是一个正常提交
- 该提交下有 **2344 个文件**（`git ls-files | wc -l`）
- 本地 clone 时 `.git/HEAD` 引用损坏（`fatal: failed to resolve HEAD as a valid ref`），导致工作区看起来是空的
- **修复方式**：`git fetch origin main && git checkout -b main origin/main` —— 之后一切正常

所以**内容是完整的**，不是「本 fork 内容待同步」。

### README 的结构

```
┌─────────────────────────────────────────────┐
│  👆 本节：中文详细说明（面向普通读者）        │  ← 本次新增
├─────────────────────────────────────────────┤
│  👇 下方：上游 README 原文（未删改）           │  ← 上游 iOfficeAI/AionUi 撰写
└─────────────────────────────────────────────┘
```

- 上游 README 共 **747 行**，内容详尽：与 Claude Cowork 的对比表、21 个内置助手列表、30+ 支持平台列表、多 Agent / Team Mode 详解、定时任务、预览面板、文件管理、Excel、图像、文档生成、WebUI 与聊天平台集成、FAQ、社区链接。**这些内容全部保留在下方。**
- 另外 9 个语言的 README 也**全部保留**在 `docs/readme/` 目录。
- 本中文区块的**增量价值**在于：
  1. 把「安装 / WebUI / 服务器部署 / Docker / 源码开发」四条路径的**真实命令**从 `docs/` 里挖出来汇总成一份速查
  2. 补充了 11 条**实际会踩的坑**（AionCore 必须先装、Windows C++ Build Tools、Xvfb、libegl1、容器 ICU、Team Mode 静默 Agent 等）
  3. 补充了「AionUi + AionCore 双仓库」这个上游 README 里只在开发章节提一句、但实际最容易卡住的关键结构

---

## 📌 快速自查清单

想快速体验：

- [ ] 从 Releases 下载了对应系统的安装包
- [ ] 准备了一个 API Key（Gemini / OpenAI / Anthropic 任意一个）
- [ ] 至少 4GB 内存、500MB 磁盘空间
- [ ] 想在手机上用 → 装完记得开 WebUI 并配置 Channel Bot Token

想开发：

- [ ] Node.js 22+、bun、Rust stable、Cargo、Python 3.11+、prek 都装好了
- [ ] **AionCore 已 clone 并 `cargo install` 成功**
- [ ] `which aioncore` / `where.exe aioncore` 有输出
- [ ] `~/.cargo/bin` 已在 PATH 里（且**重开过终端**）

---

<!-- 中文说明结束 -->

---

↓ **上游 README 原文开始**（以下内容来自 [iOfficeAI/AionUi](https://github.com/iOfficeAI/AionUi)，未做任何删改） ↓

<p align="center">
  <img src="./resources/aionui-banner-1.png" alt="AionUi - Cowork with AI Agents" width="100%">
</p>

<p align="center">
  <img src="https://img.shields.io/github/v/release/iOfficeAI/AionUi?style=flat-square&color=32CD32" alt="Version">
  &nbsp;
  <img src="https://img.shields.io/badge/license-Apache--2.0-32CD32?style=flat-square&logo=apache&logoColor=white" alt="License">
  &nbsp;
  <img src="https://img.shields.io/badge/platform-macOS%20%7C%20Windows%20%7C%20Linux-6C757D?style=flat-square&logo=linux&logoColor=white" alt="Platform">
</p>

<p align="center">
  <a href="https://trendshift.io/repositories/15423" target="_blank">
    <img src="https://trendshift.io/api/badge/repositories/15423" alt="GitHub Trending" height="80">
  </a>
</p>

---

<p align="center">
  <strong>A free, open-source, Cowork app with AI Agents</strong><br>
  <em>Built-in Agent | Zero Setup | Any API Key | Multi-Agents | Remote Access | Cross-Platform | 24/7 Automation</em>
</p>

<p align="center">
  <a href="https://github.com/iOfficeAI/AionUi/releases">
    <img src="https://img.shields.io/badge/⬇️%20Download%20Now-Latest%20Release-32CD32?style=for-the-badge&logo=github&logoColor=white" alt="Download Latest Release" height="50">
  </a>
</p>

<p align="center">
  <strong>English</strong> | <a href="./docs/readme/readme_ch.md">简体中文</a> | <a href="./docs/readme/readme_tw.md">繁體中文</a> | <a href="./docs/readme/readme_jp.md">日本語</a> | <a href="./docs/readme/readme_ko.md">한국어</a> | <a href="./docs/readme/readme_es.md">Español</a> | <a href="./docs/readme/readme_pt.md">Português</a> | <a href="./docs/readme/readme_tr.md">Türkçe</a> | <a href="./docs/readme/readme_ru.md">Русский</a> | <a href="./docs/readme/readme_uk.md">Українська</a> | <a href="https://www.aionui.com" target="_blank">Official Website</a>
</p>

<p align="center">
  <strong>💬 Community:</strong> <a href="https://discord.gg/2QAwJn7Egx" target="_blank">Discord (English)</a> | <a href="./resources/wx-26.png" target="_blank">微信 (中文群)</a> | <a href="https://twitter.com/AionUI" target="_blank">Twitter</a>
</p>

---

<p align="center">
  <a href="https://x.com/AionUi/status/2079493379914961069" target="_blank">
    <img src="./resources/kimi/contributor-bonus-black-blue.jpg" alt="AionUi × Kimi Contributor Bonus" width="600">
  </a>
</p>

<p align="center">
  🎁 <strong>AionUi × Kimi Partnership</strong>: Free premium <strong>Kimi "Allegretto" plans ($39/mo · ¥199/mo value)</strong> for our contributors!
</p>

<h3 align="center">
  <a href="https://x.com/AionUi/status/2079493379914961069" target="_blank">View Campaign Details & How to Claim →</a>
</h3>

<p align="center">
  <sub><strong>Kimi K3</strong> is here and works out of the box in AionUi — <a href="https://www.kimi.com/code?aff=aionui" target="_blank">get a Kimi For Coding plan</a> or an API key (<a href="https://platform.kimi.ai?track_id=track-32e04532b08d460fac729191744fa75c&aff=aionui" target="_blank">Global</a> / <a href="https://platform.kimi.com?track_id=track-98f92981df1c4c61b2c68930ba3ab658&aff=aionui" target="_blank">China</a>) · ready to claim? <a href="https://github.com/iOfficeAI/AionUi/discussions/3640">comment here</a></sub>
</p>

---

## 📋 Quick Navigation

<p align="center">

[Cowork in Action](#-cowork-in-action) ·
[Why Choose AionUi?](#-why-choose-aionui-over-claude-cowork) ·
[Quick Start](#-quick-start) ·
[Community](#-community--support)

</p>

---

## Cowork — AI Agents That Work Alongside You

**AionUi is more than a chat client.** It's a Cowork platform where AI agents work alongside you on your computer — reading files, writing code, browsing the web, and automating tasks. You see everything the agent does, and you're always in control.

|                                 | Traditional AI Chat Clients | **AionUi (Cowork)**                                                                                                                      |
| :------------------------------ | :-------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------- |
| AI can operate on your files    | Limited or No               | **Yes — built-in agent with full file access**                                                                                           |
| AI can execute multi-step tasks | Limited                     | **Yes — autonomous with your approval**                                                                                                  |
| Remote access from phone        | Rarely                      | **WebUI + Telegram / Lark / DingTalk / WeChat**                                                                                          |
| Scheduled automation            | No                          | **Cron — 24/7 unattended**                                                                                                               |
| Multiple AI Agents at once      | No                          | **Dozens of external agents — including Claude Code, Codex, Qwen Code, Hermes Agent, Cursor Agent, and more — in one unified interface** |
| Price                           | Free / Paid                 | **Free & Open Source**                                                                                                                   |

<p align="center">
  <img src="./resources/offica-ai BANNER-function.png" alt="AionUi Cowork Platform" width="800">
</p>

---

## Built-in Agent — Install & Go, Zero Configuration

AionUi ships with a complete AI agent engine. Unlike tools that require you to install CLI agents separately, **AionUi works the moment you install it**.

- **No CLI tools to install** — the agent engine is built in
- **No complex setup** — paste any API key to get started
- **Full agent capabilities** — file read/write, web search, image generation, MCP (Model Context Protocol) tools
- **Ready-to-use assistants** — 21 built-in professional assistants (Cowork, PPT Creator, Word Creator, Word Form Creator, Excel Creator, Morph PPT, Morph PPT 3D, Pitch Deck Creator, Dashboard Creator, Academic Paper Writer, Financial Model Creator, and more) ready to use immediately

<p align="center">
  <img src="./resources/homepage.png" alt="Built-in Agents" width="800">
</p>

### **Office assistants — PPT, Word & Excel**

These tracks match what the app actually ships: **Morph PPT** presets and the **`pptx` / `docx` / `xlsx` skills**. The canonical [assistant catalog](https://github.com/iOfficeAI/AionCore/blob/main/crates/aionui-app/assets/builtin-assistants/assistants.json) and [built-in skills](https://github.com/iOfficeAI/AionCore/tree/main/crates/aionui-app/assets/builtin-skills) are maintained with AionCore. Want document/table output? AionUi’s built-in **[OfficeCLI](https://github.com/iOfficeAI/OfficeCLI)** helps PPT (Morph), Word (`.docx`), and Excel (`.xlsx/.xlsm/.csv`) go from request to deliverable faster and more reliably.
The three assistant types map to file workflows, and the final outputs are directly editable and reusable.

#### **PPT assistant**

> **Output:** editable Morph PPT (`.pptx`)
> Morph-animated slide-to-slide transitions with coherent story pacing; powered by [OfficeCLI](https://github.com/iOfficeAI/OfficeCLI).

<table>
  <tr>
    <td align="center" width="50%">
      <img src="./resources/morph-ppt-balanced.gif" alt="Morph PPT — slide-to-slide transitions (OfficeCLI)" width="390">
    </td>
    <td align="center" width="50%">
      <img src="./resources/readme-demo-assistant-ppt.gif" alt="PPT assistant — screen recording" width="390">
    </td>
  </tr>
</table>

#### **Word assistant**

> **Output:** editable Word (`.docx`)
> Paper/thesis writing and production-ready document editing via the `docx` skill; powered by [OfficeCLI](https://github.com/iOfficeAI/OfficeCLI).

<table>
  <tr>
    <td align="center" width="50%">
      <img src="./resources/readme-demo-generate-academic-paper.gif" alt="Generate academic paper demo" width="390">
    </td>
    <td align="center" width="50%">
      <img src="./resources/readme-demo-assistant-write-paper.gif" alt="Paper writing assistant demo" width="390">
    </td>
  </tr>
</table>

#### **Excel assistant**

> **Output:** usable Excel (`.xlsx/.xlsm/.csv`)
> Generate/refresh spreadsheets with `xlsx` for analysis, auto-formatting, and charts; powered by [OfficeCLI](https://github.com/iOfficeAI/OfficeCLI).

<table>
  <tr>
    <td align="center" width="50%">
      <img src="./resources/readme-demo-generate-excel.gif" alt="Excel generation demo" width="390">
    </td>
    <td align="center" width="50%">
      <img src="./resources/readme-demo-assistant-excel.gif" alt="Excel assistant demo" width="390">
    </td>
  </tr>
</table>

---

## Multi-Agent Mode — Already Have CLI Agents? Bring Them In

If you already use Claude Code, Codex, Hermes Agent, or OpenClaw, AionUi auto-detects them and lets you Cowork with all of them — alongside the built-in agent.

**Supported Agents:** Built-in Agent (powered by the embedded [aionrs](https://github.com/iOfficeAI/aionrs) agent engine) • Claude Code • Codex • Qwen Code • Gemini CLI • Goose • OpenClaw • Augment Code • CodeBuddy • Kimi CLI • OpenCode • Factory Droid • GitHub Copilot • Qoder • Mistral Vibe • Nanobot • Snow • Hermes • Cursor Agent • Pi • MiMo Code • omp • Antigravity • and more

<p align="center">
  <img src="./resources/multi-agent支持openclaw.gif" alt="Multi-Agent Cowork" width="800">
</p>

- **Auto Detection** — automatically recognizes installed CLI tools
- **Unified Interface** — one Cowork platform for all your AI agents
- **Parallel Sessions** — run multiple agents simultaneously with independent context
- **MCP Unified Management** — manage MCP (Model Context Protocol) tools in one place; AionUi injects or syncs compatible transports according to each agent's capabilities
- **YOLO / Full-Auto Mode** — supported agents can expose an unattended mode; available modes and permission behavior depend on the selected agent

### Team Mode — Coordinated Multi-Agent Collaboration

Run multiple AI agents as an organized team: a **Leader** agent receives your instructions, breaks them into subtasks, and delegates to **Teammate** agents via a built-in Team MCP Server. Teammates execute in parallel, share results through an async mailbox, and write to a shared task board.

<p align="center">
  <img src="./resources/AionUi_team.gif" alt="Team Mode overview" width="800">
</p>

- **Parallel multi-agent execution** — Leader breaks tasks into subtasks and delegates to Teammate agents running in parallel; each Teammate uses its own model through the selected backend. External agents connect through ACP (Agent Client Protocol), while AionUi coordinates the team
- **Leader orchestration** — Leader assigns, tracks, and aggregates results; supported backends include Claude Code, Codex, Hermes Agent, Gemini, Snow CLI, and Aion CLI
- **Team-isolated workspace** — all agents share the same folder; each has its own permission dialog with sidebar badge for pending approvals

<details>
<summary><strong>🔍 View Team Mode Details ▶️</strong></summary>

<br>

- **Shared Workspace** — all agents read/write the same folder; the file panel stays visible throughout
- **Supported backends** — Claude Code, Codex, Gemini, Snow CLI, Aion CLI (aionrs); other ACP backends with `mcpCapabilities.stdio` are auto-supported
- **Dynamic scaling** — add or remove Teammates while the team is running; silent agents auto-escalate to failed with one-click removal
- **Granular permissions** — each agent has its own permission confirmation dialog; sidebar badge shows pending approvals
- **File sharing** — Leader can pass file attachments to Teammates

</details>

---

## Any API Key, Full Cowork Agent Power

Other AI apps give you a chatbox with your API key. **AionUi gives you a full Cowork agent.**

| Your API Key               | What You Get                                |
| :------------------------- | :------------------------------------------ |
| Gemini API Key             | Gemini-powered Cowork Agent                 |
| OpenAI API Key             | GPT-powered Cowork Agent                    |
| Anthropic API Key          | Claude-powered Cowork Agent                 |
| AWS Bedrock credentials    | Bedrock-powered Agent via Aion CLI (aionrs) |
| Ollama / LM Studio (local) | Local model Cowork Agent                    |
| NewAPI Gateway             | Unified access to 20+ models                |

Same agent capabilities — file read/write, web search, image generation, tool use — regardless of which model powers it. AionUi supports **30+ AI platforms** including cloud services and local deployments.

<p align="center">
  <img src="./resources/llm_newapi.png" alt="Multi-Model Support" width="800">
</p>

<details>
<summary><strong>🔍 View All 30+ Supported Platforms ▶️</strong></summary>

<br>

**Comprehensive Platform Support:**

- **Official Platforms** — Gemini, Gemini (Vertex AI), Anthropic (Claude), OpenAI
- **Cloud Providers** — AWS Bedrock, New API (unified AI model gateway)
- **Chinese Platforms** — Dashscope (Qwen), Dashscope Coding Plan, Zhipu, Moonshot (Kimi), Qianfan (Baidu), Hunyuan (Tencent), Lingyi, ModelScope, InfiniAI, Ctyun, StepFun, SiliconFlow-CN, PPIO
- **International Platforms** — DeepSeek, MiniMax, Novita, OpenRouter, SiliconFlow, xAI, Ark (Volcengine), Poe
- **Local Models** — Ollama, LM Studio (via Custom platform with local API endpoint)

AionUi also supports [NewAPI](https://github.com/QuantumNous/new-api) gateway service — a unified AI model hub that aggregates and distributes various LLMs. Flexibly switch between different models in the same interface to meet various task requirements.

</details>

---

## Extensible Assistants & Skills

_Extensible assistant system with 21 built-in professional assistants and a three-tier skill system. Create and manage your own assistants and skills._

- **Create Custom Assistants** — Define your own assistants with custom rules and capabilities
- **Three-tier Skills** — Builtin skills (shipped with AionUi), custom skills (your own), and Extension skills (contributed by third-party extensions); enable/disable per conversation with the skill indicator
- **Per-conversation Control** — A skill indicator in the chat header shows active skills for the current conversation; search and exclude skills as needed

<p align="center">
  <img src="./resources/assitants.png" alt="AI Assistants & Skills Ecosystem" width="800">
</p>

AionUi supports three skill layers: **built-in** skills (shipped with the app), **custom** skills (user-defined), and **extension** skills (loaded from the Extension SDK).

<details>
<summary><strong>🔍 View Assistant Details and Custom Skills ▶️</strong></summary>

<br>

AionUi includes **21 professional assistants** with predefined capabilities, extendable through custom skills:

- **🤝 Cowork** — Autonomous task execution (file operations, document processing, workflow planning)
- **📊 PPT Creator / Morph PPT / Morph PPT 3D** — Generate and animate PPTX presentations with Morph transitions
- **📐 Pitch Deck Creator** — Investor-ready pitch deck generation
- **📊 Dashboard Creator** — Data dashboard generation
- **📝 Word Creator** — Production-ready Word (`.docx`) document generation
- **📋 Word Form Creator** — Structured Word form / contract template generation
- **📗 Excel Creator** — Spreadsheet generation with analysis, charts, and auto-formatting
- **🎓 Academic Paper Writer** — Structured academic paper writing
- **💰 Financial Model Creator** — Financial models and projections
- **🎮 3D Game** — Single-file 3D game generation
- **🎨 UI/UX Pro Max** — Professional UI/UX design (57 styles, 95 color palettes)
- **📋 Planning with Files** — File-based planning for complex tasks (Manus-style persistent markdown planning)
- **🧭 HUMAN 3.0 Coach** — Personal development coach
- **📣 Social Job Publisher** — Job posting and publishing
- **🦞 moltbook** — Zero-deployment AI agent social networking
- **📈 Beautiful Mermaid** — Flowcharts, sequence diagrams, and more
- **🔧 OpenClaw Setup** — Setup and configuration assistant for OpenClaw integration
- **📖 Story Roleplay** — Immersive story roleplay with character cards and world info (SillyTavern compatible)
- **🧭 AionUi Butler** — Product guidance, setup help, and troubleshooting inside AionUi

**Custom Skills**: Import or create skills from **Settings → Skills**, then attach them to assistants as needed. Skills come from three sources: built-in (shipped with AionUi), custom (your own), and Extension (contributed via the Extension SDK). Built-in skills include `pptx`, `docx`, `pdf`, `xlsx`, `mermaid`, and more.

> 💡 The canonical built-in definitions live in AionCore's [assistant catalog](https://github.com/iOfficeAI/AionCore/blob/main/crates/aionui-app/assets/builtin-assistants/assistants.json); assistant rules remain Markdown and can be customized in AionUi.

</details>

---

## Cowork from Anywhere

_Your 24/7 AI assistant — access AionUi from any device, anywhere._

- **WebUI Mode** — access via browser from phone, tablet, or any computer. Supports LAN, cross-network, and server deployment. QR code or password login.

- **Chat Platform Integration**
  - **Telegram** — Cowork with your AI agent directly from Telegram
  - **Lark (Feishu)** — Cowork through Feishu bots for enterprise collaboration
  - **DingTalk** — AI Card streaming with automatic fallback
  - **WeChat** — Personal WeChat account integration
  - **WeCom (企业微信)**, **Slack**, **Discord** and more platforms coming soon

> **Setup:** AionUi Settings → WebUI Settings → Channel, configure the Bot Token.

<p align="center">
  <img src="./resources/webui-remote.gif" alt="WebUI remote access demo" width="800">
</p>

<p align="center"><em>Remote control &amp; monitor your agent — Claude, Gemini, Codex. Use from browser or phone, same as Claude Code remote.</em></p>

> [Remote Internet Access Tutorial](https://github.com/iOfficeAI/AionUi/wiki/Remote-Internet-Access-Guide-Chinese)

## ✨ Cowork in Action

### **Scheduled Tasks — Cowork on Autopilot**

_Set it up once, the AI agent runs automatically on schedule — truly 24/7 unattended operation._

- **Natural Language** — tell the agent what to do, just like chatting
- **Three scheduling modes** — standard cron expression (with timezone), fixed interval (every N minutes/hours), or one-time trigger
- **AI-created tasks** — agents can autonomously create scheduled tasks during a conversation
- **Use Cases:** scheduled data aggregation, report generation, file organization, reminders

<p align="center">
  <img src="./resources/alart-task.png" alt="Scheduled Tasks" width="800">
</p>

<details>
<summary><strong>🔍 View Scheduled Task Details ▶️</strong></summary>

<br>

**Scheduling modes:**

- `Cron expression` — standard 5-field cron with timezone support (e.g. `0 9 * * 1`, `Asia/Shanghai`)
- `Every N minutes/hours` — fixed interval, e.g. run every 30 minutes
- `One-time` — trigger once at a specified datetime, then auto-disable

**Execution modes:**

- `Continue in existing conversation` — appends to the bound conversation so the AI retains full context history
- `Create new conversation each time` — opens a fresh session on each trigger, ideal for independent periodic reports

**Other capabilities:**

- **Conversation-Bound** — Each scheduled task is bound to a conversation, maintaining context and history
- **Automatic Execution** — Tasks run automatically at scheduled times, sending messages to the conversation
- **Easy Management** — Create, modify, enable/disable, delete, and view scheduled tasks anytime
- **Keep-awake** — AionUi automatically prevents system sleep while tasks are active, and detects missed triggers after wake
- **Advanced config** — each task can have its own model, workspace directory, and reasoning effort settings

**Real-World Examples:**

- Daily weather report generation
- Weekly sales data aggregation
- Monthly backup file organization
- Custom reminder notifications

</details>

---

### **Preview Panel — Instantly View AI-Generated Results**

_10+ formats: PDF, Word, Excel, PPT, code, Markdown, images, HTML, Diff — view everything without switching apps._

- **Instant Preview** — after the agent generates files, view results immediately without switching apps
- **Real-time Tracking + Editable** — automatically tracks file changes; supports live editing of Markdown, code, HTML
- **Multi-Tab Support** — open multiple files simultaneously, each in its own tab

<p align="center">
  <img src="./resources/preview.gif" alt="Preview Panel" width="800">
</p>

<details>
<summary><strong>🔍 View Complete Format List ▶️</strong></summary>

<br>

**Supported Preview Formats:**

- **Documents** — PDF, Word (`.doc`, `.docx`, `.odt`), Excel (`.xls`, `.xlsx`, `.ods`, `.csv`), PowerPoint (`.ppt`, `.pptx`, `.odp`)
- **Code** — JavaScript, TypeScript, Python, Java, Go, Rust, C/C++, CSS, JSON, XML, YAML, Shell scripts, and 30+ programming languages
- **Markup** — Markdown (`.md`, `.markdown`), HTML (`.html`, `.htm`)
- **Images** — PNG, JPG, JPEG, GIF, SVG, WebP, BMP, ICO, TIFF, AVIF
- **Other** — Diff files (`.diff`, `.patch`)

</details>

---

### **Smart File Management — Automated File Operations**

_Batch renaming, automatic organization, smart classification, file merging — the Cowork agent handles it for you._

<p align="center">
  <img src="./resources/aionui sort file 2.gif" alt="Smart File Management" width="800">
</p>

<details>
<summary><strong>🔍 View File Management Features Details ▶️</strong></summary>

<br>

- **Auto Organize** — Intelligently identify content and auto-classify, keeping folders tidy
- **Efficient Batch** — One-click rename, merge files, say goodbye to tedious manual tasks
- **Automated Execution** — AI agents can independently execute file operations, read/write files, and complete tasks automatically

**Use Cases:**

- Organize messy download folders by file type
- Batch rename photos with meaningful names
- Merge multiple documents into one
- Auto-classify files by content

</details>

---

### **Excel Data Processing — AI-Powered Analysis**

_Deeply analyze Excel data, automatically beautify reports, and generate insights — all powered by AI agents._

<p align="center">
  <img src="./resources/generate_xlsx.gif" alt="Excel Processing" width="800">
</p>

<details>
<summary><strong>🔍 View Excel Processing Features ▶️</strong></summary>

<br>

- **Smart Analysis** — AI analyzes data patterns and generates insights
- **Auto Formatting** — Automatically beautify Excel reports with professional styling
- **Data Transformation** — Convert, merge, and restructure data with natural language commands
- **Report Generation** — Create comprehensive reports from raw data

**Use Cases:**

- Analyze sales data and generate monthly reports
- Clean and format messy Excel files
- Merge multiple spreadsheets intelligently
- Create data visualizations and charts

</details>

---

### **AI Image Generation & Editing**

_Intelligent image generation, editing, and recognition, powered by Gemini_

<p align="center">
  <img src="./resources/Image_Generation.gif" alt="AI Image Generation" width="800">
</p>

<details>
<summary><strong>🔍 View Image Generation Features ▶️</strong></summary>

<br>

- **Text-to-Image** — Generate images from natural language descriptions
- **Image Editing** — Modify and enhance existing images
- **Image Recognition** — Analyze and describe image content
- **Batch Processing** — Generate multiple images at once

</details>

> [Image generation model configuration guide](https://github.com/iOfficeAI/AionUi/wiki/AionUi-Image-Generation-Tool-Model-Configuration-Guide)

---

### **Document Generation — PPT, Word, Markdown**

_Automatically generate professional documents — presentations, reports, and more — with AI agents._

<p align="center">
  <img src="./resources/file_generation_preview.png" alt="Document Generation" width="800">
</p>

<details>
<summary><strong>🔍 View Document Generation Features ▶️</strong></summary>

<br>

- **PPTX Generator** — Create professional presentations from outlines or topics
- **Word Documents** — Generate formatted Word documents with proper structure
- **Markdown Files** — Create and format Markdown documents for documentation
- **PDF Conversion** — Convert between various document formats

**Use Cases:**

- Generate quarterly business presentations
- Create technical documentation
- Convert PDF to editable formats
- Auto-format research papers

</details>

### **Personalized Interface Customization**

_Customize with your own CSS code, make your interface match your preferences_

<p align="center">
  <img src="./resources/css with skin.gif" alt="CSS Customization" width="800">
</p>

- ✅ **Fully Customizable** — Freely customize interface colors, styles, layout through CSS code, create your exclusive experience

---

### **Multi-Task Parallel Processing**

_Open multiple conversations, tasks don't get mixed up, independent memory, double efficiency_

<p align="center">
  <img src="./resources/multichat-side-by-side.gif" alt="Multi-Task Parallel" width="800">
</p>

- ✅ **Independent Context** — Each conversation maintains its own context and history
- ✅ **Parallel Execution** — Run multiple tasks simultaneously without interference
- ✅ **Smart Management** — Easy switching between conversations with visual indicators

---

## 🤔 Why Choose AionUi Over Claude Cowork?

<details>
<summary><strong>Click to see detailed comparison</strong></summary>

<br>

AionUi is a **free and open-source Multi-AI Agent Desktop**. Compared to Claude Cowork which only runs on macOS and is locked to Claude, AionUi is its full-model, cross-platform enhanced version.

| Dimension     | Claude Cowork | AionUi                                                    |
| :------------ | :------------ | :-------------------------------------------------------- |
| OS            | macOS Only    | macOS / Windows / Linux                                   |
| Model Support | Claude Only   | Gemini, Claude, DeepSeek, OpenAI, Ollama, ...             |
| Interaction   | Desktop GUI   | Desktop GUI + WebUI + Telegram / Lark / DingTalk / WeChat |
| Automation    | Manual only   | Cron scheduled tasks — 24/7 unattended                    |
| Cost          | $100/month    | Free & Open Source                                        |

Deep AI Office Scenario Support:

- **File Management**: Intelligently organize local folders and batch rename with one click.
- **Data Processing**: Deeply analyze and automatically beautify Excel reports.
- **Document Generation**: Automatically write and format PPT, Word, and Markdown documents.
- **Instant Preview**: Built-in 10+ format preview panels, AI collaboration results instantly visible.

</details>

---

## Quick Q&A

<details>
<summary><strong>Q: Do I need to install Gemini CLI or Claude Code first?</strong></summary>
A: <strong>No.</strong> AionUi has a built-in AI agent that works immediately after installation. Just enter any API key to get started. If you also have CLI tools like Claude Code or Gemini CLI installed, AionUi will auto-detect and integrate them for even more capabilities.
</details>

<details>
<summary><strong>Q: What can I do with AionUi?</strong></summary>
A: AionUi is your <strong>private Cowork workspace</strong>. The built-in agent can batch organize folders, process Excel data, generate documents, search the web, and generate images. With Multi-Agent Mode, you can also leverage Claude Code, Codex, and other powerful CLI agents through the same interface.
</details>

<details>
<summary><strong>Q: Is it free?</strong></summary>
A: AionUi is completely free and open source. You only pay for the API usage of whichever provider you choose, and you can use API keys from any provider you prefer.
</details>

<details>
<summary><strong>Q: Can I run AionUi on a server (headless)?</strong></summary>
A: Yes — AionUi WebUI mode runs as a standalone HTTP server. See the WebUI section above for setup instructions.
</details>

<details>
<summary><strong>Q: Is my data secure?</strong></summary>
A: All data is stored locally in a SQLite database. Nothing is uploaded to any server.
</details>

---

## See How People Use AionUi

<p align="center">
  <a href="https://www.youtube.com/watch?v=vWxE6VO9TKo" target="_blank">
    <img src="https://img.youtube.com/vi/vWxE6VO9TKo/maxresdefault.jpg" alt="Hermes + Aion UI is Insane (FREE)!" width="400">
  </a>
  &nbsp;&nbsp;
  <a href="https://www.youtube.com/watch?v=RgSLdOhICZw" target="_blank">
    <img src="https://img.youtube.com/vi/RgSLdOhICZw/maxresdefault.jpg" alt="OpenClaw + Aion UI is Insane (FREE!)" width="400">
  </a>
</p>
<p align="center">
  <em>Julian Goldie SEO — Hermes + Aion UI is Insane (FREE!) · 27K views</em> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <em>Julian Goldie SEO — OpenClaw + Aion UI is Insane (FREE!) · 11K views</em>
</p>

<p align="center">
  <a href="https://www.youtube.com/watch?v=yUU5E-U5B3M" target="_blank">
    <img src="https://img.youtube.com/vi/yUU5E-U5B3M/maxresdefault.jpg" alt="WorldofAI Review" width="400">
  </a>
  &nbsp;&nbsp;
  <a href="https://www.youtube.com/watch?v=enQnkKfth10" target="_blank">
    <img src="https://img.youtube.com/vi/enQnkKfth10/maxresdefault.jpg" alt="Julian Goldie SEO Review" width="400">
  </a>
</p>
<p align="center">
  <em>WorldofAI (200K subscribers)</em> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <em>Julian Goldie SEO (384K subscribers)</em>
</p>

### Community Articles

- [Open-source free Cowork, full model integration + autonomous file operations](https://mp.weixin.qq.com/s/F3f-CCsVPaK3lK00jXhOOg) — Open Source AI Project Landing
- [Making ordinary people use Claude Code like an APP](https://mp.weixin.qq.com/s/TsMojSbkUUFvsd-HQCazZg) — Lazy Cat Loves Fishing
- [5500 Stars: How Open Source Breaks Anthropic's AI Tool Moat](https://mp.weixin.qq.com/s/saEk49cYV6MqBgw19Lw6Gw) — AI Silicon Moment

> **Made a video about AionUi?** [Let us know on X](https://x.com/AionUi) and we'll feature it here!

---

## 🚀 Quick Start

### System Requirements

- **macOS**: 10.15 or higher
- **Windows**: Windows 10 or higher
- **Linux**: Ubuntu 18.04+ / Debian 10+ / Fedora 32+
- **Memory**: 4GB+ recommended
- **Storage**: 500MB+ available space

### Install

<p>
  <a href="https://github.com/iOfficeAI/AionUi/releases">
    <img src="https://img.shields.io/badge/Download-Latest%20Release-32CD32?style=for-the-badge&logo=github&logoColor=white" alt="Download Latest Release" height="50">
  </a>
</p>

Click the button above to go to the Releases page and download the installer for your platform (macOS / Windows / Linux).

```bash
# Alternatively, macOS via Homebrew
brew install aionui
```

### Get Started in 3 Steps

1. **Install** AionUi
2. **Enter** any API key to get started
3. **Start Coworking** — the built-in AI agent is ready to go

### 📖 Detailed Guides

<details>
<summary><strong>📖 Expand to View Complete Usage Guide</strong></summary>

<br>

**🚀 Quick Start**

- [📖 Complete Installation Guide](https://github.com/iOfficeAI/AionUi/wiki/Getting-Started) — Detailed steps from download to configuration
- [⚙️ LLM Configuration Guide](https://github.com/iOfficeAI/AionUi/wiki/LLM-Configuration) — Multi-platform AI model configuration
- [🤖 Multi-Agent Mode Setup](https://github.com/iOfficeAI/AionUi/wiki/ACP-Setup) — Integrate terminal AI agents
- [🔌 MCP Tool Configuration](https://github.com/iOfficeAI/AionUi/wiki/MCP-Configuration-Guide) — Model Context Protocol server setup
- [🌐 WebUI Configuration Guide](https://github.com/iOfficeAI/AionUi/wiki/WebUI-Configuration-Guide) — Complete WebUI setup and configuration tutorial

**🎯 Use Cases**

- [📁 File Management](https://github.com/iOfficeAI/AionUi/wiki/file-management) — Smart file organization
- [📊 Excel Processing](https://github.com/iOfficeAI/AionUi/wiki/excel-processing) — AI-driven data processing
- [🎨 Image Generation](https://github.com/iOfficeAI/AionUi/wiki/AionUi-Image-Generation-Tool-Model-Configuration-Guide) — AI image creation
- [📚 More Use Cases](https://github.com/iOfficeAI/AionUi/wiki/Use-Cases-Overview)

**❓ Support & Help**

- [❓ FAQ](https://github.com/iOfficeAI/AionUi/wiki/FAQ) — Questions and troubleshooting
- [🔧 Configuration & Usage Tutorials](https://github.com/iOfficeAI/AionUi/wiki/Configuration-Guides) — Complete configuration documentation

</details>

---

## 💬 Community & Support

**Your ideas matter!** We value every suggestion and feedback.

<p align="center">
  <a href="https://x.com/AionUi" target="_blank">
    <img src="./resources/contactus-x.png" alt="Contact Us on X" width="600">
  </a>
</p>

- [GitHub Discussions](https://github.com/iOfficeAI/AionUi/discussions) — share ideas and exchange tips
- [Report Issues](https://github.com/iOfficeAI/AionUi/issues) — bugs and feature requests
- [Release Updates](https://github.com/iOfficeAI/AionUi/releases) — get the latest version
- [Discord Community](https://discord.gg/2QAwJn7Egx) — English community
- [WeChat Group](./resources/wx-26.png) — Chinese community

### Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) before opening a PR.

1. Fork this project
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Development Setup

AionUi local development uses two repositories: AionUi for the Electron frontend and AionCore for the local backend. See the [Development Guide](docs/contributing/development.md) for the full macOS, Linux, and Windows setup.

---

## License

This project is licensed under [Apache-2.0](LICENSE).

---

## Contributors

<p align="center">
  <a href="https://github.com/iOfficeAI/AionUi/graphs/contributors">
    <img src="https://contrib.rocks/image?repo=iOfficeAI/AionUi&max=100" alt="Contributors" />
  </a>
</p>

## Star History

<p align="center">
  <a href="https://www.star-history.com/#iOfficeAI/aionui&Date" target="_blank">
    <img src="https://api.star-history.com/svg?repos=iOfficeAI/aionui&type=Date" alt="Star History" width="600">
  </a>
</p>

<div align="center">

**If you like it, give us a star**

[Report Bug](https://github.com/iOfficeAI/AionUi/issues) · [Request Feature](https://github.com/iOfficeAI/AionUi/issues)

</div>

<sub><a href="https://linux.do/">LINUX DO - A New Ideal Community</a></sub>
