---
name: git-helper
description: Common Git operations and workflows for version control
---

# Git Helper Skill

This skill provides guidance for common Git operations and best practices.

## When to Use

Use this skill when the user needs help with:
- Creating and managing branches
- Committing changes
- Merging and rebasing
- Resolving conflicts
- Git best practices

## Steps

1. Understand what Git operation the user needs
2. Provide the appropriate Git command or workflow
3. Explain the purpose and potential side effects
4. Offer to execute the command if appropriate

## Common Commands

- `git status` - Check current state
- `git branch` - List branches
- `git checkout -b <branch>` - Create and switch to new branch
- `git add . && git commit -m "message"` - Stage and commit changes
- `git merge <branch>` - Merge a branch
- `git rebase <branch>` - Rebase onto another branch

## Notes

- Always check status before destructive operations
- Commit messages should be clear and concise
- Consider using `--dry-run` for testing commands
