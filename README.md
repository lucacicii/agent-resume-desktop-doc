# Agent Resume Desktop — User Documentation

Languages: [English](#english) | [简体中文](#简体中文)

macOS-oriented **Session OS + Memory** desktop app: calendar digests, **Agent** Q&A over reports, **Workbench** with embedded terminal, plus **Notes** and **GTD** workflows.

Pairs with the **Agent Resume Panel VS Code extension** — same agent sessions, same `~/.agent-resume-panel` data directory, no duplicate setup.

| | Desktop app (macOS) | VS Code extension |
|---|---|---|
| **Install** | [Download DMG](https://github.com/lucacicii/agent-resume-desktop-doc/releases/latest) | [Marketplace](https://marketplace.visualstudio.com/items?itemName=lucacicii.agent-resume-panel-v2) |
| **Docs** | This repo | [panel-doc](https://github.com/lucacicii/agent-resume-panel-doc) |

Desktop version: see [releases](https://github.com/lucacicii/agent-resume-desktop-doc/releases) · Extension: **2.6.6**

> **No cloud · Local-first**  
> Data is stored under **`~/.agent-resume-panel`** by default (shared with the VS Code extension; change in settings).  
> Digest generation, Agent chat, and semantic search only use a third-party API when you configure one.

---

## English

### Download

- **macOS** (Apple Silicon + Intel universal): [Latest release](https://github.com/lucacicii/agent-resume-desktop-doc/releases/latest)
- Open the DMG and drag **Agent Resume** into **Applications**.
- **First launch:** macOS may block the app because it is not notarized. Right-click the app → **Open** once, or run:

  ```bash
  xattr -cr "/Applications/Agent Resume.app"
  ```

Older versions and release notes: [All releases](https://github.com/lucacicii/agent-resume-desktop-doc/releases).

### Navigation

| Entry | Role |
|-------|------|
| **Report** (default) | Calendar · daily/weekly/monthly digests · GTD bar · day detail |
| **Agent** | Natural-language Q&A over digests |
| **Workbench** | Session list + embedded or external terminal resume |
| **Sessions** | Reference list + read-only preview |
| **Notes** | Markdown note editor |
| **⚙ Settings** | General, models, sessions, workbench, memory, data, usage |

### Report & GTD

1. Generate **daily / weekly / monthly** digests from the right panel (click the calendar to sync the daily date).
2. Use **Analyze GTD + todolist from weekly/monthly reports** to open an editable preview.
3. Apply selected items to update session GTD labels and project task lists.

Historical backfill: **Settings → General**.

### Workbench

- Create sessions (default agent: **Settings → Workbench**).
- Resume in embedded terminal or system default terminal.
- **⌘T** can be configured for new session or new terminal.

### Data & backup

Data lives under **`~/.agent-resume-panel`**: session index, notes, reports, and desktop settings. Back up this folder when moving machines.

### Feedback & support

- **Bugs / feature requests**: [GitHub Issues](https://github.com/lucacicii/agent-resume-desktop-doc/issues)
- Do not paste API keys, full transcripts, or sensitive paths in issues.

### VS Code extension vs Desktop

| | **Agent Resume Desktop** | **VS Code extension** |
|---|---|---|
| **What it is** | Standalone macOS app — **Session OS + Memory** | Sidebar panel inside VS Code / Cursor / VSCodium |
| **Best for** | Calendar digests, **Agent** Q&A over work history, embedded **Workbench** | Resume while coding; **ACP Chat** beside the editor; GTD / Notes in the IDE |
| **Desktop-only** | Daily / weekly / monthly digests; semantic recall over reports; xterm Workbench | — |
| **Extension-only** | — | ACP Chat; Claude / Codex IDE panel resume; Ghostty / Alma targets |

**Shared:** `catalog.db`, GTD tags, Notes, LLM settings (`settings.json`). Desktop extras live under `panelHome/.desktop/`.

[Download Desktop](https://github.com/lucacicii/agent-resume-desktop-doc/releases/latest) · [Install extension](https://marketplace.visualstudio.com/items?itemName=lucacicii.agent-resume-panel-v2) · [Extension docs](https://github.com/lucacicii/agent-resume-panel-doc)

### Related links

- [VS Code extension documentation](https://github.com/lucacicii/agent-resume-panel-doc)
- [Install VS Code extension](https://marketplace.visualstudio.com/items?itemName=lucacicii.agent-resume-panel-v2)

---

## 简体中文

macOS 导向的 **Session OS + Memory** 桌面应用：日历回顾 AI 工作记忆，**Agent** 对报告问答，**Workbench** 恢复会话并嵌入终端，配合 **Notes** 与 **GTD**。

与 **Agent Resume Panel VS Code 扩展** 搭配使用 — 同一批 Agent 会话、共用 **`~/.agent-resume-panel`**，无需重复配置。

| | Desktop 桌面端（macOS） | VS Code 扩展 |
|---|---|---|
| **安装** | [下载 DMG](https://github.com/lucacicii/agent-resume-desktop-doc/releases/latest) | [Marketplace](https://marketplace.visualstudio.com/items?itemName=lucacicii.agent-resume-panel-v2) |
| **文档** | 本仓库 | [panel-doc](https://github.com/lucacicii/agent-resume-panel-doc) |

桌面端版本见 [Releases](https://github.com/lucacicii/agent-resume-desktop-doc/releases) · 扩展：**2.6.6**

> **无云端 · 纯本机存储**  
> 数据默认在 **`~/.agent-resume-panel`**（与 VS Code 扩展共用，可在设置中修改）。

### 下载安装

- **macOS**（Apple Silicon + Intel 通用包）：[最新版本](https://github.com/lucacicii/agent-resume-desktop-doc/releases/latest)
- 打开 DMG，将 **Agent Resume** 拖入 **应用程序**。
- **首次打开：** 应用未经 Apple 公证，macOS 可能拦截。请右键应用 → **打开** 一次，或执行：

  ```bash
  xattr -cr "/Applications/Agent Resume.app"
  ```

历史版本与更新说明：[全部 Releases](https://github.com/lucacicii/agent-resume-desktop-doc/releases)。

### 导航

| 入口 | 作用 |
|------|------|
| **Report**（默认） | 日历 · 日/周/月报 · GTD 条 · 当日详情 |
| **Agent** | 基于报告的自然语言问答 |
| **Workbench** | 会话列表 + 嵌入式 / 外部终端恢复 |
| **Sessions** | 参考列表 + 只读预览 |
| **Notes** | Markdown 笔记编辑 |
| **⚙ Settings** | 通用 / 模型 / Sessions / Workbench / Memory / 数据 / 用量 |

### Report 与 GTD

1. 右侧生成 **日 / 周 / 月报**（点击日历同步日报日期）。
2. **从周报/月报分析 GTD + todolist** 打开可编辑预览。
3. 确认后应用 → 更新 GTD 标记与项目待办。

历史回填：**Settings → 通用**。

### Workbench

新建 Session、嵌入式或系统终端恢复；**⌘T** 与默认 Agent 在 **Settings → Workbench** 配置。

### 数据与备份

数据在 **`~/.agent-resume-panel`**，换机请自行备份该目录。

### 反馈与支持

- [GitHub Issues](https://github.com/lucacicii/agent-resume-desktop-doc/issues)
- 请勿粘贴 API Key、完整对话内容或敏感路径。

### VS Code 扩展 vs Desktop

| | **Agent Resume Desktop** | **VS Code 扩展** |
|---|---|---|
| **定位** | 独立 macOS 应用 — **Session OS + Memory** | VS Code / Cursor / VSCodium 侧边栏面板 |
| **适合场景** | 日历日报、对报告 **Agent** 问答、内嵌 **Workbench** | 写代码时恢复会话；编辑器旁 **ACP Chat**；IDE 内 GTD / 笔记 |
| **仅 Desktop** | 日 / 周 / 月 Digest；基于报告的语义回忆；xterm Workbench | — |
| **仅扩展** | — | ACP Chat；Claude / Codex 插件面板恢复；Ghostty / Alma |

**共用：** `catalog.db`、GTD、Notes、LLM 设置（`settings.json`）。Desktop 私有数据在 `panelHome/.desktop/`。

[下载 Desktop](https://github.com/lucacicii/agent-resume-desktop-doc/releases/latest) · [安装扩展](https://marketplace.visualstudio.com/items?itemName=lucacicii.agent-resume-panel-v2) · [扩展文档](https://github.com/lucacicii/agent-resume-panel-doc)

### 相关链接

- [VS Code 扩展用户文档](https://github.com/lucacicii/agent-resume-panel-doc)
- [安装 VS Code 扩展](https://marketplace.visualstudio.com/items?itemName=lucacicii.agent-resume-panel-v2)