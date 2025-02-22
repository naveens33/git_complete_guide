# Git Scenarios and Commands (Interviewer Perspective)

## 1. Starting a New Project with Git
**Interviewer:** Imagine you’re starting a brand-new project. How would you initialize Git and push your first commit?
```sh
git init  # Initialize an empty Git repository
git add .  # Stage all files for commit
git commit -m "Initial commit"  # Commit the changes
git branch -M main  # Rename default branch to 'main'
git remote add origin <repo-url>  # Link the repository to a remote
git push -u origin main  # Push changes to the remote repository
```

## 2. Cloning an Existing Project
**Interviewer:** You just joined a team, and they have a repository you need to work on. How would you clone it?
```sh
git clone <repo-url>  # Clone the repository from remote
cd <repo-name>  # Move into the project directory
```

## 3. Working on a New Feature
**Interviewer:** Your team follows a feature-branch workflow. How would you create a branch and push your changes?
```sh
git checkout -b feature-branch  # Create and switch to a new branch
git add <file>  # Stage the modified or new file
git commit -m "Add new feature"  # Commit the changes
git push origin feature-branch  # Push the branch to remote
```

## 4. Keeping Your Local Repository Up to Date
**Interviewer:** Before starting work, how would you make sure your `main` branch is up to date?
```sh
git checkout main  # Switch to the main branch
git pull origin main  # Fetch and merge the latest changes
```

## 5. Merging a Feature Branch into Main
**Interviewer:** Your feature is complete. What steps would you take to merge it into `main`?
```sh
git checkout main  # Switch to the main branch
git pull origin main  # Ensure it's up to date
git merge feature-branch  # Merge the feature branch
git push origin main  # Push changes to remote
```

## 6. Undoing a Commit
**Interviewer:** You just committed a change by mistake. How can you undo it while keeping or discarding the changes?
```sh
git reset --soft HEAD~1  # Undo commit but keep changes staged
git reset --hard HEAD~1  # Undo commit and discard changes
```

## 7. Rebasing a Feature Branch
**Interviewer:** Your `main` branch has been updated while working on your feature. How would you rebase it?
```sh
git checkout feature-branch  # Switch to the feature branch
git rebase main  # Reapply commits on top of the updated main
```

## 8. Stashing Temporary Changes
**Interviewer:** You need to switch branches urgently, but you have uncommitted changes. What do you do?
```sh
git stash  # Save changes temporarily
git checkout main  # Switch to another branch
git pull origin main  # Get the latest changes
git checkout feature-branch  # Return to your feature branch
git stash pop  # Restore stashed changes
```

## 9. Resolving a Merge Conflict
**Interviewer:** A merge conflict occurs. How do you resolve it?
```sh
# Open the conflicted files and manually resolve conflicts
git add <resolved-file>  # Mark the conflict as resolved
git commit -m "Resolved merge conflict"  # Commit the resolution
git push origin main  # Push changes to remote
```

## 10. Squashing Commits Before Merging
**Interviewer:** Your pull request has multiple small commits. How can you squash them into one?
```sh
git rebase -i HEAD~3  # Interactive rebase the last 3 commits
# Change "pick" to "squash" for commits you want to merge
# Edit the commit message as needed
git push origin feature-branch --force  # Force push the changes
```

## 11. Squashing During a Merge
**Interviewer:** Instead of keeping all commits, your team prefers merging a feature as a single commit. How do you do that?
```sh
git checkout main  # Switch to main
git pull origin main  # Ensure it's up to date
git merge --squash feature-branch  # Squash changes into a single commit
git commit -m "Merge feature branch as a single commit"  # Create a single commit
git push origin main  # Push changes to remote
```

## 12. Checking the Commit History
**Interviewer:** How do you check the commit history in a readable format?
```sh
git log  # Show commit history
git log --oneline --graph  # Show a concise history with branch structure
```

## 13. Resetting a File to Its Last Committed State
**Interviewer:** You accidentally modified a file and want to reset it. How?
```sh
git checkout -- <file>  # Reset a file to the last committed version
```

## 14. Tagging Releases
**Interviewer:** Your project has a new release. How would you tag a specific commit?
```sh
git tag -a v1.0 -m "Release version 1.0"  # Create an annotated tag
git push origin v1.0  # Push the tag to remote
```

## 15. Bisecting to Find a Bug Introduction
**Interviewer:** A bug was introduced, and you need to pinpoint the exact commit. How would you do that?
```sh
git bisect start  # Start bisect mode
git bisect bad  # Mark current commit as bad
git bisect good <commit-hash>  # Mark an earlier commit as good
git bisect run <test-script>  # Automatically find the culprit commit
```

## 16. Recovering a Deleted Branch
**Interviewer:** You accidentally deleted a branch. How do you recover it?
```sh
git reflog  # Find the commit hash of the deleted branch
git checkout -b recovered-branch <commit-hash>  # Restore the branch
```

## 17. Reverting a Commit
**Interviewer:** How do you undo a commit that has already been pushed to the remote repository?
```sh
git revert <commit-hash>  # Create a new commit that undoes the specified commit
git push origin main  # Push the reverted commit to remote
```

## 18. Changing the Last Commit Message
**Interviewer:** You committed changes but realized you need to update the message. How do you do it?
```sh
git commit --amend -m "Updated commit message"  # Modify the last commit message
git push origin feature-branch --force  # Push the changes (if already pushed)
```

## 19. Cherry-Picking a Commit
**Interviewer:** A bug fix was committed to another branch. How do you apply it to your current branch?
```sh
git checkout feature-branch  # Switch to the branch where you need the fix
git cherry-pick <commit-hash>  # Apply the specific commit
git push origin feature-branch  # Push the changes
```

## 20. Ignoring Files Globally
**Interviewer:** You need to ignore some files across all repositories. How do you do that?
```sh
git config --global core.excludesfile ~/.gitignore_global  # Set up a global ignore file
echo "*.log" >> ~/.gitignore_global  # Ignore log files globally
```

## 21. Seeing Who Changed a Specific Line in a File
**Interviewer:** How do you find out who last modified a specific line in a file?
```sh
git blame <file>  # Show commit history line by line
```

## 22. Viewing Differences Between Branches
**Interviewer:** How do you check the difference between your branch and `main`?
```sh
git diff main..feature-branch  # Show differences between branches
```

## 23. Undoing the Last `git push`
**Interviewer:** You mistakenly pushed a commit and want to undo it. How?
```sh
git reset --hard HEAD~1  # Remove the last commit
git push origin feature-branch --force  # Force push the reset branch
```

## 24. Listing All Remote Branches
**Interviewer:** How do you check all branches in the remote repository?
```sh
git branch -r  # Show remote branches
```

## 25. Cleaning Up Untracked Files
**Interviewer:** Your working directory has unwanted files. How do you clean them?
```sh
git clean -f  # Remove untracked files
git clean -fd  # Remove untracked files and directories
```

## 26. Creating a Patch File
**Interviewer:** How do you create a patch file from your local changes?
```sh
git diff > changes.patch  # Save the diff into a patch file
```

## 27. Applying a Patch File
**Interviewer:** How do you apply a patch file to your repository?
```sh
git apply changes.patch  # Apply the patch to the working directory
```

## 28. Configuring a Custom Git Alias
**Interviewer:** How can you shorten a frequently used Git command?
```sh
git config --global alias.st status  # Create an alias for `git status`
git st  # Use the alias
```

## 29. Checking Out a Remote Branch Locally
**Interviewer:** A teammate created a new branch. How do you check it out?
```sh
git fetch origin  # Fetch the latest branches
git checkout -b new-branch origin/new-branch  # Create a local copy of the remote branch
```

## 30. Finding and Fixing a Mistaken Merge
**Interviewer:** You accidentally merged the wrong branch. How do you undo it?
```sh
git reset --hard ORIG_HEAD  # Reset to before the merge
git push origin main --force  # Push the reset state
```

---
