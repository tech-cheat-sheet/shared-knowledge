- [Installation](#installation)
- [Git First Setup](#git-first-setup)
  - [Set Globally (applies to all repos)](#set-globally-applies-to-all-repos)
  - [Set locally](#set-locally)
- [Useful Commands](#useful-commands)
# Installation
```shell
sudo apt install git --yes
```
# Git First Setup
## Set Globally (applies to all repos)
```shell
git config --global user.name "Your Name"
git config --global user.email "you@example.com"

git config --global init.defaultBranch main
# hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and 'development'. The just-created branch can be renamed via this command: 
# git branch -m  BRANCH_NAME
cd path/to/your/project
git init
git branch -m main
git status
git add .
git status
git commit -m COMMIT_MESSAGE

# Verify
git config --global --list
```
## Set locally
```shell
git config user.name "Your Name"
git config user.email "you@example.com"
```

# Useful Commands
| Category         | Command                                | Description                                                  |
|------------------|----------------------------------------|--------------------------------------------------------------|
| **Setup**        | `git config --global user.name "Name"` | Set your Git username                                        |
|                  | `git config --global user.email "email@example.com"` | Set your Git email address                        |
| **Initialize**   | `git init`                             | Create a new Git repository                                 |
|                  | `git clone <url>`                      | Clone an existing repository                                |
| **Staging**      | `git add <file>`                       | Stage a specific file                                       |
|                  | `git add .`                            | Stage all changes                                           |
| **Commit**       | `git commit -m "message"`              | Commit staged changes with a message                        |
|                  | `git commit --amend`                   | Modify the last commit                                     |
| **Branching**    | `git branch`                           | List branches                                               |
|                  | `git branch <name>`                    | Create a new branch                                         |
|                  | `git checkout <name>`                  | Switch to a branch                                          |
|                  | `git checkout -b <name>`               | Create and switch to a new branch                          |
|                  | `git merge <branch>`                   | Merge a branch into current branch                         |
| **Remote**       | `git remote add origin <url>`          | Add a remote repository                                    |
|                  | `git push -u origin <branch>`          | Push branch and set upstream                               |
|                  | `git pull`                             | Fetch and merge changes from remote                        |
| **Status & Logs**| `git status`                           | Show current status                                         |
|                  | `git log`                              | Show commit history                                         |
|                  | `git diff`                             | Show unstaged changes                                      |
| **Undo**         | `git reset <file>`                     | Unstage a file                                              |
|                  | `git checkout -- <file>`               | Discard changes to a file                                  |
|                  | `git revert <commit>`                  | Create a new commit that undoes a previous one             |
| **Stash**        | `git stash`                            | Save changes for later                                     |
|                  | `git stash pop`                        | Reapply stashed changes                                    |
