# Quality Assurance - Santri/Pelajar

## Domain: Quality Assurance

## Objective
Deliver small, safe, measurable improvements strictly inside the quality-assurance domain.

## Phase Workflow
1. **INIT** → Check for existing PRs, Issues, or proactive scan
2. **PLANNING** → Create workplan/todo
3. **IMPLEMENT** → Execute improvements
4. **VERIFY** → Ensure changes work correctly
5. **SELF-REFLECTION** → Update docs, create issues if needed
6. **DELIVER** → Create PR with proper labeling

## INIT Phase Protocol
- Check for open PRs with `quality-assurance` label
- Check for issues with `quality-assurance` label
- If none exist → proactive scan limited to QA domain
- If nothing valuable → scan and fix repository health within QA domain

## QA Standards

### Test Coverage Requirements
- Minimum 80% coverage for backend logic
- Minimum 70% coverage for frontend components
- Critical paths must have 100% coverage

### Code Quality Gates
- All tests must pass
- Zero linting warnings
- Zero type errors
- Build must succeed

### Security QA
- No hardcoded secrets
- Input validation on all endpoints
- Authentication checks on protected routes
- SQL injection prevention

### Performance QA
- API response time < 500ms
- Page load time < 2s
- No N+1 query patterns
- Proper indexing

## Issue Creation Rules
- One issue = one problem = one owner
- Must have clear acceptance criteria
- Must have measurable definition of done
- Label with `quality-assurance`
- Include test scenarios

## PR Requirements
- Label: `quality-assurance`
- Linked to issue if exists
- Up to date with default branch
- No conflicts
- Build/lint/test success
- ZERO warnings
- Small atomic diff

## Testing Strategy

### Unit Tests
- Test individual functions/methods
- Mock external dependencies
- Fast execution

### Integration Tests
- Test component interactions
- Use test database
- Verify data flow

### E2E Tests
- Critical user paths
- Cross-browser compatibility
- Performance benchmarks

## Known Quality Issues (Backlog)
- None currently identified

## QA Workflow Integration
This QA agent integrates with the larger orchestrator:
- Architect stage creates issues
- Specialists execute fixes
- Kritikus audits changes
- PR-Handler merges qualified PRs
