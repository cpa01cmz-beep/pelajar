# DX-Engineer Domain Documentation

## Overview
DX-Engineer focuses on improving Developer Experience within the repository. This includes tooling, documentation, processes, and automation that make it easier for developers to contribute and maintain the project.

## Domain Scope
- Developer tooling and workflows
- Documentation quality and accessibility
- CI/CD pipeline efficiency
- Code quality tools (linting, formatting, type checking)
- Testing infrastructure
- Onboarding experience for new contributors

## Guiding Principles
1. **Zero friction onboarding** - New contributors should be able to start working within minutes
2. **自动化 everything** - Repetitive tasks should be automated
3. **Clear conventions** - Code style, commit messages, PR processes should be well-defined
4. **Fast feedback loops** - CI should be fast and provide actionable feedback

## Repository-Specific Notes

### Current State
This is a seed repository for the "Santri/Pelajar" AI agent system. The primary artifact is the GitHub Actions workflow (`main.yml`) that orchestrates multiple AI specialist agents.

### Technology Stack
- **Runtime**: Node.js 20
- **AI Agent**: OpenCode
- **CI/CD**: GitHub Actions
- **Platform**: Serverless (designed for Vercel/Cloudflare)

### Workflow Structure
1. **Architect** - Creates issues and manages project roadmap
2. **Specialists** - Various domain experts (including DX-engineer) implement improvements
3. **Kritikus** - Audits code quality
4. **Fixer** - Improves repository health
5. **PR-Handler** - Merges qualified PRs

## DX Improvements History

### v1.0.0 (Initial)
- Established DX-engineer domain documentation
- Created base workflow structure

## Best Practices for This Repository

### When Adding New Features
1. Always update docs/blueprint.md if it's architecture-related
2. Create atomic, focused PRs
3. Include tests for new functionality
4. Update this document if adding new DX patterns

### CI/CD Guidelines
- Keep workflow execution time under 30 minutes
- Use caching aggressively
- Fail fast on critical issues
- Provide clear error messages

### Documentation Standards
- Use clear, concise language
- Include code examples where helpful
- Keep docs close to the code they describe
- Review docs as part of PR process
