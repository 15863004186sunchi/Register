# Using Git Worktrees

## Overview
Git worktrees create isolated workspaces sharing the same repository, allowing work on multiple branches simultaneously without switching.

**Core principle:** Systematic directory selection + safety verification = reliable isolation.

**Announce at start:** "I'm using the using-git-worktrees skill to set up an isolated workspace."

## Directory Selection Process
1. **Check Existing Directories:** `.worktrees` or `worktrees`.
2. **Check CLAUDE.md:** For specified preferences.
3. **Ask User:** If no preference is found.

## Safety Verification
**MUST verify directory is ignored before creating worktree:**
```bash
git check-ignore -q .worktrees
```
If not ignored, add to `.gitignore` and commit.

## Creation Steps
1. **Detect Project Name.**
2. **Create Worktree:** `git worktree add <path> -b <branch>`.
3. **Run Project Setup:** `npm install`, `pip install`, etc.
4. **Verify Clean Baseline:** Run tests to ensure it starts green.
5. **Report Location.**
