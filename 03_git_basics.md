# Git Basics

## Initializing a Repository
To start using Git, navigate to your project directory and initialize a repository:
```sh
git init
```
This creates a `.git` directory, which stores all version control data.

## Cloning a Repository
To copy an existing repository from a remote source:
```sh
git clone <repository-url>
```
Example:
```sh
git clone https://github.com/user/repository.git
```

## Checking Repository Status
To check the status of your working directory and staged changes:
```sh
git status
```

## Adding Files to Staging
To track new or modified files:
```sh
git add <file>
```
To add all changes:
```sh
git add .
```

## Committing Changes
To save changes to the local repository:
```sh
git commit -m "Commit message"
```

## Viewing Commit History
To see a log of commits:
```sh
git log
```
For a compact one-line summary:
```sh
git log --oneline
```

## Undoing Changes
To unstage a file before committing:
```sh
git reset <file>
```
To undo the last commit (without deleting changes):
```sh
git reset --soft HEAD~1
```

## Deleting Files
To remove a file from tracking and delete it:
```sh
git rm <file>
```

## Summary
You have now learned the fundamental Git commands. Next, let's proceed to [04_branching_merging.md](./04_branching_merging.md) to understand branching and merging.

