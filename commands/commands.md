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

### Repository Management

**Description:** These commands are used to create, clone, manage, and configure Git repositories.

- **Create a new repository:**
  ```bash
  git init
  ```
  Initializes a new Git repository in the current directory. This creates a `.git` subdirectory where all the repository metadata is stored.

- **Clone an existing repository:**
  ```bash
  git clone <repository-URL>
  ```
  Clones an existing repository from the specified URL. This command copies all the files, branches, and history from the remote repository to your local machine.

- **Show current repository details:**
  ```bash
  git remote -v
  ```
  Displays the URLs of the remote repositories associated with the current Git repository. This shows both fetch and push URLs.

- **Add a remote repository:**
  ```bash
  git remote add origin <repository-URL>
  ```
  Adds a new remote repository (usually named `origin`) to the current repository, pointing to the provided URL. This is often used to link a local repository to a remote one.

- **Rename a remote repository:**
  ```bash
  git remote rename origin new-origin-name
  ```
  Renames an existing remote repository. For example, you can rename `origin` to something like `upstream`.

- **Remove a remote repository:**
  ```bash
  git remote remove origin
  ```
  Removes the specified remote repository (`origin` in this case) from the current repository.

 - **Check the status of the repository:**
   ```bash
   git status
   ```
   Shows the current status of the repository, including staged, modified, and untracked files. It also provides information about the current branch and if it's up to date with the remote repository.

 - **View commit history:**
   ```bash
   git log
   ```
   Displays the commit history for the current branch. This shows commit messages, author details, and commit hashes.

 - **Pull changes from a remote repository:**
   ```bash
   git pull origin <branch-name>
   ```
   Fetches and merges changes from the remote repository for the specified branch into your local branch.

 - **Push changes to a remote repository:**
   ```bash
   git push origin <branch-name>
   ```
   Pushes your local commits to the specified branch on the remote repository.

 - **View configuration settings for Git:**
   ```bash
   git config --list
   ```
   Displays the current configuration settings for the repository, such as user name, email, and other Git configurations.

---

### File Management

**Description:** Commands to manage files in a repository, stage them, or revert changes.

- **Add a file to staging:**
  ```bash
  git add <file-name>
  ```
  Stages the specified file, preparing it for a commit. The file is tracked by Git once staged.

- **Add all files to staging:**
  ```bash
  git add .
  ```
  Stages all modified or newly created files in the current directory and its subdirectories. This is a convenient way to add everything to the staging area before committing.

- **Remove a tracked file from the repository:**
  ```bash
  git rm <file-name>
  ```
  Removes a file from both the working directory and the staging area, so it will be deleted from the repository upon the next commit.

- **Undo file changes in the working directory:**
  ```bash
  git checkout -- <file-name>
  ```
  Discards changes made to a file in the working directory and restores it to the last committed version. This command only works on files that are not staged.

---

### Branch Management

**Description:** Commands for creating, switching, managing, and deleting branches.

- **Create a new branch:**
  ```bash
  git branch <branch-name>
  ```
  Creates a new branch with the given name but does not switch to it. This is useful when you want to create multiple branches and switch between them later.

- **Switch to an existing branch:**
  ```bash
  git checkout <branch-name>
  ```
  Switches the working directory to the specified branch. The changes in your working directory will reflect the latest commit of that branch.

- **Create and switch to a new branch:**
  ```bash
  git checkout -b <branch-name>
  ```
  Creates a new branch and immediately switches to it. This is a shortcut for running `git branch` followed by `git checkout` in one command.

- **Show all branches:**
  ```bash
  git branch -a
  ```
  Lists all the local branches in the repository, along with the remote branches. Remote branches are prefixed with `remotes/`.

- **Rename a branch:**
  ```bash
  git branch -m <new-branch-name>
  ```
  Renames the current branch to a new name. If the branch you want to rename is not the currently active branch, you can specify its name before the new name.

- **Delete a branch:**
  ```bash
  git branch -d <branch-name>
  ```
  Deletes the specified branch. If the branch has unmerged changes, Git will prevent deletion to avoid losing work. You can force the deletion with `-D` if necessary.

- **Delete a remote branch:**
  ```bash
  git push origin --delete <branch-name>
  ```
  Deletes a branch from the remote repository (e.g., GitHub, GitLab). This command is typically used when a feature branch is no longer needed after being merged.

---

### **Commit Management**

**Description:** Commit management commands allow you to track and manage changes in your Git repository. A commit is a snapshot of changes made to the repository.

1. **Create a commit:**
   ```bash
   git commit -m "Commit message"
   ```
   - This command is used to create a commit in the local repository. The `-m` flag specifies the commit message, describing the changes made.

2. **Amend the last commit:**
   ```bash
   git commit --amend
   ```
   - This command modifies the last commit. You can edit the commit message or add changes to the previous commit. If you don't provide any new changes, it will only allow editing the commit message.

3. **Show commit history:**
   ```bash
   git log
   ```
   - This command shows the commit history in reverse chronological order, including commit hashes, author names, dates, and commit messages.

4. **Show a specific commit:**
   ```bash
   git show <commit-hash>
   ```
   - This command displays detailed information about a specific commit identified by `<commit-hash>`. It shows changes introduced in that commit along with metadata.

5. **Undo the last commit (keep changes unstaged):**
   ```bash
   git reset HEAD~
   ```
   - This command undoes the last commit while leaving the changes in the working directory. The `HEAD~` points to the commit before the last commit. The changes are not removed; they just become unstaged.

6. **Revert a specific commit:**
   ```bash
   git revert <commit-hash>
   ```
   - This command creates a new commit that undoes the changes made by a previous commit, identified by `<commit-hash>`. It doesn't remove the commit from history but reverses its effects.

### **Synchronization**

**Description:** Synchronization commands ensure that your local repository is in sync with the remote repository, either by sending or receiving changes.

1. **Push changes to a remote repository:**
   ```bash
   git push origin <branch-name>
   ```
   - This command uploads your local changes to the remote repository on the specified branch `<branch-name>`. `origin` refers to the default remote repository.

2. **Fetch changes from a remote repository:**
   ```bash
   git fetch
   ```
   - This command downloads objects and refs from the remote repository, including new commits, branches, or tags. It doesn't update your working directory or merge changes.

3. **Pull changes (fetch and merge):**
   ```bash
   git pull origin <branch-name>
   ```
   - This command is a combination of `git fetch` and `git merge`. It retrieves changes from the remote repository and merges them into your current branch.

- **Push tags to a remote repository:**
  ```bash
  git push origin --tags
  ```
  - This command pushes all tags to the remote repository. Tags are often used to mark specific points in history (e.g., releases).

### **Merging and Rebasing**

**Description:** These commands handle integrating changes from one branch into another, either by merging the branches together or by rebasing one branch onto another.

1. **Merge a branch:**
   ```bash
   git merge <branch-name>
   ```
   - This command merges the specified branch into the current branch. If there are no conflicts, the merge happens automatically. If there are conflicts, you'll need to resolve them manually.

2. **Resolve merge conflicts (manual editing and staging files):**
   ```bash
   git add <file-name>
   git commit
   ```
   - If merge conflicts occur during a merge, you need to manually resolve the conflicts in the affected files. After resolving the conflicts, use `git add` to stage the changes, and then create a commit to finalize the merge.

3. **Rebase a branch:**
   ```bash
   git rebase <branch-name>
   ```
   - This command re-applies commits from the current branch onto the `<branch-name>`, effectively changing the base of the current branch. Rebasing is often used to keep a clean commit history by avoiding unnecessary merge commits.

- **Abort a rebase (if issues arise during rebase):**
  ```bash
  git rebase --abort
  ```
  - This command cancels the ongoing rebase process and reverts to the state before the rebase started.

- **Skip a commit during rebase:**
  ```bash
  git rebase --skip
  ```
  - If you encounter a problematic commit during a rebase, this command skips that commit and continues with the rebase process.

---


### **Stashing**

**Description:** Stashing allows you to temporarily save changes that are not yet ready to be committed. This way, you can switch to another task or branch without losing your current work.

- **Stash changes:**
  ```bash
  git stash
  ```
  - This command temporarily saves changes (tracked files, staged files) to a "stash" and reverts the working directory to the last commit. The changes are stored in a special Git stash stack.
  
- **Apply stashed changes:**
  ```bash
  git stash apply
  ```
  - This command re-applies the changes saved in the most recent stash. It does not remove the stash from the stash list, so you can apply it again if needed.

- **Show stashed changes:**
  ```bash
  git stash list
  ```
  - Lists all the stashes saved in the stash stack. Each stash will be shown with an identifier like `stash@{0}`, `stash@{1}`, etc.

- **Delete a specific stash:**
  ```bash
  git stash drop <stash-id>
  ```
  - Deletes the stash with the given identifier (e.g., `stash@{0}`). Once deleted, the stash can no longer be applied.

- **Apply and delete the most recent stash:**
  ```bash
  git stash pop
  ```
  - This applies the most recent stash and removes it from the stash list in one operation.

- **Stash changes including untracked files:**
  ```bash
  git stash -u
  ```
  - This includes untracked files (files that are not yet added to Git) in the stash. If you don’t want to stash untracked files, omit the `-u` flag.

---

### **Comparison and Inspection**

**Description:** These commands help you compare changes in your repository or inspect file modifications, which is helpful for code review and tracking changes.

- **Show differences between commits:**
  ```bash
  git diff <commit1> <commit2>
  ```
  - Compares the changes between two commits. It will show which lines were added, modified, or deleted between the two specified commits. If no file is specified, it compares the entire repository.

- **Compare local branch with remote branch:**
  ```bash
  git diff <branch-name> origin/<branch-name>
  ```
  - Compares the changes in your local branch with the corresponding remote branch. This helps you see the differences between your local changes and the changes that are already on the remote repository.

- **Show who changed each line in a file:**
  ```bash
  git blame <file-name>
  ```
  - Displays the commit hash, author, and date for each line of a file. This helps you identify who made a particular change in a file, which is useful for debugging or understanding the history of a file.

- **Compare current changes with the last commit:**
  ```bash
  git diff
  ```
  - Shows the changes that have been made since the last commit. It will show differences between the current state of the working directory (including staged files) and the last commit in the repository.

- **Show differences between staged changes and the last commit:**
  ```bash
  git diff --cached
  ```
  - Compares the changes that have been staged (using `git add`) with the most recent commit, allowing you to see what will be committed next.

---

### **Git Configuration**

**Description:** These commands are used to configure Git settings globally or locally, such as your username, email, and other preferences.

- **Set global username:**
  ```bash
  git config --global user.name "Your Name"
  ```
  - This sets your global username that will be associated with all commits in all repositories. The `--global` flag applies this configuration to all repositories on your system unless overridden by local settings.

- **Set global email:**
  ```bash
  git config --global user.email "your.email@example.com"
  ```
  - Sets your global email address to be used in commits. Similar to `user.name`, this email will be used unless overridden in a specific repository.

- **View current Git configuration:**
  ```bash
  git config --global --list
  ```
  - Lists all the global configurations that have been set. This includes your username, email, and other preferences like color settings, core editor, etc.

- **Set a local repository username (overrides global):**
  ```bash
  git config user.name "Repo-Specific Name"
  ```
  - This sets a repository-specific username that overrides the global username for that specific repository. Useful if you contribute to multiple projects with different identities.

- **Set a local repository email (overrides global):**
  ```bash
  git config user.email "repo-specific-email@example.com"
  ```
  - Similarly, this sets a repository-specific email that overrides the global one for that specific repository.

- **View current configuration (local repository):**
  ```bash
  git config --list
  ```
  - Displays the configuration settings that apply to the current repository, including both global and local configurations.

- **Change the default editor for Git:**
  ```bash
  git config --global core.editor "nano"
  ```
  - This sets your default editor for Git commands like `git commit` (when it opens a text editor to write a commit message). You can use any text editor (e.g., `nano`, `vim`, `emacs`).


---

Here’s a detailed explanation of the Git commands you provided, along with any relevant additional commands for the topics:

---

### **Practical Use Cases**

#### **1. Switch to a previous commit:**
```bash
git checkout <commit-hash>
```
- **Explanation:** This command allows you to switch to a specific commit in the repository by using its commit hash. This is useful when you want to check the state of the repository at a particular point in time.
- **Additional commands:**
  - `git log`: Shows the history of commits, allowing you to find commit hashes for checkout.
  - `git checkout <branch-name>`: If you wish to switch to a branch instead of a specific commit.

#### **2. Remove a file from the last commit:**
```bash
git reset HEAD~1 <file-name>
```
- **Explanation:** This command removes a file from the last commit. It does so by "unstaging" the file, meaning it will only be removed from the commit but will remain in your working directory.
- **Additional commands:**
  - `git reset <commit>`: If you want to reset to a specific commit instead of just one commit prior (`HEAD~1`).
  - `git commit --amend`: If you want to modify the most recent commit (e.g., to remove a file).
  - `git rm <file-name>`: This command removes the file from the staging area and the working directory.

#### **3. Create a tag:**
```bash
git tag <tag-name>
```
- **Explanation:** Tags are used to mark a specific point in the history of the repository (typically for marking versions). You can create a lightweight tag like the one shown or an annotated tag using `git tag -a <tag-name> -m "Message"`.
- **Additional commands:**
  - `git tag -l`: Lists all tags in the repository.
  - `git show <tag-name>`: Displays information about the tag, such as the commit it points to.

#### **4. Push tags to remote:**
```bash
git push origin --tags
```
- **Explanation:** This command pushes all the tags to the remote repository. Tags are not automatically pushed with commits, so this is necessary to synchronize tags between the local and remote repositories.
- **Additional commands:**
  - `git push origin <tag-name>`: Push a specific tag to the remote repository.
  - `git push --tags`: Pushes all tags at once.

---

### **How to Practice**

#### **1. Create a demo project:**

##### - Initialize a repository:
```bash
git init
```
- **Explanation:** Initializes a new Git repository in the current directory. This command creates a `.git` directory where Git stores configuration files and repository data.
  
##### - Create multiple branches and work on features:
```bash
git branch <branch-name>
git checkout <branch-name>
```
- **Explanation:** `git branch` creates a new branch, and `git checkout` switches to that branch. These are used for working on separate features or bug fixes in isolation.
- **Additional commands:**
  - `git checkout -b <branch-name>`: A shorthand command to create a new branch and switch to it in one step.
  - `git merge <branch-name>`: Used to merge another branch into the current branch.

##### - Commit changes:
```bash
git add <file-name>
git commit -m "commit message"
```
- **Explanation:** `git add` stages changes for commit, and `git commit` records the changes with a message describing the commit. 
- **Additional commands:**
  - `git add .`: Stages all modified and new files for commit.
  - `git commit --amend`: Amend the last commit if you want to modify the commit message or add files to the last commit.

#### **2. Experiment with remote repositories:**

##### - Clone a repository from GitHub:
```bash
git clone <repository-url>
```
- **Explanation:** This command clones a repository from a remote URL to your local machine. It's useful for obtaining a local copy of a remote repository, enabling you to contribute to it.
- **Additional commands:**
  - `git remote -v`: Lists all remotes associated with your local repository.
  - `git pull origin <branch-name>`: Fetches changes from the remote and merges them into the current branch.

##### - Push changes and observe their effect:
```bash
git push origin <branch-name>
```
- **Explanation:** This command pushes your local commits to the remote repository, making them visible to others and sharing your changes.
- **Additional commands:**
  - `git push origin <branch-name> --force`: Pushes changes and overwrites any conflicts in the remote repository.
  - `git pull origin <branch-name>`: Fetches changes from the remote repository and merges them into the current branch.

#### **3. Handle scenarios:**

##### - Simulate merge conflicts and resolve them:
- **Explanation:** Merge conflicts occur when changes in different branches are incompatible with each other. You can simulate conflicts by editing the same lines of a file in two branches and trying to merge them.
- **Command for merging branches:**
  ```bash
  git merge <branch-name>
  ```
  - If conflicts arise, Git will mark the conflicted files, and you'll need to manually resolve them by editing the files. Once resolved, add the files with `git add <file-name>` and then commit the merge.

##### - Practice rebasing:
```bash
git rebase <branch-name>
```
- **Explanation:** Rebasing is the process of integrating changes from one branch into another, but it does so by rewriting the commit history. It’s often used to maintain a clean and linear project history.
- **Additional commands:**
  - `git rebase --interactive <commit-hash>`: Allows you to interactively rebase commits, such as squashing or editing commits.
  - `git rebase --continue`: Resumes the rebase after resolving any conflicts.

##### - Use stash commands when switching tasks:
```bash
git stash
git stash pop
```
- **Explanation:** `git stash` temporarily saves changes that are not yet ready to commit, allowing you to switch branches or work on something else without losing your work. `git stash pop` restores the stashed changes.
- **Additional commands:**
  - `git stash list`: Lists all stashed changes.
  - `git stash drop`: Removes a particular stash from the stash list.
  - `git stash apply`: Applies the stashed changes without removing them from the stash list.

---

