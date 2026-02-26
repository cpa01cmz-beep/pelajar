# Architecture

## System Overview

Santri/Pelajar is an autonomous AI-driven development system that continuously builds and maintains a fullstack serverless application.

## CI/CD Pipeline

The system uses GitHub Actions with 5 main stages:

### Stage 1: Architect (The Brain)
- Analyzes repository state
- Creates/audits GitHub issues
- Determines if system should enter CREATOR or MANAGER mode
- Creates development roadmap

### Stage 2: Specialists (The Muscle)
Parallel execution of 13 specialized agents:
1. RnD - Research and development
2. Product-Architect - Product design
3. AI-Agent-Engineer - AI agent development
4. Backend-Engineer - Backend implementation
5. Frontend-Engineer - Frontend implementation
6. UI-UX-Engineer - User interface design
7. Platform-Engineer - Infrastructure
8. Security-Engineer - Security auditing
9. Quality-Assurance - Testing
10. DX-Engineer - Developer experience
11. Technical-Writer - Documentation
12. User-Story-Engineer - User stories
13. Growth-Innovation-Strategist - Growth strategy

### Stage 2.5: Kritikus (The Supreme Auditor)
- Security review
- Logic validation
- Code quality assessment
- Performance analysis
- Consistency checking

### Stage 3: Fixer
- Repository health improvements
- AI agent integration
- OpenCode configuration management

### Stage 4: PR Handler
- Merges qualified PRs
- Resolves conflicts
- Runs build and test suite

## Workflow Triggers

- **Push to main**: Full pipeline execution
- **Every 4 hours**: Scheduled maintenance
- **Manual dispatch**: On-demand execution

## Security

The workflow has the following permissions:
- contents: write
- issues: write
- pull-requests: write
- actions: write
- id-token: write

## Agent Communication

Agents communicate through:
- GitHub Issues (task assignment)
- Pull Requests (code delivery)
- Documentation files (shared knowledge)
