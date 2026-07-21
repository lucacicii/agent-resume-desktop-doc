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
4. Watch the **status bar** for live **cwd** and **git branch** (including nested repos when detected).  
5. Click the status bar branch to switch branches when Git IPC is available.

### Side panel

| Tool | Purpose |
|------|---------|
| **Explorer** | Browse project files linked to the session / workspace |
| **Nested git scan** | Discover git repos under the project tree |
| **Git log graph** | Branch graph and commit node details in the side panel |
| **Git actions** | Common side-panel git operations tied to the project |

### Keyboard & defaults

- **⌘T** can be configured for **new session** or **new terminal** under Workbench settings.  
- Default agent for new sessions is set in **Settings → Workbench**.

### Tips

1. Prefer embedded terminal when you want multi-tab continuity inside Desktop.  
2. Use external terminal if you rely on a custom shell / terminal app workflow.  
3. Project path appears in the workbench detail header for orientation.  
4. Terminal features depend on a healthy PTY host; other Desktop tabs still work if the terminal subsystem fails to load.

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
4. 在 **状态栏** 查看实时 **cwd** 与 **git 分支**（可识别嵌套仓库）。  
5. 在 Git IPC 可用时，点击状态栏分支切换分支。

### 侧边栏

| 工具 | 作用 |
|------|------|
| **Explorer** | 浏览与会话 / 项目关联的文件 |
| **嵌套 Git 扫描** | 发现项目树下的 git 仓库 |
| **Git Log 图** | 侧边栏分支图与提交节点信息 |
| **Git 操作** | 与项目关联的常见侧边栏 Git 操作 |

### 快捷键与默认值

- **⌘T** 可在 Workbench 设置中配置为 **新建会话** 或 **新建终端**。  
- 新建会话的默认 Agent 在 **Settings → Workbench**。

### 提示

1. 希望在 Desktop 内多标签连续工作时，优先用内嵌终端。  
2. 依赖自定义 shell / 终端 App 时用外部终端。  
3. 详情头会显示项目路径，便于定位。  
4. 终端依赖 PTY；若终端子系统加载失败，其它页签仍可使用。

### 相关文档

- [Sessions](sessions.md) · [Report](report.md) · [设置与数据](settings-and-data.md)  
- 扩展恢复目标（Ghostty、IDE 面板）：[panel-doc 恢复](https://github.com/lucacicii/agent-resume-panel-doc/blob/main/resume-and-targets.md)
