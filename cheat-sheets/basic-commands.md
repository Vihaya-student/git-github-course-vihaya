# Git Commands Cheat Sheet 📋

A quick reference guide for the most commonly used Git commands.

## 🔄 Basic Workflow

| Command | Description |
|---------|-------------|
| `git init` | Initialize a new Git repository |
| `git clone <url>` | Clone a repository from remote source |
| `git add <file>` | Stage changes for commit |
| `git add .` | Stage all changes |
| `git commit -m "message"` | Commit staged changes with a message |
| `git push` | Push commits to remote repository |
| `git pull` | Pull changes from remote repository |

## 📊 Status & Information

| Command | Description |
|---------|-------------|
| `git status` | Show working tree status |
| `git log` | Show commit history |
| `git diff` | Show changes between commits |
| `git branch` | List all local branches |
| `git branch -a` | List all branches (local and remote) |

## 🌿 Branching

| Command | Description |
|---------|-------------|
| `git branch <name>` | Create a new branch |
| `git checkout <branch>` | Switch to a branch |
| `git checkout -b <name>` | Create and switch to new branch |
| `git merge <branch>` | Merge branch into current branch |
| `git branch -d <branch>` | Delete a branch |

## 🔄 Remote Operations

| Command | Description |
|---------|-------------|
| `git remote -v` | List remote repositories |
| `git remote add origin <url>` | Add remote repository |
| `git fetch` | Download objects and refs from remote |
| `git pull origin <branch>` | Pull changes from remote branch |
| `git push origin <branch>` | Push changes to remote branch |

## 🔧 Configuration

| Command | Description |
|---------|-------------|
| `git config --global user.name "Name"` | Set global username |
| `git config --global user.email "email"` | Set global email |
| `git config --list` | List all configurations |

## 🗑️ Undoing Changes

| Command | Description |
|---------|-------------|
| `git restore <file>` | Discard changes in working directory |
| `git reset HEAD <file>` | Unstage changes |
| `git revert <commit>` | Create new commit that undoes changes |
| `git reset --hard <commit>` | Reset to specific commit (caution!) |

## 📦 Stashing

| Command | Description |
|---------|-------------|
| `git stash` | Stash changes |
| `git stash list` | List stashes |
| `git stash pop` | Apply and remove most recent stash |
| `git stash apply` | Apply most recent stash |
| `git stash drop` | Remove most recent stash |

## 🔍 Searching

| Command | Description |
|---------|-------------|
| `git grep "pattern"` | Search for pattern in tracked files |
| `git log --grep="pattern"` | Search commit messages |

## 📝 Tips & Tricks

1. **View commit history with graph:**
   ```bash
   git log --graph --oneline --all
   ```

2. **Show changes in last commit:**
   ```bash
   git show
   ```

3. **Amend last commit:**
   ```bash
   git commit --amend
   ```

4. **Create alias for common commands:**
   ```bash
   git config --global alias.st status
   ```

## 🚨 Common Issues

1. **Undo last commit (keeping changes):**
   ```bash
   git reset --soft HEAD~1
   ```

2. **Undo last commit (discarding changes):**
   ```bash
   git reset --hard HEAD~1
   ```

3. **Recover deleted branch:**
   ```bash
   git reflog
   git checkout -b <branch> <commit>
   ```

---

<div align="center">
  <p>Need more advanced commands? Check out our <a href="../docs/advanced-topics.md">Advanced Topics</a> guide!</p>
</div> 