# Git Stashing

## What is Stashing?
Stashing allows you to temporarily save your uncommitted changes without committing them, so you can switch branches or work on something else.

## Saving Changes to Stash
To stash your current changes:
```sh
git stash
```
To include untracked files in the stash:
```sh
git stash -u
```

## Listing Stashes
To see all stashed changes:
```sh
git stash list
```

## Applying Stashed Changes
To apply the latest stash without removing it from the stash list:
```sh
git stash apply
```
To apply a specific stash:
```sh
git stash apply stash@{n}
```

## Popping Stashes
To apply and remove the latest stash:
```sh
git stash pop
```
To pop a specific stash:
```sh
git stash pop stash@{n}
```

## Dropping a Stash
To remove a specific stash:
```sh
git stash drop stash@{n}
```
To remove all stashes:
```sh
git stash clear
```

## Summary
Now you understand stashing in Git. Next, let's proceed to [08_git_reset_revert.md](./08_git_reset_revert.md) to learn about resetting and reverting changes.

