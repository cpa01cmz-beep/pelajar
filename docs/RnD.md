# RnD Domain Documentation

## Overview
RnD (Research & Development) specialist focuses on:
- Technical improvements to the repository
- Innovation opportunities
- Workflow optimization
- Repository health within R&D scope

## Current State (2026-02-26)
- Repository: cpa01cmz-beep/pelajar
- Initial commit: Workflow automation only
- No application code present yet

## Findings

### Issue 1: Inefficient PR Check in Specialists
**Location**: `.github/workflows/main.yml` lines 248-256
**Problem**: Each specialist job independently checks for open PRs AFTER architect runs, causing unnecessary job execution
**Impact**: Wastes CI/CD resources when PR already exists
**Proposed Solution**: Add early-exit job before architect to check for open PRs

## Implemented Fix
**Status**: Workflow change implemented locally (issue #36), awaiting merge. Docs update merged in PR #35.

Add `check-pr-exists` job before architect stage:
```yaml
check-pr-exists:
  name: "Check if PR Exists"
  runs-on: ubuntu-24.04-arm
  outputs:
    skip-all: ${{ steps.check.outputs.skip }}
  steps:
    - name: Check for Open PRs
      id: check
      run: |
        COUNT=$(gh pr list --state open --json number --jq length)
        if [ "$COUNT" -gt 0 ]; then
          echo "skip=true" >> $GITHUB_OUTPUT
        else
          echo "skip=false" >> $GITHUB_OUTPUT
        fi
```

Then update subsequent jobs:
- architect: add `needs: check-pr-exists` and `if: needs.check-pr-exists.outputs.skip-all != 'true'`
- specialists: add `needs: [architect, check-pr-exists]` and `if: ...`
- kritikus: add `needs: [specialists, check-pr-exists]` and `if: ...`
- fixer: add `needs: [specialists, check-pr-exists]` and `if: ...`
- PR-Handler: add `check-pr-exists` to needs array

Remove redundant check in specialists (lines 275-283).

<<<<<<< HEAD
**Note**: This change requires `workflows: write` permission to push. Current token lacks this permission due to GitHub security restrictions. Manual apply required.

## Action Items
- [x] Document findings in docs/RnD.md
- [ ] Apply workflow optimization manually (blocked by GitHub security)

## History
- 2026-02-26: Initial RnD scan - found workflow inefficiency
=======
## Action Items
- [x] Document findings in docs/RnD.md
- [x] Implement workflow optimization (local)
- [ ] Merge workflow changes (blocked by token permissions - see issue #36)

## History
- 2026-02-26: Initial RnD scan - found workflow inefficiency
- 2026-02-26: Workflow optimization implemented locally (issue #36)
>>>>>>> origin/main
