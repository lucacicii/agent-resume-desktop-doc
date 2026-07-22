# Agent

[← Back to README](README.md)

Languages: [English](#english) | [简体中文](#简体中文)

---

## English

### What it is

The **Agent** tab is Desktop’s **meta-agent**: natural-language Q&A over your **digests and session history** (semantic retrieval when embeddings are configured). It is for recalling and reasoning about past work — not a full IDE replacement for coding agents (use [Workbench](workbench.md) or the VS Code extension for resume / ACP).

### Main workflows

1. Open the **Agent** tab.  
2. Create or select a **thread** (rename / delete as needed).  
3. Ask questions such as “what did I work on last Tuesday?” or “summarize the auth refactor week”.  
4. Watch **streaming** replies; cancel an in-flight ask if needed.  
5. Use citations / linked context when shown to jump back into reports or sessions.  
6. Open **Execution flow** below a reply to review the retrieval, model, and action steps behind it.  
7. Clear a thread’s chat history when you want a clean slate.

### Requirements

- LLM (and optionally **embeddings**) configured under **Settings → Models**.  
- Useful digests in [Report](report.md) improve answer quality for calendar-style questions.  
- Without embeddings, retrieval quality may be limited to keyword / digest-level context depending on configuration.

### Execution flow and approvals

- The execution-flow summary separates **context retrieval**, **LLM requests**, and actual **tool actions**. A report, note, or session citation comes from retrieval; it is not itself a tool call.
- Open the right-side flow panel to inspect each step. Inputs and outputs are collapsed by default; MCP actions also show their source and risk level.
- Read-only actions proceed automatically. Write, launch, command, and network actions request approval by default. Delete and unknown-risk actions always request approval.
- In **Settings → General → Agent actions**, **Always allow non-delete Agent actions** skips approval for classified non-delete actions. Use it only when you trust the configured model and tools.

### Privacy

- Agent Q&A **sends retrieved local content and your prompts** to the third-party API you configure.  
- Do not ask questions that force secrets into the prompt if the endpoint is untrusted.  
- Chat threads and execution-flow records are stored locally under panel home / desktop data. Recorded tool inputs and outputs are redacted for common secret fields and limited in length.

### Tips

1. Prefer concrete time ranges and project names in questions.  
2. Generate or refresh relevant digests first for better recall.  
3. Keep separate threads per topic (weekly review vs. one project).  
4. Usage of LLM calls appears under **Settings → Usage**.

### Related

- [Report](report.md) · [Sessions](sessions.md) · [Settings & data](settings-and-data.md)  
- Extension-side assist (summarize / rename / handoff): [panel-doc LLM Assist](https://github.com/lucacicii/agent-resume-panel-doc/blob/main/llm-assist.md)

---

## 简体中文

### 是什么

**Agent** 页签是 Desktop 的 **元 Agent**：用自然语言对 **回顾报告与会话历史** 提问（配置 embeddings 时支持语义检索）。适合回忆与梳理过往工作，而不是完整替代写代码的 Agent（恢复会话请用 [Workbench](workbench.md) 或 VS Code 扩展 / ACP）。

### 主要流程

1. 打开 **Agent** 页签。  
2. 新建或选择 **线程**（可重命名 / 删除）。  
3. 提问，例如「上周二我在做什么」或「总结鉴权重构那一周」。  
4. 查看 **流式** 回答；需要时可取消进行中的提问。  
5. 有引用 / 关联上下文时，可跳回报告或会话。  
6. 点击回答下方的 **执行流程**，查看检索、模型与操作步骤。  
7. 需要干净上下文时可清空该线程聊天记录。

### 前提

- 在 **Settings → 模型** 配置 LLM（可选 **embeddings**）。  
- [Report](report.md) 中有相关回顾时，日历类问题效果更好。  
- 未配置 embeddings 时，检索可能偏关键词 / 报告级上下文（视配置而定）。

### 执行流程与授权

- 执行流程会分别统计 **上下文检索**、**LLM 请求** 与实际的 **工具操作**。报告、笔记、会话引用来自检索，本身不算工具调用。
- 打开右侧执行流程面板可查看每个步骤；输入和输出默认折叠，MCP 操作还会显示来源和风险级别。
- 只读操作自动执行。写入、启动、命令和网络操作默认请求授权；删除和未知风险操作始终请求授权。
- 在 **设置 → 通用 → Agent 操作** 中开启 **始终允许非删除 Agent 操作** 后，已分类的非删除操作会跳过授权。仅在信任当前模型与工具时开启。

### 隐私

- Agent 问答会把 **检索到的本机内容与你的提示** 发往配置的第三方 API。  
- 端点不可信时，避免在问题中带入密钥等敏感信息。  
- 线程与执行流程记录保存在本机面板 / Desktop 数据目录。记录的工具输入与输出会对常见密钥字段脱敏，并限制长度。

### 提示

1. 问题尽量带上时间范围与项目名。  
2. 先生成或刷新相关回顾，回忆更准。  
3. 按主题分线程（周回顾 vs 单项目）。  
4. LLM 用量见 **Settings → 用量**。

### 相关文档

- [Report](report.md) · [Sessions](sessions.md) · [设置与数据](settings-and-data.md)  
- 扩展侧辅助（摘要 / 重命名 / Handoff）：[panel-doc LLM 辅助](https://github.com/lucacicii/agent-resume-panel-doc/blob/main/llm-assist.md)
