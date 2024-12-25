Here’s a comprehensive list of Git commands categorized by different actions to help you practice and cover all topics:  

---

### **1. Repository Management**  
- **Create a new repository**  
  ```bash
  git init
  ```  

- **Clone an existing repository**  
  ```bash
  git clone <repository-URL>
  ```  

- **Show current repository details**  
  ```bash
  git remote -v
  ```  

- **Add a remote repository**  
  ```bash
  git remote add origin <repository-URL>
  ```  

- **Rename a remote repository**  
  ```bash
  git remote rename origin new-origin-name
  ```  

- **Remove a remote repository**  
  ```bash
  git remote remove origin
  ```  

---

### **2. File Management**  
- **Add a file to staging**  
  ```bash
  git add <file-name>
  ```  

- **Add all files to staging**  
  ```bash
  git add .
  ```  

- **Remove a tracked file from the repository**  
  ```bash
  git rm <file-name>
  ```  

- **Undo file changes in the working directory**  
  ```bash
  git checkout -- <file-name>
  ```  

---

### **3. Branch Management**  
- **Create a new branch**  
  ```bash
  git branch <branch-name>
  ```  

- **Switch to an existing branch**  
  ```bash
  git checkout <branch-name>
  ```  

- **Create and switch to a new branch**  
  ```bash
  git checkout -b <branch-name>
  ```  

- **Show all branches**  
  ```bash
  git branch -a
  ```  

- **Rename a branch**  
  ```bash
  git branch -m <new-branch-name>
  ```  

- **Delete a branch**  
  ```bash
  git branch -d <branch-name>
  ```  

- **Delete a remote branch**  
  ```bash
  git push origin --delete <branch-name>
  ```  

---

### **4. Commit Management**  
- **Create a commit**  
  ```bash
  git commit -m "Commit message"
  ```  

- **Amend the last commit**  
  ```bash
  git commit --amend
  ```  

- **Show commit history**  
  ```bash
  git log
  ```  

- **Show a specific commit**  
  ```bash
  git show <commit-hash>
  ```  

- **Undo the last commit (keep changes unstaged)**  
  ```bash
  git reset HEAD~
  ```  

- **Revert a specific commit**  
  ```bash
  git revert <commit-hash>
  ```  

---

### **5. Synchronization**  
- **Push changes to a remote repository**  
  ```bash
  git push origin <branch-name>
  ```  

- **Fetch changes from a remote repository**  
  ```bash
  git fetch
  ```  

- **Pull changes (fetch and merge)**  
  ```bash
  git pull origin <branch-name>
  ```  

---

### **6. Merging and Rebasing**  
- **Merge a branch**  
  ```bash
  git merge <branch-name>
  ```  

- **Resolve merge conflicts** (manual editing and staging files)  
  ```bash
  git add <file-name>
  git commit
  ```  

- **Rebase a branch**  
  ```bash
  git rebase <branch-name>
  ```  

---

### **7. Stashing**  
- **Stash changes**  
  ```bash
  git stash
  ```  

- **Apply stashed changes**  
  ```bash
  git stash apply
  ```  

- **Show stashed changes**  
  ```bash
  git stash list
  ```  

- **Delete a specific stash**  
  ```bash
  git stash drop <stash-id>
  ```  

---

### **8. Comparison and Inspection**  
- **Show differences between commits**  
  ```bash
  git diff <commit1> <commit2>
  ```  

- **Compare local branch with remote branch**  
  ```bash
  git diff <branch-name> origin/<branch-name>
  ```  

- **Show who changed each line in a file**  
  ```bash
  git blame <file-name>
  ```  

---

### **9. Git Configuration**  
- **Set global username**  
  ```bash
  git config --global user.name "Your Name"
  ```  

- **Set global email**  
  ```bash
  git config --global user.email "your.email@example.com"
  ```  

- **View current Git configuration**  
  ```bash
  git config --list
  ```  

---

### **10. Practical Use Cases**  
- **Switch to a previous commit**  
  ```bash
  git checkout <commit-hash>
  ```  

- **Remove a file from the last commit**  
  ```bash
  git reset HEAD~ <file-name>
  ```  

- **Create a tag**  
  ```bash
  git tag <tag-name>
  ```  

- **Push tags to remote**  
  ```bash
  git push origin --tags
  ```  

---

### **How to Practice**  
1. **Create a demo project**:  
   - Initialize a repository (`git init`).  
   - Create multiple branches and work on features (`git branch`).  
   - Commit changes (`git add`, `git commit`).  

2. **Experiment with remote repositories**:  
   - Clone a repository from GitHub (`git clone`).  
   - Push changes and observe their effect (`git push`).  

3. **Handle scenarios**:  
   - Simulate merge conflicts and resolve them.  
   - Practice rebasing (`git rebase`).  
   - Use stash commands when switching tasks.  

