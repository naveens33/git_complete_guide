# Git Rebasing

## What is Rebasing?
Rebasing is a way to integrate changes from one branch into another by moving or rewriting commits instead of merging.

## Basic Rebasing
To rebase your current branch onto another branch:
```sh
git rebase <branch-name>
```

## Interactive Rebasing
To modify commit history:
```sh
git rebase -i HEAD~<number-of-commits>
```
Options include:
- `pick` - Keep the commit
- `edit` - Modify the commit
- `squash` - Merge with the previous commit
- `drop` - Remove the commit

## Resolving Conflicts During Rebase
If conflicts occur:
1. Manually resolve conflicts in affected files.
2. Stage resolved files:
   ```sh
   git add <file>
   ```
3. Continue the rebase:
   ```sh
   git rebase --continue
   ```
4. To abort rebasing:
   ```sh
   git rebase --abort
   ```

## Force Push After Rebasing
Since rebasing rewrites history, you may need to force push:
```sh
git push origin <branch-name> --force
```

## Summary
Now you understand rebasing in Git. Next, let's proceed to [07_git_stashing.md](./07_git_stashing.md) to learn about stashing changes.

