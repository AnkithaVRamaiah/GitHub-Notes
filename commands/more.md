Here’s a comprehensive list of **Git and GitHub commands** to cover a variety of operations, from basic version control actions to advanced features. Please note that there are many Git commands and related commands for GitHub actions, some of which may be specialized or rarely used. Below are about 300 Git-related commands.

---

### **Git Basics**

1. `git init` – Initialize a new Git repository.
2. `git clone <url>` – Clone an existing repository from a URL.
3. `git status` – Show the working directory status.
4. `git add <file>` – Stage a file to be committed.
5. `git add .` – Stage all modified files in the current directory.
6. `git commit -m "<message>"` – Commit staged changes with a message.
7. `git commit --amend` – Amend the last commit.
8. `git log` – Show the commit history.
9. `git log --oneline` – Show the commit history with one commit per line.
10. `git diff` – Show changes between commits, working tree, and index.
11. `git diff <file>` – Show changes for a specific file.
12. `git branch` – List all branches.
13. `git branch <branch_name>` – Create a new branch.
14. `git checkout <branch_name>` – Switch to a specific branch.
15. `git checkout -b <branch_name>` – Create and switch to a new branch.
16. `git merge <branch_name>` – Merge a branch into the current branch.
17. `git pull` – Fetch and merge changes from the remote repository.
18. `git fetch` – Download changes from the remote without merging.
19. `git push` – Push changes to a remote repository.
20. `git push <remote> <branch_name>` – Push changes to a specific remote branch.
21. `git reset` – Reset the current branch to a specific commit.
22. `git reset <commit>` – Reset changes from the staging area.
23. `git revert <commit>` – Create a new commit that undoes changes.
24. `git rm <file>` – Remove a file from both the staging area and the working directory.
25. `git rm --cached <file>` – Remove a file from the staging area without deleting it.
26. `git show <commit>` – Display information about a specific commit.
27. `git show <branch_name>` – Show details about a branch.
28. `git tag <tag_name>` – Create a new tag for a commit.
29. `git tag -d <tag_name>` – Delete a tag.
30. `git remote` – Show remote repositories.
31. `git remote add <name> <url>` – Add a new remote repository.
32. `git remote set-url <name> <url>` – Change the URL of a remote repository.
33. `git remote remove <name>` – Remove a remote repository.
34. `git push --tags` – Push tags to the remote repository.
35. `git fetch --all` – Fetch all branches from all remotes.
36. `git pull --rebase` – Pull changes from the remote repository, rebasing instead of merging.
37. `git clean -fd` – Remove untracked files from the working directory.
38. `git clean -fdx` – Remove all untracked files and directories.
39. `git reflog` – Show the reference logs.
40. `git stash` – Save changes temporarily.
41. `git stash pop` – Apply and remove the latest stash.
42. `git stash apply` – Apply a stash without removing it.
43. `git stash list` – List all stashes.
44. `git stash drop` – Remove a specific stash.
45. `git stash clear` – Remove all stashes.

---

### **Branching and Merging**

46. `git branch -d <branch_name>` – Delete a branch.
47. `git branch -D <branch_name>` – Force delete a branch.
48. `git merge --no-ff <branch_name>` – Merge a branch without fast-forward.
49. `git merge --squash <branch_name>` – Merge and squash all commits from the specified branch.
50. `git rebase <branch_name>` – Rebase the current branch onto another branch.
51. `git rebase --interactive` – Interactively rebase commits.
52. `git cherry-pick <commit>` – Apply a specific commit from another branch.
53. `git diff --staged` – Show the staged changes between the index and last commit.
54. `git merge --abort` – Abort the merge process.
55. `git rebase --abort` – Abort the rebase process.
56. `git rebase --continue` – Continue rebasing after resolving conflicts.

---

### **Working with Remotes**

57. `git remote -v` – Show all remotes.
58. `git remote show <remote_name>` – Show details about a specific remote repository.
59. `git remote prune <remote_name>` – Clean up stale references to remotes.
60. `git push origin --delete <branch_name>` – Delete a remote branch.
61. `git push origin :<branch_name>` – Delete a branch from the remote repository.
62. `git pull origin <branch_name>` – Pull a specific branch from the remote repository.
63. `git clone --depth <depth>` – Clone a repository with a specific depth (shallow clone).
64. `git fetch <remote>` – Fetch updates from a specific remote.
65. `git fetch --prune` – Fetch and prune references to deleted remote branches.

---

### **Tagging**

66. `git tag` – List all tags.
67. `git tag <tag_name> <commit>` – Create a new tag at a specific commit.
68. `git push origin <tag_name>` – Push a tag to a remote repository.
69. `git push origin --tags` – Push all tags to a remote repository.
70. `git tag -a <tag_name> -m "<message>"` – Create an annotated tag with a message.
71. `git tag -d <tag_name>` – Delete a tag locally.
72. `git tag -l` – List tags with a pattern.
73. `git show <tag_name>` – Display information about a tag.
74. `git describe --tags` – Show the most recent tag reachable from the current commit.
75. `git push origin :refs/tags/<tag_name>` – Delete a remote tag.

---

### **Configuration and Settings**

76. `git config --global user.name "<name>"` – Set the global user name.
77. `git config --global user.email "<email>"` – Set the global user email.
78. `git config --global core.editor <editor>` – Set the global editor for Git.
79. `git config --global color.ui auto` – Enable colored output for Git commands.
80. `git config --global alias.<alias> <command>` – Create a custom Git alias.
81. `git config --list` – List all Git configurations.
82. `git config --global core.autocrlf true` – Set Git to automatically convert line endings.
83. `git config --global merge.tool <tool>` – Set the default merge tool.

---

### **Git Log and History**

84. `git log --oneline` – Display commit history as one line per commit.
85. `git log --graph` – Display commit history in a graph form.
86. `git log --pretty=format:"%h - %an, %ar : %s"` – Customize the format of the commit history.
87. `git log --since=<date>` – Show commits since a specific date.
88. `git log --until=<date>` – Show commits up to a specific date.
89. `git log --author=<name>` – Show commits by a specific author.
90. `git log --grep=<pattern>` – Search commits for a pattern.
91. `git blame <file>` – Show line-by-line commit history for a file.
92. `git bisect` – Find the commit that introduced a bug by binary search.

---

### **Advanced Git Commands**

93. `git submodule add <url> <path>` – Add a submodule to a repository.
94. `git submodule update` – Update a submodule to the latest commit.
95. `git submodule update --remote` – Update a submodule to the latest commit from the remote.
96. `git submodule init` – Initialize submodules in a repository.
97. `git submodule status` – Show the status of submodules.
98. `git submodule update --recursive` – Update submodules recursively.
99. `git gc` – Run garbage collection to optimize repository performance.
100. `git fsck` – Check the integrity of the repository.

---

### **GitHub Commands**

101. `git hub` – (via GitHub CLI) Interact with GitHub repositories.
102. `gh repo create` – Create a new GitHub repository from the command line.
103. `gh repo clone <owner>/<repo>` – Clone a GitHub repository using GitHub CLI.
104. `gh pr create` – Create a pull request from the command line.
105. `gh pr merge` – Merge a pull request from the command line.
106. `gh pr status` – Show the status of pull requests.
107. `gh pr list` – List pull requests in the current repository.
108. `gh issue create` – Create a GitHub issue.
109. `gh issue list` – List open issues on GitHub.
110. `gh repo view` – View repository details from the command line.
111. `gh repo fork` – Fork a GitHub repository.
112. `gh pr checkout <pr_number>` – Checkout a pull request locally.
113. `gh pr review --approve` – Approve a pull request.
114. `gh pr review --request-changes` – Request changes to a pull request.
115. `gh repo sync

` – Sync your local fork with the upstream repository.

---

### **Git Hooks and Automation**

116. `git hooks` – Automate tasks using Git hooks (pre-commit, post-commit, etc.).
117. `git commit-msg` – Validate commit messages before committing.
118. `git pre-push` – Automate tasks before pushing changes.
119. `git pre-commit` – Run checks before a commit is made.

---

### **Interactive Rebase**

120. `git rebase -i HEAD~<n>` – Interactive rebase of the last `n` commits.
121. `git rebase --interactive <commit>` – Rebase from a specific commit.
122. `git rebase --edit-todo` – Edit the rebase todo list.
123. `git rebase --skip` – Skip a commit during rebase.

---

### **Cherry-Pick**

124. `git cherry-pick <commit>` – Apply a commit from another branch.
125. `git cherry-pick --abort` – Abort the cherry-pick operation.
126. `git cherry-pick --continue` – Continue after resolving conflicts during cherry-pick.

---

### **Working with SSH Keys and GitHub Authentication**

127. `ssh-keygen` – Generate a new SSH key.
128. `ssh-add <key>` – Add an SSH key to the agent.
129. `git remote set-url origin git@github.com:<user>/<repo>.git` – Change to SSH URL for GitHub.
130. `gh auth login` – Log in to GitHub using GitHub CLI.
131. `gh auth logout` – Log out from GitHub via GitHub CLI.
132. `gh auth status` – Check the authentication status.

---

### **Rewriting History and Squashing**

133. `git rebase -i HEAD~<n>` – Squash multiple commits into one.
134. `git filter-branch --env-filter` – Rewriting history of the repository.
135. `git reset --soft <commit>` – Reset to a commit and keep changes staged.

---

### **Working with Large Repositories and Git LFS**

136. `git lfs install` – Install Git Large File Storage (LFS).
137. `git lfs track <pattern>` – Track large files with Git LFS.
138. `git lfs push` – Push large files to GitHub with Git LFS.
139. `git lfs pull` – Pull large files from GitHub using Git LFS.
140. `git lfs fetch` – Fetch large files from the server.
141. `git lfs status` – Check the status of Git LFS files.
Here is a **continued list of additional Git and GitHub commands** to give you a more comprehensive understanding, focusing on advanced topics and automation tasks:

---

### **Git Rebase and Advanced History Management**

142. `git rebase --onto <new_base> <old_base> <branch>` – Rebase a branch onto a new base.
143. `git rebase --interactive HEAD~<n>` – Interactive rebase for the last `n` commits.
144. `git rebase --exec <command>` – Execute a command on each commit during rebase.
145. `git reflog expire --expire=<time>` – Expire reflog entries older than the specified time.
146. `git reflog delete` – Remove entries from the reflog.
147. `git log --graph --oneline --all` – View a graph of all commits in a repository.
148. `git diff --cached` – Show the differences between staged and committed changes.
149. `git log --merges` – Show only merge commits in the log.
150. `git log --stat` – Show the diffstat for each commit.
151. `git log --name-only` – Show the filenames of files modified in each commit.
152. `git log --name-status` – Show the status (added, modified, deleted) of files in each commit.
153. `git log --reverse` – Show the commit history in reverse order.
154. `git log --skip=<n>` – Skip the first `n` commits when showing the commit history.
155. `git blame -L <start>,<end> <file>` – Show blame information for specific lines in a file.

---

### **Git Stash**

156. `git stash save "<message>"` – Save changes with a custom message.
157. `git stash show` – Show the most recent stash.
158. `git stash show -p` – Show the diff of the most recent stash.
159. `git stash apply <stash_name>` – Apply a specific stash without removing it.
160. `git stash pop <stash_name>` – Apply and remove a specific stash.
161. `git stash drop <stash_name>` – Drop a specific stash from the list.
162. `git stash clear` – Remove all stashes from the list.

---

### **Git Workflows**

163. `git flow init` – Initialize a new git flow repository.
164. `git flow feature start <feature_name>` – Start a new feature in the git flow workflow.
165. `git flow feature finish <feature_name>` – Finish a feature in git flow and merge it into `develop`.
166. `git flow release start <release_name>` – Start a new release in git flow.
167. `git flow release finish <release_name>` – Finish a release and merge it into `master` and `develop`.
168. `git flow hotfix start <hotfix_name>` – Start a hotfix in git flow.
169. `git flow hotfix finish <hotfix_name>` – Finish a hotfix and merge it into `master` and `develop`.

---

### **GitHub Actions and CI/CD Automation**

170. `gh workflow run <workflow_name>` – Trigger a specific GitHub Actions workflow.
171. `gh workflow list` – List all workflows in a repository.
172. `gh workflow view <workflow_name>` – View details about a workflow.
173. `gh workflow logs <workflow_name>` – Show logs of a workflow run.
174. `gh run list` – List all workflow runs.
175. `gh run cancel <run_id>` – Cancel a workflow run.
176. `gh pr create --base <base_branch> --head <head_branch>` – Create a pull request with custom base and head.
177. `gh pr update --title <new_title>` – Update the title of an existing pull request.
178. `gh pr comment <pr_number> --body "<comment>"` – Add a comment to a pull request.
179. `gh repo delete <repo_name>` – Delete a repository on GitHub using GitHub CLI.
180. `gh repo fork <user>/<repo>` – Fork a GitHub repository using GitHub CLI.

---

### **GitHub Pages**

181. `git checkout --orphan <branch_name>` – Create a new branch with no previous commit history (useful for GitHub Pages).
182. `git rm -rf .` – Remove all files from the working directory (for GitHub Pages deployment).
183. `git commit --allow-empty -m "GitHub Pages commit"` – Create an empty commit for GitHub Pages.
184. `git push origin <branch_name>:gh-pages` – Push a branch to the GitHub Pages branch (`gh-pages`).

---

### **Git Submodules**

185. `git submodule add <url> <path>` – Add a submodule to the current repository.
186. `git submodule init` – Initialize the submodules.
187. `git submodule update` – Update the submodules to the latest commit.
188. `git submodule update --recursive` – Update all nested submodules.
189. `git submodule status` – Show the status of submodules.
190. `git submodule deinit <path>` – Deinitialize a submodule.
191. `git submodule update --remote <path>` – Update a submodule from the remote repository.

---

### **Advanced Merging and Rebasing**

192. `git merge --squash <branch_name>` – Squash changes from the specified branch into a single commit.
193. `git merge --no-commit` – Perform a merge but do not automatically commit.
194. `git merge --strategy=recursive -X ours` – Resolve merge conflicts by choosing the current branch's version.
195. `git merge --strategy=recursive -X theirs` – Resolve merge conflicts by choosing the other branch's version.
196. `git rebase -i HEAD~<n>` – Interactive rebase for the last `n` commits to edit, squash, or reorder commits.
197. `git rebase --skip` – Skip the current commit in an interactive rebase.
198. `git rebase --continue` – Continue the rebase after resolving conflicts.
199. `git merge --abort` – Abort the merge operation.
200. `git rebase --abort` – Abort the rebase operation.

---

### **Git Alias and Customization**

201. `git config --global alias.<alias> <command>` – Create a custom alias for a Git command.
202. `git config --global alias.st status` – Create an alias `st` for `git status`.
203. `git config --global alias.co checkout` – Create an alias `co` for `git checkout`.
204. `git config --global alias.br branch` – Create an alias `br` for `git branch`.
205. `git config --global alias.ci commit` – Create an alias `ci` for `git commit`.

---

### **Git Hooks**

206. `git config --global core.hooksPath <path>` – Set a custom path for Git hooks.
207. `git commit --no-verify` – Skip pre-commit hooks.
208. `git push --no-verify` – Skip pre-push hooks.
209. `git init --template=<path>` – Initialize a Git repository with a custom template.
210. `git log --format=%H` – Show commit hashes to use in hook scripts.
211. `git diff --cached` – Show the difference between staged changes and the previous commit (useful in pre-commit hooks).
212. `git pre-commit run` – Manually run pre-commit hooks.

---

### **GitHub and GitHub CLI**

213. `gh repo create <repo_name>` – Create a new repository on GitHub.
214. `gh repo fork <repo_name>` – Fork a repository on GitHub.
215. `gh repo clone <repo_name>` – Clone a GitHub repository.
216. `gh issue create` – Create a new issue in a repository.
217. `gh issue list` – List all issues in a repository.
218. `gh pr list` – List all pull requests in a repository.
219. `gh pr merge` – Merge a pull request from the command line.
220. `gh pr status` – Check the status of pull requests.
221. `gh pr comment` – Comment on a pull request.
222. `gh pr checkout` – Check out a pull request locally.
223. `gh pr review --approve` – Approve a pull request from the command line.
224. `gh repo view` – View repository details on GitHub.
225. `gh auth login` – Log in to GitHub CLI.
226. `gh auth logout` – Log out of GitHub CLI.
227. `gh auth status` – Check GitHub CLI authentication status.

---

### **GitHub API Usage**

228. `curl -u "<username>:<token>" https://api.github.com/users/<username>/repos` – Fetch repositories of a GitHub user via API.
229. `curl -u "<username>:<token>" https://api.github.com/repos/<username>/<repo>/issues` – Fetch issues of a specific repository.
230. `curl -u "<username>:<token>" -X POST -d '{"title":"<title>","body":"<body>"}' https://api.github.com/repos/<username>/<repo>/issues` – Create an issue on GitHub via API.
231. `curl -u "<username>:<token>" -X PATCH -d '{"state":"closed"}' https://api.github.com/repos/<username>/<repo>/issues/<issue_number>` – Close an issue via GitHub API.

---

### **Advanced Git Configuration**

232. `git config --global core.editor "<editor>"` – Set a global default text editor (e.g., `vim`, `nano`).
233. `git config --global user.signingkey <key>` – Set a

 GPG key for signing commits.
234. `git config --global merge.tool <tool>` – Set a default merge tool.
235. `git config --global diff.tool <tool>` – Set a default diff tool.
