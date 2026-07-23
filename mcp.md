# External Agent MCP

Languages: [English](#english) | [简体中文](#简体中文)

## English

### Overview

Agent Resume Desktop provides one local **Agent Resume MCP** service. It uses stdio, starts only when an MCP client invokes it, and reads the same local data directory as Desktop: `~/.agent-resume-panel` by default.

This is one service with **20 tools**, not 20 independent services:

| Area | Tools | Access |
|---|---:|---|
| Notes and note GTD | 11 | Read and write |
| Reports | 3 | Read-only |
| Sessions | 6 | Read, GTD update, and resume-command generation |

The service does not listen on a network port and does not add an authentication layer. Any client registered on this Mac receives the same access as the local Desktop data store. Register only agents and configurations you trust.

### Register a client

1. Open **Agent Resume → Settings → MCP**.
2. Review the full read/write permission warning.
3. Select **Register detected agents**, or register one client at a time.
4. Restart the external client if it was already running.

Desktop detects and can register these clients automatically:

| Client | Registration |
|---|---|
| Codex | Uses the local `codex mcp` command |
| Claude Code | Uses the local `claude mcp` command with user scope |
| Gemini CLI | Updates its local MCP JSON configuration |
| Antigravity | Updates its local MCP JSON configuration |
| OpenCode | Updates its local MCP JSON configuration |

For **Cursor**, **Pi**, and **Grok Build**, use **Copy config** in the MCP settings page and paste the generated JSON into that client's MCP configuration. Desktop does not guess or overwrite their configuration locations.

Use **Update** after moving or reinstalling Agent Resume. Use **Remove** to remove only the `agent-resume` MCP entry from an automatically managed client.

### Tool reference

#### Notes and note GTD

| Tool | Purpose |
|---|---|
| `note_list` | Page through every indexed note, optionally by scope |
| `note_search` | Search note titles, content, filenames, and paths |
| `note_create` | Create a library, project, or session note |
| `note_read` | Read full Markdown for one note |
| `note_write` | Replace a note's full Markdown content |
| `note_append` | Append Markdown without changing existing content |
| `note_delete` | Permanently delete one note |
| `note_gtd_list` | List `:::gtd` tasks stored in notes |
| `note_gtd_create` | Add a GTD task to a note |
| `note_gtd_update` | Change a GTD task's text or status |
| `note_gtd_delete` | Delete a GTD task from a note |

GTD status values are `inbox`, `next`, `waiting`, `someday`, `reference`, and `done`. When task text is repeated in a note, the agent must use the selected occurrence before an update or delete.

#### Reports

| Tool | Purpose |
|---|---|
| `report_list` | List daily, weekly, or monthly memory digests |
| `report_read` | Read a digest by report ID |
| `report_search` | Search report content, including semantic search when configured |

#### Sessions

| Tool | Purpose |
|---|---|
| `session_list` | List recent sessions with optional filters |
| `session_search` | Find sessions by topic, project, provider, date, or GTD status |
| `session_read` | Read catalog metadata and the session summary |
| `session_read_transcript` | Read a short recent transcript excerpt when a summary is insufficient |
| `session_set_gtd` | Set a session's GTD status in the shared catalog |
| `session_resume` | Return the terminal command for resuming a saved session |

An external MCP invocation cannot open Desktop's Workbench. Therefore, `session_resume` returns the command and project path for the user or agent to run in a terminal.

### Data and safety

- All data remains on the local machine. Configuring an LLM provider is unrelated to MCP registration.
- Notes, GTD tags, session GTD statuses, and the catalog are shared with the VS Code extension.
- `note_delete` and `note_gtd_delete` are destructive. There is no MCP recycle bin or undo operation.
- Removing a client registration does not delete Notes, Reports, Sessions, or GTD data.

## 简体中文

### 概览

Agent Resume Desktop 提供一个本机 **Agent Resume MCP** 服务。它使用 stdio，仅在 MCP 客户端调用时启动，并读取与 Desktop 相同的本机数据目录，默认是 `~/.agent-resume-panel`。

这是一个服务，包含 **20 个工具**，不是 20 个相互独立的服务：

| 范围 | 工具数 | 权限 |
|---|---:|---|
| Notes 与笔记 GTD | 11 | 读写 |
| Reports | 3 | 只读 |
| Sessions | 6 | 读取、更新 GTD、生成恢复命令 |

服务不会监听网络端口，也不会额外增加认证层。本机上注册的任意客户端都会获得访问 Desktop 本机数据的权限，因此只应注册你信任的 Agent 与配置。

### 注册客户端

1. 打开 **Agent Resume → 设置 → MCP**。
2. 阅读完整读写权限提示。
3. 选择 **注册已检测 Agent**，或逐个注册客户端。
4. 如外部客户端已经运行，重启它以加载新配置。

Desktop 可自动检测并注册以下客户端：

| 客户端 | 注册方式 |
|---|---|
| Codex | 使用本机 `codex mcp` 命令 |
| Claude Code | 使用带 user scope 的本机 `claude mcp` 命令 |
| Gemini CLI | 更新本机 MCP JSON 配置 |
| Antigravity | 更新本机 MCP JSON 配置 |
| OpenCode | 更新本机 MCP JSON 配置 |

**Cursor**、**Pi**、**Grok Build** 请在 MCP 设置页选择 **复制配置**，再把生成的 JSON 粘贴到对应客户端的 MCP 配置中。Desktop 不会猜测或覆盖这些客户端的配置路径。

移动或重新安装 Agent Resume 后，可选择 **更新**。选择 **移除** 只会从自动管理的客户端移除 `agent-resume` MCP 条目。

### 工具说明

#### Notes 与笔记 GTD

| 工具 | 用途 |
|---|---|
| `note_list` | 分页列出所有已索引笔记，可按范围筛选 |
| `note_search` | 搜索笔记标题、内容、文件名和路径 |
| `note_create` | 创建库、项目或会话笔记 |
| `note_read` | 读取一篇笔记的完整 Markdown |
| `note_write` | 覆盖一篇笔记的完整 Markdown 内容 |
| `note_append` | 在不修改原有内容的前提下追加 Markdown |
| `note_delete` | 永久删除一篇笔记 |
| `note_gtd_list` | 列出笔记中的 `:::gtd` 任务 |
| `note_gtd_create` | 向笔记添加 GTD 任务 |
| `note_gtd_update` | 修改 GTD 任务的文字或状态 |
| `note_gtd_delete` | 从笔记中删除 GTD 任务 |

GTD 状态为 `inbox`、`next`、`waiting`、`someday`、`reference`、`done`。当同一篇笔记中存在重复任务文字时，Agent 在更新或删除前必须指定用户选中的出现序号。

#### Reports

| 工具 | 用途 |
|---|---|
| `report_list` | 列出日、周、月工作记忆报告 |
| `report_read` | 按 report ID 读取完整报告 |
| `report_search` | 搜索报告内容；配置后也可进行语义搜索 |

#### Sessions

| 工具 | 用途 |
|---|---|
| `session_list` | 按可选条件列出最近会话 |
| `session_search` | 按主题、项目、提供方、日期或 GTD 状态查找会话 |
| `session_read` | 读取 catalog 元数据和会话摘要 |
| `session_read_transcript` | 摘要不足时读取最近一小段转录内容 |
| `session_set_gtd` | 在共享 catalog 中设置会话 GTD 状态 |
| `session_resume` | 返回恢复已保存会话所需的终端命令 |

外部 MCP 调用不能打开 Desktop 的 Workbench，因此 `session_resume` 会返回用户或 Agent 可在终端执行的命令和项目路径。

### 数据与安全

- 所有数据保留在本机。是否配置 LLM 提供方与 MCP 注册无关。
- Notes、GTD 标签、会话 GTD 状态和 catalog 与 VS Code 扩展共用。
- `note_delete` 与 `note_gtd_delete` 属于破坏性操作；MCP 不提供回收站或撤销功能。
- 移除客户端注册不会删除 Notes、Reports、Sessions 或 GTD 数据。
