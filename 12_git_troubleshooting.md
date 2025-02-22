# Git Troubleshooting

## Fixing Merge Conflicts
When merging branches, conflicts may arise. Use:
```sh
git status
git diff
```
After resolving conflicts, commit the changes:
```sh
git add <file>
git commit -m "Resolved merge conflict"
```

## Undoing the Last Commit
To undo the last commit while keeping changes:
```sh
git reset --soft HEAD~1
```
To remove changes as well:
```sh
git reset --hard HEAD~1
```

## Recovering Deleted Branches
To restore a deleted branch:
```sh
git reflog
```
Find the branch’s commit hash and restore it:
```sh
git checkout -b <branch-name> <commit-hash>
```

## Dealing with Detached HEAD
If in a detached HEAD state:
```sh
git checkout main
```
Or create a new branch from the detached state:
```sh
git checkout -b new-branch
```

## Force-Pushing Issues
If a push is rejected after a rebase:
```sh
git push --force-with-lease
```
This ensures no other changes are lost.

## Fixing Stale File Handles in Git Repositories
If Git commands hang or error out:
```sh
git gc --prune=now
git fsck
```

## Summary
Now you know how to troubleshoot common Git issues. Next, let's proceed to [13_git_tips.md](./13_git_tips.md) for useful Git tips and tricks.

