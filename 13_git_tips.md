# Git Tips and Best Practices

## Use Descriptive Commit Messages
Write meaningful commit messages that describe what the change does.
```sh
git commit -m "Fix login bug by updating session handling"
```

## Stash Your Work Before Switching Branches
If you have uncommitted changes and need to switch branches:
```sh
git stash
git checkout <branch>
git stash pop  # Apply the stashed changes
```

## Use Aliases to Speed Up Commands
Set up Git aliases for frequently used commands:
```sh
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.cm "commit -m"
```

## Auto-Correct Mistyped Commands
Enable Git’s autocorrect feature:
```sh
git config --global help.autocorrect 1
```

## Track an Upstream Branch
To set an upstream branch for easy pulling and pushing:
```sh
git branch --set-upstream-to=origin/main
```

## Clean Up Unused Local Branches
To remove branches that have been merged and are no longer needed:
```sh
git branch --merged | grep -v "\*" | xargs git branch -d
```

## Find the Author of a Line in a File
To see who last modified a specific line:
```sh
git blame <file>
```

## Summary
Now you know useful Git tips and best practices. Next, let's proceed to [14_git_cheat_sheet.md](./14_git_cheat_sheet.md) for a quick reference guide to Git commands.

