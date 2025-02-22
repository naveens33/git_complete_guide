# Undoing Changes in Git

## Undoing Unstaged Changes
To discard unstaged changes in a file:
```sh
git checkout -- <file>
```
To discard all unstaged changes:
```sh
git reset --hard
```

## Undoing Staged Changes
To unstage a file while keeping the changes:
```sh
git reset <file>
```
To unstage all files:
```sh
git reset
```

## Undoing a Commit
To undo the last commit but keep the changes staged:
```sh
git reset --soft HEAD~1
```
To undo the last commit and move changes back to unstaged:
```sh
git reset --mixed HEAD~1
```
To undo the last commit and discard the changes:
```sh
git reset --hard HEAD~1
```

## Reverting a Commit
To create a new commit that undoes a previous commit:
```sh
git revert <commit-hash>
```

## Summary
Now you understand how to undo changes in Git. Next, let's proceed to [10_git_workflows.md](./10_git_workflows.md) to learn about Git workflows and how to use them effectively.

