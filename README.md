# Agent Resume Desktop — 用户文档

Languages: [简体中文](#简体中文) | [English](#english)

macOS 导向的 **Session OS + Memory** 桌面应用：在日历上回顾 AI 工作记忆，用 **Agent** 对 digest 自然语言问答，在 **Workbench** 中恢复会话并嵌入终端，配合 **Notes** 与 **GTD** 工作流。

> **无云端 · 纯本机存储（Local-first）**  
> 数据默认存放在 **`~/.agent-resume-panel`**（与 VS Code 扩展共享 `panelHome`）。  
> Digest 生成、Ask 聊天、Embedding 等仅在配置 LLM API 时才会访问第三方服务。

---

## 简体中文

### 导航

| 入口 | 作用 |
|------|------|
| **Report**（默认） | 日历 · 日/周/月报 · GTD 条 · 当日详情 |
| **Agent** | 基于 digest 的自然语言问答 |
| **Workbench** | 会话列表 + 嵌入式终端 / 外部终端恢复 |
| **Sessions** | 参考列表 + 只读预览 |
| **Notes** | Markdown 笔记编辑 |
| **⚙ Settings** | 通用 / 模型 / Sessions / Workbench / Memory / 数据 / 用量 |

### Report 与 GTD

1. 在右侧生成 **日 / 周 / 月报**（点击日历可同步日报日期）。
2. 使用 **从周报/月报分析 GTD + todolist** 打开可编辑预览。
3. 确认后应用 → 写入 `session_gtd` 与 `todolist.md`。

批量回填历史 digest：Settings → 通用。

### Workbench

- 新建 Session（默认 Agent 可在 Settings → Workbench 配置）。
- 嵌入式 xterm 或系统默认终端恢复会话。
- ⌘T 快捷键可配置为新建 Session 或新建终端。

### 数据目录

```text
~/.agent-resume-panel/
  catalog.db
  notes/
  .desktop/desktop.db
```

### 反馈与支持

- **Bug 报告 / 功能建议**：[GitHub Issues](https://github.com/lucacicii/agent-resume-desktop-doc/issues)
- 提交 Issue 时请勿粘贴 API Key、完整对话 transcript 或敏感路径。

### 相关链接

- [VS Code 扩展用户文档](https://github.com/lucacicii/agent-resume-panel-doc)
- [源代码仓库](https://github.com/lucacicii/agent-resume-panel)

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
3. Apply selected items to `session_gtd` and `todolist.md`.

Historical backfill: Settings → General.

### Workbench

Create sessions, resume in embedded xterm or system terminal. Configure default agent and ⌘T behavior in Settings → Workbench.

### Data storage

Local-first under `~/.agent-resume-panel` (shared `panelHome` with the VS Code extension).

### Feedback & support

- **Bugs / feature requests**: [GitHub Issues](https://github.com/lucacicii/agent-resume-desktop-doc/issues)
- Do not paste API keys, full transcripts, or sensitive paths in issues.

### Related links

- [VS Code extension documentation](https://github.com/lucacicii/agent-resume-panel-doc)
- [Source repository](https://github.com/lucacicii/agent-resume-panel)

---

## License

MIT — see [LICENSE](LICENSE).