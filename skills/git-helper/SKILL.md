---
name: git-helper
description: Helps with common Git operations like branching, merging, and conflict resolution
---

# Git Helper

## When to Use

Use this skill when the user needs help with:
- Creating and managing branches
- Merging branches
- Resolving merge conflicts
- Checking Git status
- Committing changes
- Pushing/pulling changes

## Instructions

1. **Identify the Git operation needed**
   - Ask the user what they want to do
   - Understand their current Git state

2. **Provide the exact Git command**
   - Give the command with correct syntax
   - Include any necessary flags or options

3. **Explain what the command does**
   - Describe the purpose of the command
   - Explain any flags or options used

4. **Suggest best practices**
   - Recommend conventional commit messages
   - Suggest meaningful branch names
   - Advise on when to use `--force` (rarely)

5. **Handle common issues**
   - Merge conflicts
   - Detached HEAD state
   - Uncommitted changes blocking operations

## Common Commands Reference

### Branch Operations
```bash
# Create new branch
git checkout -b feature/my-feature

# List all branches
git branch -a

# Delete branch
git branch -d feature/my-feature
```

### Merging
```bash
# Merge a branch
git merge feature/my-feature

# Abort merge
git merge --abort
```

### Status and History
```bash
# Check status
git status

# View commit history
git log --oneline -10
```

## Notes

- Always advise users to commit or stash changes before switching branches
- Recommend creating a backup branch before complex operations
- Warn about `--force` push and suggest safer alternatives
