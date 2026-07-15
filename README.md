# Agent Resume Desktop — 用户文档

Languages: [简体中文](#简体中文) | [English](#english)

macOS 导向的 **Session OS + Memory** 桌面应用：在日历上回顾 AI 工作记忆，用 **Agent** 对报告进行自然语言问答，在 **Workbench** 中恢复会话并嵌入终端，配合 **Notes** 与 **GTD** 工作流。

> **无云端 · 纯本机存储（Local-first）**  
> 数据默认存放在 **`~/.agent-resume-panel`**（与 VS Code 扩展共用数据目录，可在设置中修改）。  
> 日报 / 周报 / 月报、Agent 问答、语义搜索等仅在配置 LLM API 时才会访问第三方服务。

---

## 简体中文

### 导航

| 入口 | 作用 |
|------|------|
| **Report**（默认） | 日历 · 日/周/月报 · GTD 条 · 当日详情 |
| **Agent** | 基于报告内容的自然语言问答 |
| **Workbench** | 会话列表 + 嵌入式终端 / 外部终端恢复 |
| **Sessions** | 参考列表 + 只读预览 |
| **Notes** | Markdown 笔记编辑 |
| **⚙ Settings** | 通用 / 模型 / Sessions / Workbench / Memory / 数据 / 用量 |

### Report 与 GTD

1. 在右侧生成 **日 / 周 / 月报**（点击日历可同步日报日期）。
2. 使用 **从周报/月报分析 GTD + todolist** 打开可编辑预览。
3. 确认后应用 → 更新会话 GTD 标记与项目待办清单。

历史报告较少时，可在 **Settings → 通用** 中批量回填。

### Workbench

- 新建 Session（默认 Agent 可在 **Settings → Workbench** 配置）。
- 嵌入式终端或系统默认终端恢复会话。
- **⌘T** 可配置为新建 Session 或新建终端。

### 数据与备份

数据默认保存在 **`~/.agent-resume-panel`**，包括会话索引、笔记、报告与桌面应用配置。换机时请自行备份该目录。

### 反馈与支持

- **Bug 报告 / 功能建议**：[GitHub Issues](https://github.com/lucacicii/agent-resume-desktop-doc/issues)
- 提交 Issue 时请勿粘贴 API Key、完整对话内容或敏感路径。

### 相关链接

- [VS Code 扩展用户文档](https://github.com/lucacicii/agent-resume-panel-doc)

---

## English

### Overview

macOS-oriented desktop app for session memory: calendar digests, Agent Q&A, Workbench with embedded terminal, Notes, and GTD workflows.

### Navigation

| Entry | Role |
|-------|------|
| **Report** | Calendar, daily/weekly/monthly digests, GTD bar |
| **Agent** | Natural-language Q&A over digests |
| **Workbench** | Session list + embedded or external terminal resume |
| **Sessions** | Reference list + read-only preview |
| **Notes** | Markdown note editor |
| **⚙ Settings** | General, models, sessions, workbench, memory, data, usage |

### Report & GTD

1. Generate daily / weekly / monthly digests from the right panel.
2. Run GTD analysis from weekly/monthly reports; preview before applying.
3. Apply selected items to update session GTD labels and project task lists.

Historical backfill: **Settings → General**.

### Workbench

Create sessions, resume in embedded or system terminal. Configure default agent and **⌘T** in **Settings → Workbench**.

### Data & backup

Data is stored locally under **`~/.agent-resume-panel`** (shared with the VS Code extension). Back up this folder when moving machines.

### Feedback & support

- **Bugs / feature requests**: [GitHub Issues](https://github.com/lucacicii/agent-resume-desktop-doc/issues)
- Do not paste API keys, full transcripts, or sensitive paths in issues.

### Related links

- [VS Code extension documentation](https://github.com/lucacicii/agent-resume-panel-doc)