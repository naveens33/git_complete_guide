# Branching and Merging in Git

## Creating a Branch
Branches allow you to work on new features without affecting the main project:
```sh
git branch <branch-name>
```
To list all branches:
```sh
git branch
```

## Switching Branches
To move between branches:
```sh
git checkout <branch-name>
```
Alternatively, using the newer command:
```sh
git switch <branch-name>
```

## Creating and Switching to a New Branch
To create and switch to a new branch in one step:
```sh
git checkout -b <branch-name>
```
Or using:
```sh
git switch -c <branch-name>
```

## Merging Branches
To merge a branch into the current branch:
```sh
git merge <branch-name>
```

## Resolving Merge Conflicts
If a conflict occurs during merging, Git will notify you. Manually edit the conflicting files, then stage and commit the resolved changes:
```sh
git add <file>
git commit -m "Resolved merge conflict"
```

## Deleting a Branch
To delete a branch that is no longer needed:
```sh
git branch -d <branch-name>
```
To force delete a branch:
```sh
git branch -D <branch-name>
```

## Summary
Now you have a good understanding of branching and merging in Git. Next, let's proceed to [05_remote_repositories.md](./05_remote_repositories.md) to learn about working with remote repositories.

