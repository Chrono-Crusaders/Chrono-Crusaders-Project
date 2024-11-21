# Git Tutorial

This markdown file provides a detailed overview of Git, a widely-used version control system. It is essential for code management and collaborative software development.

## Table of Contents

- [Introduction](#introduction)
- [Standard Git Workflow](#standard-git-workflow)
- [Summary of Commands](#summary-of-commands)
  - [Basic Git Commands](#basic-git-commands)
  - [Config Commands](#config-commands)
  - [Working with Branches](#working-with-branches)
  - [Merging, Rebase and Conflicts](#merging-rebase-and-conflicts)
  - [Repository Inspection](#repository-inspection)
  - [Version Control Modification](#version-control-modification)
  - [Using Remote Repositories](#using-remote-repositories)
- [Branching Strategies](#branching-strategies)
- [Best Practices](#best-practices)
- [Visual Studio Code Extensions](#visual-studio-code-extensions)

## Introduction

- Git is a free and open source distributed version control system.
- Designed to track changes in files and coordinate work on those files among multiple people.
- Widely used in software development and in any projects involving file management.
- Designed to handle everything from small to very large projects with efficient and without interfering with each other.
- There are many platforms for hosting git repositories such as GitLab and GitHub.

### Key Features

**Version control**: Keeps a history of changes, allowing your to recert to previous versions.
**Collaborating**: Enables teams to work efficiently, even on large and complex projects.
**Branching**: Allows to experiment without affecting the main codebase and to work on multiple features simultaneously.
**Speed: Designed for performance even in large projects.
**Distributed nature**: Every developer has a full copy of the repository, improving reliability and flexibility.

### Key Terms in Git

**Repository**: A project folder tracked by Git.
**Remote Repository**: A Git repository hosted on a server, like GitLab.
**Commit**: A snapshot of changes saved to the repository.
**Branch**: An independent line of development.
**Merge**: Combining changes from one branch into another.

## Standard Git Workflow

### Clone or Create a Project

Option 1: Copy a remote repository to your local machine.

    git clone <repository-link>

Option 2: Initialize a local repository and link to a remote repository.

    git init
    git remote add origin <repository-link>

### Configure User Information

Before starting, verify and configure your Git user information. Adjust the global configuration if necessary, or set project-specific configuration:

    git config --list # Lists current Git configuration
    git config --global user.name "<your name>"
    git config --global user.email "<your email>"
    git config user.name "<project specific name>" # Set for current repository only
    git config user.email "<project specific email>" # Set for current repository only

### Select the right branch

Ensure you are working on the correct branch with these commands:

    git branch # Lists all branches
    git checkout (-b) <branch-name> # Switch to an existing branch or switch to a new one
    git pull origin <branch-name> # Pull latest changes for the branch from remote

### Track Changes and Commit

After modifying files or code, select the changes you want to include in the next commit and create the commit.

    git status # Shows the status
    git add <filename> # Add a specific file to the staging area
    git reset HEAD <filename> # Optionally, remove a file from the staging area
    git commit -m "<message>" # Create a local commit with a message

### Synchronize with Remote Repository: Push

Upload local commits to the remote repository.

    git push # Push local changes to the remote repository
    git push --set-upstream origin <branch-name> # For the first push in this branch

This step is typically followed by creating a merge or pull request in remote repository.

### Synchronize with Remote Repository: Pull

Fetch and merge changes from the remote repository:

    git pull origin <branch-name>

Repeat the steps from [Track Changes and Commit](#track-changes-and-commit) until the feature is completed or the task is done.

### Optional: Get Features of Other Branches into your Branch

To integrate changes from other branches into your branch, use:

    git fetch # Fetches all branches and their respective changes
    git merge origin/<target-branch> # Merge the specific branch into your current branch
    git push origin <your-branch-name> # Push merged changes to your branch on the remote

This is particularly useful when multiple team members' changes need to be consolidated or when major updates have been made to the main development branch since your last update.

---

## Summary of Commands

### Basic Git Commands

### Config Commands

### Working with Branches

### Merging, Rebase and Conflicts

### Repository Inspection

### Version Control Modification

### Using Remote Repositories

## Branching Strategies

## Best Practices

- Commit often and with descriptive messages.
- Ensure commit messages are clear, written in English, and start with a capital letter.
- Phrase your commit messages to complete the sentence: "If you apply this commit, it will ..."
- Regularly integrate changes from the main branch into your feature branch to avoid conflicts.
- Push changes only after verifying they are correct and follow the established workflow.
- Keep feature branches focused on a single goal and short-lived.
- Be consistent with the established Git workflow and branching strategy.
- Use .gitignore files to maintain a clean repository.
- Ensure sensitive information like passwords, API keys, or private data is excluded from commits at all times!
- Reach out to teammater if unexpected behaviour or errors occur.

## Visual Studio Code Extensions

VS Code offers a range of extensions that enhance the Git experience, making version control more intuitive and visually engaging:

- **Git Graph**: A Useful extension for viewing your repository's history in a graphical interface. It allows you to visualize branch structures and commit histories with ease.
- **Git History**: Helps you explore and search through the commit history of files and branches. It provides a detailed log of changes, including diffs of what has changed in each commit.
- **Git Blame**: Essential for quickly identifying who made changes to any line of code. It displays author information directly in the editor, allowing you to understand code ownership and history at a glance.

---

For more detailed information, visit the [official Git documentation](https://git-scm.com/doc).
