# Agent Resume Desktop — User Documentation

Languages: [English](#english) | [简体中文](#简体中文)

macOS-oriented **Session OS + Memory** desktop app: calendar digests, **Agent** Q&A over reports, **Workbench** with embedded terminal, plus **Notes** and **GTD** workflows.

> **No cloud · Local-first**  
> Data is stored under **`~/.agent-resume-panel`** by default (shared with the VS Code extension; change in settings).  
> Digest generation, Agent chat, and semantic search only use a third-party API when you configure one.

---

## English

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

### Related links

- [VS Code extension documentation](https://github.com/lucacicii/agent-resume-panel-doc)

---

## 简体中文

macOS 导向的 **Session OS + Memory** 桌面应用：日历回顾 AI 工作记忆，**Agent** 对报告问答，**Workbench** 恢复会话并嵌入终端，配合 **Notes** 与 **GTD**。

> **无云端 · 纯本机存储**  
> 数据默认在 **`~/.agent-resume-panel`**（与 VS Code 扩展共用，可在设置中修改）。

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

### 相关链接

- [VS Code 扩展用户文档](https://github.com/lucacicii/agent-resume-panel-doc)