
# <img src="https://git-scm.com/images/logos/downloads/Git-Icon-1788C.png" alt="Git Logo" width="30"/> Git Commands for DevOps Engineers


### ✅ 1. Configuration Commands

**`git config`** – Set global username and email (important for commits).

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

---

### ✅ 2. Repository Setup

**`git init`** – Initialize a new Git repository.

```bash
git init
```

**`git clone`** – Copy a remote repo to your local system.

```bash
git clone https://github.com/user/repo.git
```

---

### ✅ 3. Staging and Committing

**`git status`** – See changes and what’s staged.

```bash
git status
```

**`git add`** – Stage files for commit.

```bash
git add filename       # stage specific file
git add .              # stage all changes
```

**`git commit`** – Save staged changes with a message.

```bash
git commit -m "Added new feature"
```
### 🛑 4.  Ignoring Unwanted Files
If you have a file like notes.txt that you don’t want Git to track (e.g., temporary notes, credentials, or logs), you can ignore it using .gitignore.

echo + .gitignore – Tell Git to always ignore a file.
```bash
echo notes.txt >> .gitignore     # add to ignore list
git rm --cached notes.txt        # stop tracking if already tracked
git add .gitignore
git commit -m "Ignore notes.txt"
```
🔒 This ensures notes.txt won’t be accidentally committed in the future.

---

### ✅ 5. Branching

**`git branch`** – List or create branches.

```bash
git branch              # list branches
git branch dev          # create branch 'dev'
```

**`git checkout`** – Switch branches.

```bash
git checkout dev
```

**`git switch`** – Alternative to checkout (simpler syntax).

```bash
git switch dev
```

---

### ✅ 5. Merging and Rebasing

**`git merge`** – Merge another branch into current branch.

```bash
git merge dev
```

**`git rebase`** – Reapply commits on top of another base tip.

```bash
git rebase main
```

---

### ✅ 6. Pushing and Pulling

**`git push`** – Upload local changes to remote.

```bash
git push origin main
```

**`git pull`** – Download and merge changes from remote.

```bash
git pull origin main
```

---

### ✅ 7. Remote Repositories

**`git remote`** – Manage remote repo URLs.

```bash
git remote -v                    # show remotes
git remote add origin <url>     # add remote
```

---

### ✅ 8. Reset and Revert

**`git reset`** – Unstage or move HEAD pointer.

```bash
git reset filename               # unstage
git reset --hard HEAD~1          # remove last commit completely
```

**`git revert`** – Undo a commit (safely for shared repos).

```bash
git revert <commit-id>
```

---

### ✅ 9. Logs and Diffs

**`git log`** – View commit history.

```bash
git log
```

**`git diff`** – Compare changes.

```bash
git diff                     # unstaged changes
git diff --staged            # staged changes
```

---

### ✅ 10. Tags

**`git tag`** – Mark specific commits (useful for CI/CD releases).

```bash
git tag v1.0
git push origin v1.0
```

---

### ✅ 11. Stash

**`git stash`** – Temporarily store changes.

```bash
git stash
```

**`git stash apply`**

```bash
git stash apply
```

---

### ✅ 12. Cherry-Pick

**`git cherry-pick`** – Apply specific commits to current branch.

```bash
git cherry-pick <commit-id>
```

---

### ✅ 13. Clean

**`git clean`** – Remove untracked files.

```bash
git clean -f
```

---

### ✅ 14. Useful Shortcuts

```bash
git shortlog          # summary of commits by author
git show              # shows details of a commit
git blame <file>      # see who changed what and when
```

---

### 🔧 DevOps Use Cases

- **CI/CD Pipelines**: Trigger builds with `git push`
- **Infra-as-Code**: Track Terraform/Ansible changes
- **Rollback**: Use `revert`, `reset`, and `tags`
- **Debugging**: Use `log`, `diff`, and `blame`

---
