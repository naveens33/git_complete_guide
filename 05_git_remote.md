# Working with Remote Repositories in Git

## Adding a Remote Repository
To link your local repository to a remote server:
```sh
git remote add origin <remote-url>
```
To verify remote repositories:
```sh
git remote -v
```

## Fetching Changes from Remote
To retrieve the latest changes from the remote repository without merging:
```sh
git fetch
```

## Pulling Changes
To fetch and merge remote changes into your local branch:
```sh
git pull origin <branch-name>
```

## Pushing Changes
To push local commits to the remote repository:
```sh
git push origin <branch-name>
```
To set an upstream branch and push:
```sh
git push --set-upstream origin <branch-name>
```

## Removing a Remote Repository
To remove a remote repository link:
```sh
git remote remove origin
```

## Summary
Now you have a solid understanding of working with remote repositories in Git. Next, let's proceed to [06_git_rebasing.md](./06_git_rebasing.md) to learn about rebasing.

