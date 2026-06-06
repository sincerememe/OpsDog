# OpsDog

> OpsDog - macOS 服务管理器

## 项目简介

OpsDog 是一个 macOS 原生窗口应用程序，专为开发者打造的高效运维工具。它集成了**终端、编辑器、文件浏览器、服务管理**于一体，最核心的特色是支持通过**自定义快捷按钮**一键管理 AI Agent 命令和各种服务操作。

无需记忆复杂的命令行，只需为常用的 AI Agent 启动、停止、配置等命令配置快捷按钮，即可通过界面按钮快速执行，大幅提升开发效率。无论是管理 Nginx、MySQL、Redis 等传统服务，还是管理各类 AI Agent 服务，如OpenClaw、Claude Code、Hermes等，OpsDog 都能提供可视化的便捷操作体验。

**技术栈：** Tauri 2 + Svelte 5 + xterm.js + Monaco Editor + portable-pty

## 功能特性

### 🖥️ 终端面板

- 💻 **xterm.js 终端** - 美观的终端输出界面
- 🔧 **PTY 伪终端** - 真正的交互式终端，支持 vim、top 等交互式程序
- 📑 **多终端标签页** - 同时打开多个终端会话
- 📜 **命令历史** - 保存最近 100 条命令，支持点击重用
- 🎨 **Tango Dark/Light 主题** - 舒适的配色方案
- ⌨️ **快捷键支持** - Cmd+C 复制、Cmd+V 粘贴
- 🔄 **重启 Shell** - 重新创建终端会话
- 🗑️ **清空终端** - 清除当前输出
- 🌐 **输入法兼容** - 完美支持中文输入法
- 🤖 **内置 AI 助手** - 侧边栏集成 AI 聊天，支持终端输出上下文对话

### 📝 文件编辑器

- 📝 **Monaco Editor** - VS Code 同款编辑器
- 📑 **多标签页** - 同时打开多个文件
- 🎯 **语法高亮** - 支持 20+ 种语言（JSON、XML、YAML、Shell、Python 等）
- 🔢 **行号显示** - 左侧显示行号
- 📂 **代码折叠** - 支持代码块折叠
- 💾 **保存文件** - Ctrl/Cmd + S 保存
- 🔄 **保存并重载** - 保存后自动执行重载命令（如 nginx -s reload）
- 📌 **未保存提示** - 标签页显示修改状态
- 🧹 **JSON 格式化/压缩** - 一键美化或压缩 JSON
- 🧹 **XML 格式化/压缩** - 一键美化或压缩 XML
- ✨ **自动格式化** - 基于语言服务自动格式化代码
- 🎨 **自定义主题** - Tango Dark/Tango Light 主题
- 🤖 **内置 AI 助手** - 侧边栏集成 AI 聊天，支持代码上下文对话

### 🌐 文件浏览器

- 📁 **目录浏览** - 浏览本地文件系统
- 🔍 **路径导航** - 支持路径输入和目录切换
- 🌲 **目录树展开** - 树形结构浏览文件夹
- 👁️ **隐藏文件显示** - 切换显示隐藏文件
- 🔎 **文件过滤** - 按文件类型过滤
- ↕️ **排序功能** - 按名称/类型/大小/时间排序
- ⭐ **收藏夹** - 收藏常用目录
- 📑 **书签系统** - 基于 macOS 书签的安全访问
- 🔋 **右键菜单** - 打开/复制路径/在终端中打开等

### 📄 预览功能

- 📖 **Markdown 预览** - 源码/预览/双栏三种视图
- 📊 **代码高亮** - Markdown 代码块语法高亮
- 📄 **PDF 查看器** - 内置 PDF 渲染，支持缩放和翻页
- 🖼️ **图片查看器** - 支持 JPG、PNG、GIF、SVG、WebP 等格式
- 📊 **Office 文档** - 支持 Word、Excel、PowerPoint 预览
- 🎵 **媒体播放器** - 支持音频和视频播放

### ⚙️ 服务管理

- 📋 **服务列表** - 显示所有配置的服务
- 🟢 **状态指示** - 运行中(绿)/已停止(红)/异常(灰)/未安装四种状态
- 📁 **可折叠展开** - 点击服务头展开/折叠详情
- 🔘 **自定义按钮** - 每个服务可配置多个操作按钮（启动/停止/重启/自定义）
- 📄 **配置文件列表** - 每个服务支持多个配置文件
- ➕ **添加/编辑/删除服务** - 完整的服务管理
- 🔀 **拖拽排序** - 服务拖拽重新排序
- 🔄 **状态自动刷新** - 可配置刷新间隔（默认 5 秒）
- 📊 **进程资源监控** - 实时显示每个服务的 CPU/内存占用
- 🔄 **自动重启** - 服务异常时自动重启，可配置重试次数和间隔
- 🤖 **AI 辅助配置** - 使用 AI 自动生成服务检测、启动、停止等命令
- 📋 **快捷模板** - 内置 Nginx、MySQL、Redis、Docker、OpenClaw 等常用服务模板
- 📥 **导入服务** - 从 JSON 文件导入服务配置
- 📤 **导出服务** - 导出服务配置为 JSON 文件

### 🤖 AI 聊天系统

- 💬 **多会话管理** - 支持创建多个 AI 聊天会话
- 📡 **流式响应** - 实时显示 AI 生成内容
- 🧠 **思考过程** - 支持 AI 推理过程展示（thinking 模式）
- 📝 **Markdown 渲染** - 完整支持 Markdown 语法高亮
- 🧮 **KaTeX 数学公式** - 支持行内和块级数学公式渲染
- 📋 **代码块复制** - 一键复制代码块内容
- 🗑️ **消息管理** - 支持删除单条或批量删除消息
- 🎯 **上下文感知** - 可选择发送全部内容或仅选中内容给 AI
- ⌨️ **快捷键支持** - Enter 发送，Shift+Enter 换行，可选 Cmd+Enter 发送
- 🎨 **侧边栏模式** - 编辑器和终端内置 AI 助手侧边栏
- 🔧 **AI 配置** - 支持自定义大模型接口地址、API 密钥和模型名称

### 🖥️ 系统集成

- 📊 **系统状态监控** - 顶部实时显示 CPU/内存/磁盘占用
- 🚀 **开机启动** - 系统登录时自动启动应用
- ⚡ **启动时执行命令** - 应用启动后自动执行预设命令（如 brew services start nginx）
- 🎨 **深色/浅色主题** - 随时切换主题
- 🌐 **中英文切换** - 支持简体中文和 English
- 📐 **窗口状态持久化** - 记住窗口大小和位置
- 📏 **侧边栏宽度调整** - 拖拽调整侧边栏宽度
- 📝 **日志系统** - 应用运行日志记录
- 🛡️ **单实例运行** - 防止启动多个应用实例

### 🔐 安全与权限

- 🔒 **配置加密** - AES-256 加密存储配置文件
- 🔑 **全磁盘访问检测** - 检测是否获得完整磁盘访问权限
- 📖 **权限引导** - 首次运行引导用户授权
- ⚙️ **系统偏好跳转** - 一键打开隐私设置

## 界面预览

```
┌─────────────────────────────────────────────────────────────────────────┐
│  OpsDog                    CPU 15%  内存 65%  磁盘 45%    🌙 中 ⚙️         │
├────────────────┬────────────────────────────────────────────────────────┤
│  服务清单        │  [Terminal 1] [Terminal 2] [nginx.conf ×]             │
│  ─────────────  │  ────────────────────────────────────────────────────│
│                 │                                                       │
│  🌐 Nginx ●      │  ┌─ Terminal ─────────────────────────────────────┐  │
│    ▼ 配置文件     │  │  $ brew services start nginx                   │  │
│      📄 nginx    │  │  ==> Successfully started...                   │  │
│      📄 conf     │  │  $ _                                           │  │
│    [启动][停止]│  │                                                   │  │
│                  │  └────────────────────────────────────────────────┘  │
│  🐬 MySQL ○      │                                                        │
│    [启动][停止]   │                                                        │
│                  │                                                        │
│  🐳 Docker ●     │                               │
│                  │                                                        │
│  [添加服务]       │                                                        │
│                │                                                        │
└────────────────┴────────────────────────────────────────────────────────┘
```

## 开发环境

### 推荐 IDE

[VS Code](https://code.visualstudio.com/) + [Svelte](https://marketplace.visualstudio.com/items?itemName=svelte.svelte-vscode) + [Tauri](https://marketplace.visualstudio.com/items?itemName=tauri-apps.tauri-vscode) + [rust-analyzer](https://marketplace.visualstudio.com/items?itemName=rust-lang.rust-analyzer)

### 开发命令

```bash
# 安装依赖
pnpm install

# 开发模式
pnpm tauri dev

# 构建
pnpm tauri build

# 类型检查
pnpm check
```

### 环境要求

- macOS 13.0+

## 配置文件格式

配置文件位于 `~/.opsdog/config.dat`（加密存储），JSON 格式如下：

```yaml
# 解密后的配置结构
general:
  autoLaunch: false           # 开机启动
  startupCommands:            # 启动时执行的命令
    - "brew services start nginx"
    - "brew services start mysql"
  theme: "dark"               # 主题 (dark/light)
  refreshInterval: 5          # 服务状态刷新间隔（秒）
  locale: "zh-CN"            # 语言 (zh-CN/en-US)

services:
  - id: "nginx"
    name: "Nginx"
    icon: "🌐"
    detectCommand: "pgrep nginx"
    configFiles:
      - id: "nginx-main"
        name: "nginx.conf"
        path: "/opt/homebrew/etc/nginx/nginx.conf"
        reloadCommand: "nginx -s reload"
    buttons:
      - id: "nginx-start"
        label: "启动"
        command: "brew services start nginx"
      - id: "nginx-stop"
        label: "停止"
        command: "brew services stop nginx"
      - id: "nginx-restart"
        label: "重启"
        command: "brew services restart nginx"

notification:
  enabled: false
ai:
  baseUrl: "https://api.openai.com/v1/chat/completions"
  apiKey: "your-api-key"
  model: "gpt-4o-mini"
```

<div align="center">

**OpsDog** - 让 macOS 服务管理更简单

</div>
