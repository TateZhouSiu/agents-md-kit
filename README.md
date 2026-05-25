# AgentsMD Kit

A compact `AGENTS.md` starter kit for coding-agent projects.

This repository is for project-level agent instructions and lightweight task memory. It deliberately does not include the Multi-Agent skill; that lives in a separate repository so the roles/brief workflow can evolve independently.

## What Is Included

- `AGENTS.md`: default project-level rules for agent behavior.
- `templates/agent_memory/context.md`: stable project context.
- `templates/agent_memory/progress.md`: current task state.
- `templates/agent_memory/bugs.md`: active issues, failed attempts, and repeated pitfalls.
- `docs/Agent-Memory.md`: explanation of the memory files and when to update them.

## What Belongs Here

Use this kit when you want an agent to:

- read relevant files before non-trivial changes,
- keep changes scoped and traceable,
- record durable context outside the chat,
- preserve current task state across long sessions,
- keep `AGENTS.md` short instead of turning it into a giant playbook.

## Quick Start

Copy these into a project root:

```text
AGENTS.md
agent_memory/
  context.md
  progress.md
  bugs.md
  archive/
```

Create `agent_memory/archive/` as an empty directory. Copy the three templates unchanged, then let the agent fill them during work.

## Runtime Fit

AgentsMD Kit is plain Markdown and works on macOS, Linux, WSL2, and Windows. It has no package install step.

The template is model-agnostic, but stronger reasoning improves outcomes on large repositories, long debugging sessions, and tasks that require evidence tracking. For workflows like the author's, a Codex-style local agent with file access, command execution, and a GPT-5.5-class reasoning model at `high` or `xhigh` reasoning is the known-good profile.

## Relationship To Multi-Agent Skill

`AGENTS.md` is project orientation. It answers: how should an agent behave in this repository?

The Multi-Agent skill is task orchestration. It answers: how should a complex task be scoped, delegated, reviewed, or handed off?

Keep them separate so global project rules stay small and the role brief workflow can be installed only when needed.
