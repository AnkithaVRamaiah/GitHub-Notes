# Git Commands Reference

## Table of Contents

1. [Repository Management](#repository-management)
2. [File Management](#file-management)
3. [Branch Management](#branch-management)
4. [Commit Management](#commit-management)
5. [Synchronization](#synchronization)
6. [Merging and Rebasing](#merging-and-rebasing)
7. [Stashing](#stashing)
8. [Comparison and Inspection](#comparison-and-inspection)
9. [Git Configuration](#git-configuration)
10. [Practical Use Cases](#practical-use-cases)
11. [How to Practice](#how-to-practice)

---

## Repository Management

**Description:** These commands are used to create, clone, manage, and configure Git repositories.

- **Create a new repository:**
  ```bash
  git init
  ```
- **Clone an existing repository:**
  ```bash
  git clone <repository-URL>
  ```
- **Show current repository details:**
  ```bash
  git remote -v
  ```
- **Add a remote repository:**
  ```bash
  git remote add origin <repository-URL>
  ```
- **Rename a remote repository:**
  ```bash
  git remote rename origin new-origin-name
  ```
- **Remove a remote repository:**
  ```bash
  git remote remove origin
  ```

---

## File Management

**Description:** Commands to manage files in a repository, stage them, or revert changes.

- **Add a file to staging:**
  ```bash
  git add <file-name>
  ```
- **Add all files to staging:**
  ```bash
  git add .
  ```
- **Remove a tracked file from the repository:**
  ```bash
  git rm <file-name>
  ```
- **Undo file changes in the working directory:**
  ```bash
  git checkout -- <file-name>
  ```

---

## Branch Management

**Description:** Commands for creating, switching, managing, and deleting branches.

- **Create a new branch:**
  ```bash
  git branch <branch-name>
  ```
- **Switch to an existing branch:**
  ```bash
  git checkout <branch-name>
  ```
- **Create and switch to a new branch:**
  ```bash
  git checkout -b <branch-name>
  ```
- **Show all branches:**
  ```bash
  git branch -a
  ```
- **Rename a branch:**
  ```bash
  git branch -m <new-branch-name>
  ```
- **Delete a branch:**
  ```bash
  git branch -d <branch-name>
  ```
- **Delete a remote branch:**
  ```bash
  git push origin --delete <branch-name>
  ```

---

## Commit Management

**Description:** Commands for creating and managing commits, which capture changes in a repository.

- **Create a commit:**
  ```bash
  git commit -m "Commit message"
  ```
- **Amend the last commit:**
  ```bash
  git commit --amend
  ```
- **Show commit history:**
  ```bash
  git log
  ```
- **Show a specific commit:**
  ```bash
  git show <commit-hash>
  ```
- **Undo the last commit (keep changes unstaged):**
  ```bash
  git reset HEAD~
  ```
- **Revert a specific commit:**
  ```bash
  git revert <commit-hash>
  ```

---

## Synchronization

**Description:** Commands for synchronizing changes between local and remote repositories.

- **Push changes to a remote repository:**
  ```bash
  git push origin <branch-name>
  ```
- **Fetch changes from a remote repository:**
  ```bash
  git fetch
  ```
- **Pull changes (fetch and merge):**
  ```bash
  git pull origin <branch-name>
  ```

---

## Merging and Rebasing

**Description:** Commands for integrating changes from one branch into another.

- **Merge a branch:**
  ```bash
  git merge <branch-name>
  ```
- **Resolve merge conflicts (manual editing and staging files):**
  ```bash
  git add <file-name>
  git commit
  ```
- **Rebase a branch:**
  ```bash
  git rebase <branch-name>
  ```

---

## Stashing

**Description:** Temporarily stores changes not ready for commit, allowing you to work on other tasks.

- **Stash changes:**
  ```bash
  git stash
  ```
- **Apply stashed changes:**
  ```bash
  git stash apply
  ```
- **Show stashed changes:**
  ```bash
  git stash list
  ```
- **Delete a specific stash:**
  ```bash
  git stash drop <stash-id>
  ```

---

## Comparison and Inspection

**Description:** Commands to inspect and compare changes in a repository.

- **Show differences between commits:**
  ```bash
  git diff <commit1> <commit2>
  ```
- **Compare local branch with remote branch:**
  ```bash
  git diff <branch-name> origin/<branch-name>
  ```
- **Show who changed each line in a file:**
  ```bash
  git blame <file-name>
  ```

---

## Git Configuration

**Description:** Commands to configure global or local settings in Git.

- **Set global username:**
  ```bash
  git config --global user.name "Your Name"
  ```
- **Set global email:**
  ```bash
  git config --global user.email "your.email@example.com"
  ```
- **View current Git configuration:**
  ```bash
  git config --list
  ```

---

## Practical Use Cases

**Description:** Real-world scenarios for utilizing Git commands effectively.

- **Switch to a previous commit:**
  ```bash
  git checkout <commit-hash>
  ```
- **Remove a file from the last commit:**
  ```bash
  git reset HEAD~ <file-name>
  ```
- **Create a tag:**
  ```bash
  git tag <tag-name>
  ```
- **Push tags to remote:**
  ```bash
  git push origin --tags
  ```

---

## How to Practice

**Description:** Steps for practicing Git commands effectively.

1. **Create a demo project:**
   - Initialize a repository: `git init`
   - Create multiple branches and work on features: `git branch`
   - Commit changes: `git add`, `git commit`

2. **Experiment with remote repositories:**
   - Clone a repository from GitHub: `git clone`
   - Push changes and observe their effect: `git push`

3. **Handle scenarios:**
   - Simulate merge conflicts and resolve them.
   - Practice rebasing: `git rebase`
   - Use stash commands when switching tasks.
