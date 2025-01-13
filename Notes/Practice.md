### **Step 1: Install Git and Set Up Your Environment**

1. **Install Git:**
   - Download and install Git from [git-scm.com](https://git-scm.com/).
   - After installation, verify by running:
     ```bash
     git --version
     ```

2. **Set up your Git identity:**
   Configure your name and email to be associated with commits:
   ```bash
   git config --global user.name "Your Name"
   git config --global user.email "youremail@example.com"
   ```

---

### **Step 2: Create a Demo Project and Initialize a Repository**

1. **Create a new directory for your project:**
   ```bash
   mkdir my-demo-project
   cd my-demo-project
   ```

2. **Initialize a Git repository:**
   ```bash
   git init
   ```
   This creates a new `.git` directory in your project folder, indicating that it’s now a Git repository.

---

### **Step 3: Basic Commands**

1. **Create a file and track it:**
   - Create a new file (e.g., `index.html`) and add some content.
   - Stage the file for commit:
     ```bash
     git add index.html
     ```

2. **Commit changes:**
   - Commit the changes to Git with a message:
     ```bash
     git commit -m "Initial commit with index.html"
     ```

3. **Check the status of your repository:**
   ```bash
   git status
   ```
   - This shows which files are staged, modified, or untracked.

---

### **Step 4: Working with Branches**

1. **Create a new branch:**
   ```bash
   git branch feature-branch
   ```

2. **Switch to the new branch:**
   ```bash
   git checkout feature-branch
   ```
   - You can also combine the above two steps with:
     ```bash
     git checkout -b feature-branch
     ```

3. **Make changes and commit them:**
   - Edit `index.html` and save the changes.
   - Stage and commit those changes:
     ```bash
     git add index.html
     git commit -m "Updated index.html in feature-branch"
     ```

4. **Switch back to the main branch:**
   ```bash
   git checkout main
   ```

---

### **Step 5: Merging Branches**

1. **Merge your `feature-branch` into `main`:**
   ```bash
   git merge feature-branch
   ```
   - If there are conflicts, Git will notify you. You’ll need to manually resolve them by editing the files.

2. **Resolve merge conflicts:**
   - After resolving conflicts, add the resolved files and commit:
     ```bash
     git add <conflicted-file>
     git commit -m "Resolved merge conflicts"
     ```

---

### **Step 6: Working with Remote Repositories**

1. **Clone a remote repository (GitHub example):**
   ```bash
   git clone https://github.com/yourusername/your-repo.git
   ```

2. **Check the current remotes:**
   ```bash
   git remote -v
   ```

3. **Add a remote repository:**
   ```bash
   git remote add origin https://github.com/yourusername/your-repo.git
   ```

4. **Push local changes to remote:**
   ```bash
   git push origin main
   ```

5. **Pull updates from remote repository:**
   ```bash
   git pull origin main
   ```

---

### **Step 7: Tagging**

1. **Create a tag:**
   ```bash
   git tag v1.0
   ```

2. **Push tags to remote:**
   ```bash
   git push origin --tags
   ```

---

### **Step 8: Stashing Changes**

1. **Stash your changes:**
   ```bash
   git stash
   ```

2. **View your stash list:**
   ```bash
   git stash list
   ```

3. **Apply the most recent stash:**
   ```bash
   git stash apply
   ```

4. **Pop the stash (apply and remove it from the stash list):**
   ```bash
   git stash pop
   ```

---

### **Step 9: Rebase and Interactive Rebase**

1. **Rebase a branch onto another:**
   ```bash
   git rebase main
   ```

2. **Interactive rebase (e.g., to squash commits):**
   ```bash
   git rebase -i HEAD~3
   ```
   - This opens an editor where you can squash, edit, or reorder the last 3 commits.

---

### **Step 10: Working with Multiple Branches and Merge Strategies**

1. **Create multiple branches and simulate a feature development process:**
   - Work on a `feature-branch`, then merge it into `main` using different strategies:
     - **Fast-forward merge**: Happens when the branch has no divergent changes.
     - **No-ff merge**: Use `git merge --no-ff` to preserve commit history.

---

### **Step 11: Handling Conflicts and Advanced Merging**

1. **Simulate merge conflicts:**
   - Make conflicting changes in two branches and then attempt to merge them.
   - Practice resolving conflicts in different ways (manual resolution, using a merge tool).

2. **Abort a merge:**
   If you encounter a problem while merging and want to start over:
   ```bash
   git merge --abort
   ```

---

### **Step 12: Finalizing and Sharing Changes**

1. **Amend a commit (fix a mistake in the last commit):**
   ```bash
   git commit --amend
   ```

2. **Push changes to remote repository:**
   ```bash
   git push origin main
   ```

---

### **Step 13: Cleaning Up and Git Maintenance**

1. **Remove untracked files:**
   ```bash
   git clean -f
   ```

2. **View the Git log with pretty format:**
   ```bash
   git log --oneline --graph --decorate --all
   ```

3. **Prune old references to remote branches:**
   ```bash
   git remote prune origin
   ```

---

### **Additional Tips for Practicing Git:**

- **Experiment in a local repository:** Try all of the above commands in a local repository. Don’t worry about making mistakes—Git allows you to undo most actions, so you can learn by doing.
- **Try contributing to open-source projects:** This will expose you to real-world Git workflows, including pull requests, reviews, and collaborative development.

---

