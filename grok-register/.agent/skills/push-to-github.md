# Pushing to GitHub

## Overview
Use this skill when you need to commit and push changes to a remote GitHub repository.

**Announce at start:** "I'm using the push-to-github skill to commit and push my changes."

## Process
1. **Status Check:** Run `git status` to see what changes are pending.
2. **Select Changes:** Decide which files to include. Avoid including:
   - Sensitive credentials (e.g., `.env`, `.env.example` with real keys)
   - Large or unnecessary data files
   - IDE-specific configurations (unless specifically requested)
3. **Stage Changes:** Use `git add` for the selected files.
4. **Commit:** Write a concise, descriptive commit message following the [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) format.
   - `feat:` for new features
   - `fix:` for bug fixes
   - `docs:` for documentation changes
   - `refactor:` for code changes that neither fix a bug nor add a feature
5. **Push:** Run `git push origin <branch-name>`.
6. **Verify:** Confirm the push was successful and the remote repository is updated.
