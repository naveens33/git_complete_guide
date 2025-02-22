# Git Logging

## Viewing Commit History
To see the commit history in your repository:
```sh
git log
```
For a compact one-line summary of commits:
```sh
git log --oneline
```

## Filtering Log Output
To view commits by a specific author:
```sh
git log --author="Author Name"
```
To search commit messages for a keyword:
```sh
git log --grep="keyword"
```
To show changes introduced by each commit:
```sh
git log -p
```

## Formatting Log Output
To display a concise commit graph:
```sh
git log --graph --oneline --decorate --all
```
To customize the output format:
```sh
git log --pretty=format:"%h - %an, %ar : %s"
```

## Viewing a Specific File's History
To see the commit history of a particular file:
```sh
git log -- <file>
```

## Checking Differences Between Commits
To compare the last two commits:
```sh
git diff HEAD~1 HEAD
```
To view changes for a specific commit:
```sh
git show <commit-hash>
```

## Summary
Now you understand how to log and inspect commit history in Git. Next, let's proceed to [09_git_aliases.md](./09_git_aliases.md) to learn about simplifying Git commands with aliases.

