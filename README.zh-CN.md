# AgentsMD Kit

面向 coding agent 项目的 `AGENTS.md` 起步套件。

这个仓库只放项目级 agent 规则和轻量任务记忆，不再混入 Multi-Agent skill。Multi-Agent skill 单独开源，便于独立演化。

## 包含内容

- `AGENTS.md`：项目级 agent 行为规则。
- `templates/agent_memory/context.md`：稳定项目上下文。
- `templates/agent_memory/progress.md`：当前任务状态。
- `templates/agent_memory/bugs.md`：仍 relevant 的问题、失败尝试和风险。
- `docs/Agent-Memory.md`：记忆文件的使用说明。

## 快速开始

在项目根目录放：

```text
AGENTS.md
agent_memory/
  context.md
  progress.md
  bugs.md
  archive/
```

`agent_memory/archive/` 只创建目录，三个 `.md` 从 `templates/agent_memory/` 原样复制。

## 运行环境

AgentsMD Kit 是纯 Markdown，macOS、Linux、WSL2 和 Windows 都可以使用，没有 package install 步骤。

模板本身不绑定模型，但大型仓库、长时间排查和需要证据追踪的任务会明显受益于更强 reasoning。作者已验证的重型工作流画像是：Codex 风格本地 agent、可读写文件、可执行命令、GPT-5.5 级别 reasoning model，并在可用时使用 `high` 或 `xhigh` reasoning。

## 与 Multi-Agent Skill 的关系

`AGENTS.md` 是项目级定位：告诉 agent 在这个仓库里如何工作。

Multi-Agent skill 是任务编排：把复杂任务变成有角色、权限、边界、输出格式和停止条件的 brief。

两者拆开后，项目级规则能保持短而稳定，复杂任务方法论也能独立安装和升级。
