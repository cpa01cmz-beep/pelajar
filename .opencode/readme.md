# OpenCode Configuration

This repository uses OpenCode for AI-assisted development. This directory contains the configuration, agents, and skills for the Pelajar/Santri project.

## Overview

OpenCode is an open source AI coding agent available as a terminal-based interface, desktop app, or IDE extension.

- **Website**: https://opencode.ai
- **Documentation**: https://opencode.ai/docs
- **Zen (Free Models)**: https://opencode.ai/docs/zen/

## Configuration

### Model

This repository uses `opencode/minimax-m2.5-free` as the default model, which is a free model available through OpenCode Zen.

Other available free models:
- `opencode/gpt-5-nano` - Free GPT-5 Nano
- `opencode/big-pickle` - Free stealth model

### Agents

Custom agents are defined in `.opencode/agents/`:

| Agent | Description |
|-------|-------------|
| `rnd` | Research and Development specialist |
| `product-architect` | System architecture and design |
| `ai-agent-engineer` | AI integration development |
| `backend-engineer` | Server-side development |
| `frontend-engineer` | Client-side development |
| `ui-ux-engineer` | User experience design |
| `platform-engineer` | Infrastructure and DevOps |
| `security-engineer` | Security auditing |
| `quality-assurance` | Testing and validation |
| `dx-engineer` | Developer experience |
| `technical-writer` | Documentation |

### Skills

Custom skills are defined in `.opencode/skills/`:

| Skill | Description |
|-------|-------------|
| `github-workflow` | GitHub Actions workflow analysis |
| `repository-audit` | Repository health auditing |

## Usage

### Running OpenCode

```bash
opencode
```

### Initialize Project

```bash
opencode /init
```

### Use Specific Agent

```bash
opencode --agent backend-engineer "your prompt"
```

### Use Specific Model

```bash
opencode --model opencode/minimax-m2.5-free "your prompt"
```

## References

- Installation: https://opencode.ai/docs
- SDK: https://opencode.ai/docs/sdk
- Agents: https://opencode.ai/docs/agents/
- Skills: https://opencode.ai/docs/skills/
- LSP Servers: https://opencode.ai/docs/lsp/
- Custom Tools: https://opencode.ai/docs/custom-tools/
- Plugins: https://opencode.ai/docs/plugins/

## GitHub Actions Integration

This repository uses OpenCode in CI/CD through `.github/workflows/main.yml`. The workflow includes:

1. **Architect** - System architecture and planning
2. **Specialists** - Domain-specific agents for various roles
3. **Kritikus** - Code review and quality audit
4. **Fixer** - Repository maintenance and improvements
5. **PR-Handler** - PR merging and management

## Development Guidelines

- Follow STRICT PHASE: ANALYZE → PLAN → IMPLEMENT → VERIFY → SELF REFLECTION → DELIVER
- Use agents for domain-specific tasks
- Maintain this configuration as the project evolves
- Keep agents and skills updated with project needs
