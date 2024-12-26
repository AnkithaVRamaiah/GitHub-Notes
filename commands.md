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

### **1. Repository Management**
**Description:** These commands are used to create, clone, manage, and configure Git repositories.  
- **Create a new repository:** Initializes a new Git repository in your current directory.  
  ```bash
  git init
  ```
- **Clone an existing repository:** Copies a remote repository to your local system.  
  ```bash
  git clone <repository-URL>
  ```
- **Show current repository details:** Displays the remote URLs associated with the repository.  
  ```bash
  git remote -v
  ```
- **Add a remote repository:** Links your local repository to a remote repository.  
  ```bash
  git remote add origin <repository-URL>
  ```
- **Rename a remote repository:** Changes the alias name of the remote repository.  
  ```bash
  git remote rename origin new-origin-name
  ```
- **Remove a remote repository:** Deletes the reference to a remote repository from your local configuration.  
  ```bash
  git remote remove origin
  ```

---

### **2. File Management**
**Description:** Commands to manage files in a repository, stage them, or revert changes.  
- **Add a file to staging:** Prepares a specific file for the next commit.  
  ```bash
  git add <file-name>
  ```
- **Add all files to staging:** Stages all modified and new files.  
  ```bash
  git add .
  ```
- **Remove a tracked file:** Deletes a file from the repository and stages the removal.  
  ```bash
  git rm <file-name>
  ```
- **Undo file changes:** Reverts changes to a file in the working directory to the last committed state.  
  ```bash
  git checkout -- <file-name>
  ```
- **Unstage a file:** Removes a file from the staging area.  
  ```bash
  git reset <file-name>
  ```

---

### **3. Branch Management**
**Description:** Commands for creating, switching, managing, and deleting branches.  
- **Create a new branch:** Creates a new branch to work on a specific feature or fix.  
  ```bash
  git branch <branch-name>
  ```
- **Switch to an existing branch:** Changes the working branch to the specified branch.  
  ```bash
  git checkout <branch-name>
  ```
- **Create and switch to a new branch:** Combines branch creation and switching into one command.  
  ```bash
  git checkout -b <branch-name>
  ```
- **Show all branches:** Lists local and remote branches.  
  ```bash
  git branch -a
  ```
- **Rename a branch:** Updates the name of a branch.  
  ```bash
  git branch -m <new-branch-name>
  ```
- **Delete a branch:** Removes a branch locally.  
  ```bash
  git branch -d <branch-name>
  ```
- **Delete a remote branch:** Deletes a branch from the remote repository.  
  ```bash
  git push origin --delete <branch-name>
  ```

---

### **4. Commit Management**
**Description:** Commands for creating and managing commits, which capture changes in a repository.  
- **Create a commit:** Saves changes in the staging area to the repository.  
  ```bash
  git commit -m "Commit message"
  ```
- **Amend the last commit:** Updates the most recent commit with new changes.  
  ```bash
  git commit --amend
  ```
- **Show commit history:** Displays a list of past commits.  
  ```bash
  git log
  ```
- **Show a specific commit:** Displays details of a specified commit.  
  ```bash
  git show <commit-hash>
  ```
- **Undo the last commit:** Reverts the most recent commit, keeping the changes unstaged.  
  ```bash
  git reset HEAD~
  ```
- **Revert a specific commit:** Creates a new commit that undoes a specific commit.  
  ```bash
  git revert <commit-hash>
  ```
- **View a summary of commits:** Provides a condensed log of commits.  
  ```bash
  git log --oneline
  ```

---

### **5. Synchronization**
**Description:** Commands for synchronizing changes between local and remote repositories.  
- **Push changes:** Uploads changes from your local branch to the remote repository.  
  ```bash
  git push origin <branch-name>
  ```
- **Fetch changes:** Downloads updates from the remote repository but does not merge them.  
  ```bash
  git fetch
  ```
- **Pull changes:** Combines fetching and merging remote changes into the current branch.  
  ```bash
  git pull origin <branch-name>
  ```

---

### **6. Merging and Rebasing**
**Description:** Commands for integrating changes from one branch into another.  
- **Merge a branch:** Combines changes from a specified branch into the current branch.  
  ```bash
  git merge <branch-name>
  ```
- **Resolve merge conflicts:** Manually resolves conflicting changes after a merge.  
  ```bash
  git add <file-name>
  git commit
  ```
- **Rebase a branch:** Reapplies commits from one branch on top of another, creating a cleaner commit history.  
  ```bash
  git rebase <branch-name>
  ```

---

### **7. Stashing**
**Description:** Temporarily stores changes not ready for commit, allowing you to work on other tasks.  
- **Stash changes:** Saves changes without committing them.  
  ```bash
  git stash
  ```
- **Apply stashed changes:** Restores saved changes without removing them from the stash.  
  ```bash
  git stash apply
  ```
- **Show stashed changes:** Lists all stashed entries.  
  ```bash
  git stash list
  ```
- **Retrieve and apply a specific stash:** Restores a specific stash entry without removing it.  
  ```bash
  git stash apply <stash-id>
  ```
- **Delete a specific stash:** Removes a specific stash entry.  
  ```bash
  git stash drop <stash-id>
  ```

---

### **8. Comparison and Inspection**
**Description:** Commands to inspect and compare changes in a repository.  
- **Show differences between commits:** Displays changes between two commits.  
  ```bash
  git diff <commit1> <commit2>
  ```
- **Compare local and remote branches:** Shows differences between a local branch and its remote counterpart.  
  ```bash
  git diff <branch-name> origin/<branch-name>
  ```
- **Show who changed each line:** Displays the author and commit associated with each line in a file.  
  ```bash
  git blame <file-name>
  ```

---

### **9. Git Configuration**
**Description:** Commands to configure global or local settings in Git.  
- **Set global username:** Configures the global username for commits.  
  ```bash
  git config --global user.name "Your Name"
  ```
- **Set global email:** Sets the email used for commits.  
  ```bash
  git config --global user.email "your.email@example.com"
  ```
- **View current configuration:** Lists all current Git configuration settings.  
  ```bash
  git config --list
  ```
- **Edit Git configuration:** Opens the configuration file for editing.  
  ```bash
  git config --global --edit
  ```

---

### **10. Practical Use Cases**
**Description:** Real-world scenarios for utilizing Git commands effectively.  
- **Switch to a previous commit:** Temporarily checks out a specific commit.  
  ```bash
  git checkout <commit-hash>
  ```
- **Remove a file from the last commit:** Unstages a file from the most recent commit.  
  ```bash
  git reset HEAD~ <file-name>
  ```
- **Create a tag:** Marks a specific commit for reference.  
  ```bash
  git tag <tag-name>
  ```
- **List all tags:** Displays all created tags.  
  ```bash
  git tag
  ```
- **Push tags to remote:** Uploads local tags to the remote repository.  
  ```bash
  git push origin --tags
  ```

---

### **11. How to Practice**
**Description:** Steps for practicing Git commands effectively.  
- **Create a demo project:** Practice basic Git operations in a controlled environment.  
  - Initialize a repository:  
    ```bash
    git init
    ```
  - Create multiple branches and work on features:  
    ```bash
    git branch <branch-name>
    ```
  - Commit changes:  
    ```bash
    git add .
    git commit -m "message"
    ```
- **Experiment with remote repositories:** Learn remote workflows by using platforms like GitHub.  
  - Clone a repository:  
    ```bash
    git clone <repository-URL>
    ```
  - Push changes and observe their effect:  
    ```bash
    git push
    ```
- **Handle scenarios:** Simulate common challenges like merge conflicts or branch management tasks.  
  - Resolve merge conflicts:  
    ```bash
    git merge <branch-name>
    ```
  - Practice rebasing:  
    ```bash
    git rebase <branch-name>
    ```
  - Use stash commands when switching tasks:  
    ```bash
    git stash
    
