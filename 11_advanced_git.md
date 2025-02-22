# Advanced Git Techniques

## Interactive Rebase
Interactive rebase allows modifying commit history by reordering, editing, squashing, or deleting commits.
```sh
git rebase -i HEAD~3
```
### When to Use
- Cleaning up commit history before merging.
- Squashing multiple commits into one for clarity.

## Cherry-Picking Commits
Apply a specific commit from one branch to another without merging the entire branch.
```sh
git cherry-pick <commit-hash>
```
### When to Use
- Selectively applying bug fixes.
- Moving isolated changes across branches.

## Bisecting to Find Bugs
Git bisect helps find the commit that introduced a bug using binary search.
```sh
git bisect start
```
### When to Use
- Debugging regressions efficiently.
- Narrowing down the cause of a bug.

## Worktrees
Worktrees allow working with multiple branches simultaneously without switching branches.
```sh
git worktree add ../new-worktree branch-name
```
### When to Use
- Handling multiple feature branches concurrently.
- Keeping the main workspace clean.

## Submodules
Submodules let you include one Git repository inside another.
```sh
git submodule add <repo-url>
```
### When to Use
- Managing dependencies as separate repositories.
- Keeping shared codebases separate while tracking updates.

## Hooks
Git hooks automate tasks at different stages of the Git workflow.
```sh
git hook pre-commit
```
### When to Use
- Enforcing coding standards automatically.
- Running tests before committing changes.

## Summary
Now you have a solid understanding of advanced Git techniques. Next, let's proceed to [12_git_troubleshooting.md](./12_git_troubleshooting.md) to learn how to fix common Git issues.

