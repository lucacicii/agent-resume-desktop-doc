# Changelog

Languages: [简体中文](#简体中文) | [English](#english)

本文件记录 **Agent Resume Desktop**（macOS）版本变更，格式参考 [Keep a Changelog](https://keepachangelog.com/zh-CN/1.1.0/)。

This file tracks **Agent Resume Desktop** (macOS) releases and follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

下载安装包与单版说明另见 [Releases](https://github.com/lucacicii/agent-resume-desktop-doc/releases)。

## 简体中文

### [0.1.2]

#### 新增

- **完整三语界面**：桌面端英文、简体中文、日文翻译已补全。
- **独立桌面语言包**：桌面端 locale 与 VS Code 扩展分离，仅包含 `desktop.*` 键。

#### 改进

- **语言覆盖检查**：新增翻译完整性校验脚本。
- **日文 locale 流水线**：桌面端日文由 catalog 直接生成，不再回退英文。

#### 修复

- **macOS 打包**：修复重复打包时 electron 符号链接冲突。

### [0.1.1]

#### 修复

- **首次打开不再误报 Agent 目录错误**：新用户未安装 Claude / Grok / Pi 等 CLI 时，同步会静默跳过缺失的默认数据目录，不再在启动时刷一整屏 “data directory not found”。
- **默认路径不再写入设置**：保存设置时不再把 `~/.claude` 等默认值当成自定义路径持久化，避免之后持续报错。
- **跨账号绝对路径**：从其他 macOS 用户目录复制的绝对路径会自动 remap 到当前用户 home（例如 `/Users/other/.claude` → `~/.claude`）。
- **启动同步状态栏**：首次同步显示已同步 session 数量，不再把后台 warning 当成红色错误展示。

### [0.1.0]

#### 新增

- **Report** — 日历、日/周/月报、GTD 条、当日详情
- **Agent** — 基于报告的自然语言问答
- **Workbench** — 会话列表，嵌入式或外部终端恢复
- **Sessions** — 参考列表与只读预览
- **Notes** — Markdown 笔记编辑
- **Settings** — 通用、模型、Sessions、Workbench、Memory、数据、用量

#### 数据

- 与 VS Code 扩展共用默认数据目录：`~/.agent-resume-panel`。

#### 要求

- macOS 12 或更高版本
- Apple Silicon 或 Intel（通用包）
- 本构建为 ad-hoc 签名，未经 Apple 公证

## English

### [0.1.2]

#### Added

- **Full trilingual UI**: complete English, Simplified Chinese, and Japanese translations for the desktop app.
- **Dedicated desktop locales**: desktop strings are separated from the VS Code extension and scoped to `desktop.*` keys.

#### Improved

- **Translation coverage checks**: new script to detect untranslated strings.
- **Japanese locale pipeline**: desktop Japanese is generated from the catalog instead of falling back to English.

#### Fixed

- **macOS packaging**: fixed electron symlink `EEXIST` error on repeated `pack:mac` runs.

### [0.1.1]

#### Fixed

- **No false agent-directory errors on first launch**: when Claude / Grok / Pi CLIs are not installed, sync quietly skips missing default data directories instead of flooding the UI with “data directory not found”.
- **Default paths are no longer persisted as custom settings**: saving settings no longer writes `~/.claude` and other defaults into `agentHomes`, which previously caused repeat errors.
- **Foreign-user absolute paths**: absolute paths copied from another macOS account are remapped to the current user home (e.g. `/Users/other/.claude` → `~/.claude`).
- **Startup sync status bar**: first sync shows the synced session count instead of treating background warnings as red errors.

### [0.1.0]

#### Added

- **Report** — Calendar, daily/weekly/monthly digests, GTD bar, day detail
- **Agent** — Natural-language Q&A over your digests
- **Workbench** — Session list with embedded or external terminal resume
- **Sessions** — Reference list and read-only preview
- **Notes** — Markdown note editor
- **Settings** — General, models, sessions, workbench, memory, data, usage

#### Data

- Shares the default data directory with the VS Code extension: `~/.agent-resume-panel`.

#### Requirements

- macOS 12 or later
- Apple Silicon or Intel (universal build)
- Ad-hoc signed; not notarized by Apple