# Git Workflows

## Introduction to Git Workflows
Git workflows define a structured approach to collaboration in software projects. Choosing the right workflow depends on your team size, project complexity, and deployment process.

## Centralized Workflow
A simple workflow where all developers work on a single branch, usually `main` or `master`.
```sh
git clone <repo-url>
git commit -m "Commit message"
git push origin main
```
### When to Use
- Small teams with minimal collaboration.
- Simple projects with infrequent changes.

## Feature Branch Workflow
Each feature or bug fix is developed in a separate branch before merging into the main branch.
```sh
git checkout -b feature-branch
git commit -m "Feature implementation"
git push origin feature-branch
```
### When to Use
- Medium to large teams.
- When features are developed independently.

## Gitflow Workflow
A structured workflow with `develop`, `feature`, `release`, and `hotfix` branches.
```sh
git checkout -b develop
git checkout -b feature-xyz develop
git checkout -b release-1.0 develop
```
### When to Use
- Large-scale projects.
- Clear release cycles with versioning.

## Forking Workflow
Each contributor forks the repository and submits pull requests for merging changes.
```sh
git clone <forked-repo>
git remote add upstream <original-repo>
git fetch upstream
git rebase upstream/main
```
### When to Use
- Open-source projects with external contributors.
- When contributors don’t have direct push access.

## Trunk-Based Development
Developers commit directly to `main`, keeping changes small and frequent.
```sh
git pull origin main
git commit -m "Small incremental change"
git push origin main
```
### When to Use
- Continuous integration (CI) environments.
- Rapid software development cycles.

## Summary
Now you understand various Git workflows. Next, let's proceed to [11_advanced_git.md](./11_advanced_git.md) to explore advanced Git techniques.

