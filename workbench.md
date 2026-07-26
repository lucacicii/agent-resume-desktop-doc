# Workbench

[← Back to README](README.md)

Languages: [English](#english) | [简体中文](#简体中文)

---

## English

### What it is

**Workbench** is Desktop’s **session OS** surface: pick or create sessions, resume in an **embedded xterm** or the **system default terminal**, and use **Git / explorer** tools in a side panel. It is the primary place to *continue working*, while [Sessions](sessions.md) is a lighter reference list.

### Core flows

1. Open the **Workbench** tab.  
2. Browse the session list; create a new session if needed (default agent: **Settings → Workbench**).  
3. Resume in the **embedded terminal** (multi-tab) or launch an **external** terminal.  
4. Use the detail header for project path and **branch** controls; the status bar still shows live **cwd** (including nested repos when detected).  
5. Open **Search** or **Scripts** from the detail toolbar, or expand scripts under **Explorer**.  
6. In **Git**, select specific changed files before commit when you do not want to commit everything.

### Side panel

| Tool | Purpose |
|------|---------|
| **Explorer** | Browse project files; shows Git tracking / change hints when available |
| **Search** | Find text in the selected project (match case, whole word, regex); open hits in the file editor |
| **Scripts** | Discover and run project scripts (npm / pnpm / yarn / bun, Make, Gradle, Python, Cargo) into the active terminal |
| **Nested git scan** | Discover git repos under the project tree |
| **Git changes** | Stage/select files, commit only selected paths, push / pull, and inspect diffs |
| **Git log graph** | Branch graph and commit node details in the side panel |

### Keyboard & defaults

- **⌘T** can be configured for **new session** or **new terminal** under Workbench settings.  
- Default agent for new sessions is set in **Settings → Workbench**.

### Tips

1. Prefer embedded terminal when you want multi-tab continuity inside Desktop.  
2. Pick a **Terminal theme** under **Settings → Workbench** (Default Dark/Light, Solarized, One Dark, Dracula); open tabs update immediately.  
3. Use external terminal if you rely on a custom shell / terminal app workflow.  
4. Closing a terminal/editor tab focuses the most recently used panel.  
5. Terminal features depend on a healthy PTY host; other Desktop tabs still work if the terminal subsystem fails to load.

### Related

- [Sessions](sessions.md) · [Report](report.md) · [Settings & data](settings-and-data.md)  
- Extension resume targets (Ghostty, IDE panels): [panel-doc Resume](https://github.com/lucacicii/agent-resume-panel-doc/blob/main/resume-and-targets.md)

---

## 简体中文

### 是什么

**Workbench** 是 Desktop 的 **Session OS** 工作台：选择或新建会话，在 **内嵌 xterm** 或 **系统默认终端** 中恢复，并使用侧边栏 **Git / 资源管理器**。这里是 *继续干活* 的主战场；[Sessions](sessions.md) 更偏参考列表。

### 核心流程

1. 打开 **Workbench** 页签。  
2. 浏览会话列表；需要时新建会话（默认 Agent：**Settings → Workbench**）。  
3. 用 **内嵌终端**（多标签）恢复，或启动 **外部终端**。  
4. 在详情头查看项目路径与 **分支** 控件；状态栏仍显示实时 **cwd**（可识别嵌套仓库）。  
5. 从详情工具栏打开 **Search** 或 **Scripts**，也可在 **Explorer** 下展开脚本区。  
6. 在 **Git** 中可先勾选变更文件再提交，不必一次提交全部改动。

### 侧边栏

| 工具 | 作用 |
|------|------|
| **Explorer** | 浏览项目文件；可显示 Git 跟踪 / 变更提示 |
| **Search** | 在当前项目中检索文本（大小写 / 整词 / 正则），点击结果在编辑器中打开 |
| **Scripts** | 发现并运行项目脚本（npm / pnpm / yarn / bun、Make、Gradle、Python、Cargo），写入当前终端 |
| **嵌套 Git 扫描** | 发现项目树下的 git 仓库 |
| **Git 变更** | 勾选文件、仅提交选中路径、push / pull 与 diff 查看 |
| **Git Log 图** | 侧边栏分支图与提交节点信息 |

### 快捷键与默认值

- **⌘T** 可在 Workbench 设置中配置为 **新建会话** 或 **新建终端**。  
- 新建会话的默认 Agent 在 **Settings → Workbench**。

### 提示

1. 希望在 Desktop 内多标签连续工作时，优先用内嵌终端。  
2. 在 **设置 → Workbench** 选择 **终端主题**（Default Dark/Light、Solarized、One Dark、Dracula）；已打开标签即时生效。  
3. 依赖自定义 shell / 终端 App 时用外部终端。  
4. 关闭终端 / 编辑器标签后会激活最近使用的面板。  
5. 终端依赖 PTY；若终端子系统加载失败，其它页签仍可使用。

### 相关文档

- [Sessions](sessions.md) · [Report](report.md) · [设置与数据](settings-and-data.md)  
- 扩展恢复目标（Ghostty、IDE 面板）：[panel-doc 恢复](https://github.com/lucacicii/agent-resume-panel-doc/blob/main/resume-and-targets.md)
