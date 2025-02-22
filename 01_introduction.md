# Introduction to Git

## What is Git?
Git is a **distributed version control system** designed to handle everything from small to very large projects with speed and efficiency. It allows multiple developers to collaborate, track changes, and manage code versions seamlessly.

## Why Use Git?
- **Version Control**: Keeps track of every change in your project.
- **Collaboration**: Allows multiple developers to work on the same project simultaneously.
- **Branching and Merging**: Enables working on new features without affecting the main project.
- **Backup and Recovery**: Ensures your code is safe and can be restored.
- **Industry Standard**: Used by companies worldwide for software development.

## Centralized vs. Distributed Version Control
- **Centralized Version Control Systems (CVCS)**: A single central repository (e.g., SVN, Perforce) where changes are made and stored.
- **Distributed Version Control Systems (DVCS)**: Each user has a full copy of the repository (e.g., Git, Mercurial), allowing offline work and better collaboration.

## Key Concepts in Git
- **Repository**: A Git project containing all files and their history.
- **Commit**: A snapshot of changes made to the repository.
- **Branch**: An independent line of development.
- **Merge**: Combining changes from different branches.
- **Remote**: A version of the repository stored on a server (e.g., GitHub, GitLab).
- **Clone**: A copy of an existing repository.
- **Push & Pull**: Sending and retrieving changes from a remote repository.

## How Git Works (Basic Workflow)
1. **Initialize a repository** (`git init`)
2. **Add files to staging** (`git add <file>`)
3. **Commit changes** (`git commit -m "message"`)
4. **Create a branch** (`git branch <branch-name>`)
5. **Switch to branch** (`git checkout <branch-name>`)
6. **Merge branches** (`git merge <branch-name>`)
7. **Push changes to remote** (`git push origin <branch-name>`)

## Summary
Git is a powerful tool for version control and collaboration. Understanding its basic concepts and workflow will help you work efficiently in any software development project.

Next, let's proceed to [02_git_setup.md](./02_git_setup.md) to install and configure Git.