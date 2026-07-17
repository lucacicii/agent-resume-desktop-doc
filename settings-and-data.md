# Settings & data

[← Back to README](README.md)

Languages: [English](#english) | [简体中文](#简体中文)

---

## English

### Open settings

Use the **⚙** button in the top bar. Settings panes:

| Pane | Typical contents |
|------|------------------|
| **General** | Language, historical backfill, startup-related options |
| **Models** | OpenAI-compatible LLM / embeddings endpoints and models |
| **Sessions** | Agent home paths, session list / sync related options |
| **Workbench** | Default agent, ⌘T behavior, terminal-related defaults |
| **Report** | Digest / memory related preferences |
| **Data** | Panel home path, open data folder, storage-oriented actions |
| **Usage** | Local LLM usage summary |
| **About** | Version, update check entry |

Desktop settings are **not** VS Code `agentResume.*` settings. Shared values (e.g. LLM) may live in panel-home files so both products can reuse them; Desktop also keeps desktop-specific config (e.g. under panel home / `.desktop`).

### Panel home (shared)

Default:

```text
~/.agent-resume-panel
```

| Content | Role |
|---------|------|
| `catalog.db` | Session index, GTD, note flags (shared) |
| Notes + assets | Shared Markdown notes |
| Shared settings files | e.g. LLM-related `settings.json` where applicable |
| `.desktop/` | Desktop-only extras (scheduler state, desktop schema, etc.) |

CLI transcripts remain in native agent homes. Change panel home only if you understand both products will need the same path to stay in sync.

### Updates

- In-app **version check** / update entry (About or update icon when available).  
- Download new DMGs from [Releases](https://github.com/lucacicii/agent-resume-desktop-doc/releases).  
- First-launch Gatekeeper steps: see [README install](README.md).

### Backup

1. Copy **`~/.agent-resume-panel`** (or custom panel home), including `.desktop`.  
2. Copy native agent homes for full transcripts.  
3. Reinstall the app from the DMG on a new machine, then restore the folder before first heavy sync if possible.

### Privacy

- Digests, Agent Q&A, embeddings, and assist features contact **your** configured third-party APIs only when used.  
- Never commit API keys; do not paste them into GitHub issues.

### Feedback

- [desktop-doc Issues](https://github.com/lucacicii/agent-resume-desktop-doc/issues)  
- [Changelog](CHANGELOG.md)

### Related

- [Report](report.md) · [Agent](agent.md) · [Workbench](workbench.md) · [Notes](notes.md)  
- Extension settings: [panel-doc Settings](https://github.com/lucacicii/agent-resume-panel-doc/blob/main/settings-and-data.md)

---

## 简体中文

### 打开设置

点击顶部栏 **⚙**。各页大致内容：

| 页 | 常见内容 |
|----|----------|
| **通用** | 语言、历史回填、启动相关 |
| **模型** | OpenAI 兼容 LLM / embeddings 端点与模型 |
| **Sessions** | 各 Agent 目录、会话列表 / 同步相关 |
| **Workbench** | 默认 Agent、⌘T 行为、终端相关默认 |
| **Report** | 回顾 / Memory 相关偏好 |
| **数据** | Panel home 路径、打开数据目录等 |
| **用量** | 本机 LLM 用量汇总 |
| **关于** | 版本、更新检查入口 |

Desktop 设置 **不是** VS Code 的 `agentResume.*`。可共用的值（如 LLM）可能写在 panel home 文件中供两产品复用；Desktop 另有桌面端专用配置（如 `.desktop`）。

### 数据目录（共用）

默认：

```text
~/.agent-resume-panel
```

| 内容 | 作用 |
|------|------|
| `catalog.db` | 会话索引、GTD、笔记标记（共用） |
| 笔记 + 资源 | 共用 Markdown |
| 共用设置文件 | 如 LLM 相关 `settings.json` |
| `.desktop/` | 仅 Desktop（调度、桌面 schema 等） |

CLI 原文仍在各 Agent 原生目录。修改 panel home 时请确保两产品使用同一路径以保持同步。

### 更新

- 应用内 **版本检查** / 更新入口（关于页或更新图标）。  
- 也可从 [Releases](https://github.com/lucacicii/agent-resume-desktop-doc/releases) 下载新 DMG。  
- 首次启动系统拦截步骤见 [README 安装](README.md)。

### 备份

1. 备份 **`~/.agent-resume-panel`**（含 `.desktop`）。  
2. 备份原生 Agent 目录以保留完整对话。  
3. 新机器安装 DMG 后，尽量在大量同步前恢复该目录。

### 隐私

- 报告生成、Agent 问答、embeddings 等仅在使用时访问 **你配置的** 第三方 API。  
- 勿将 API Key 提交进仓库或贴进 Issue。

### 反馈

- [desktop-doc Issues](https://github.com/lucacicii/agent-resume-desktop-doc/issues)  
- [更新日志](CHANGELOG.md)

### 相关文档

- [Report](report.md) · [Agent](agent.md) · [Workbench](workbench.md) · [Notes](notes.md)  
- 扩展设置：[panel-doc 设置](https://github.com/lucacicii/agent-resume-panel-doc/blob/main/settings-and-data.md)
