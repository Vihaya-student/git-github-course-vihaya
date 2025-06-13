# Git & GitHub Troubleshooting Guide 🔧

This guide helps you resolve common issues and errors you might encounter while using Git and GitHub.

## 🔍 Common Git Issues

### 1. Authentication Problems

#### SSH Key Issues
```bash
# Generate new SSH key
ssh-keygen -t ed25519 -C "your.email@example.com"

# Test SSH connection
ssh -T git@github.com

# Add key to ssh-agent
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

#### HTTPS Authentication
```bash
# Configure credential helper
git config --global credential.helper store

# Update credentials
git config --global --unset credential.helper
git config --global credential.helper store
```

### 2. Merge Conflicts

#### Resolving Conflicts
1. Identify conflicting files:
   ```bash
   git status
   ```

2. Open and edit conflicting files
3. Mark as resolved:
   ```bash
   git add <file>
   ```

4. Complete merge:
   ```bash
   git commit -m "Resolve merge conflicts"
   ```

#### Aborting Merge
```bash
git merge --abort
```

### 3. Detached HEAD State

#### Recovery
```bash
# Create new branch
git checkout -b recovery-branch

# Or return to main
git checkout main
```

## 🔄 Common GitHub Issues

### 1. Push Rejected

#### Force Push (Use with Caution)
```bash
git push -f origin <branch>
```

#### Pull First
```bash
git pull --rebase origin <branch>
git push origin <branch>
```

### 2. Repository Access

#### Permission Denied
1. Check repository permissions
2. Verify SSH key setup
3. Check organization access
4. Contact repository admin

### 3. Large File Issues

#### Git LFS Setup
```bash
# Install Git LFS
git lfs install

# Track large files
git lfs track "*.psd"
git add .gitattributes
```

## 🛠️ Repository Issues

### 1. Corrupted Repository

#### Fix Corrupted Objects
```bash
# Check repository
git fsck

# Clean repository
git gc
git prune
```

#### Recover Lost Commits
```bash
# View reflog
git reflog

# Recover commit
git checkout -b recovery <commit>
```

### 2. Performance Issues

#### Optimize Repository
```bash
# Clean repository
git gc --aggressive

# Remove old objects
git prune

# Optimize repository
git maintenance start
```

### 3. Space Issues

#### Clean Large Files
```bash
# Find large files
git rev-list --objects --all | git cat-file --batch-check='%(objecttype) %(objectname) %(objectsize) %(rest)' | sort -k3nr | head -n 10

# Remove from history
git filter-branch --force --index-filter 'git rm --cached --ignore-unmatch <file>' --prune-empty --tag-name-filter cat -- --all
```

## 🔧 Configuration Issues

### 1. Git Config Problems

#### Reset Configuration
```bash
# View current config
git config --list

# Reset to default
git config --global --unset-all
```

#### Fix Line Endings
```bash
# Configure line endings
git config --global core.autocrlf input  # Linux/Mac
git config --global core.autocrlf true   # Windows
```

### 2. Editor Issues

#### Change Default Editor
```bash
# Set VS Code
git config --global core.editor "code --wait"

# Set Vim
git config --global core.editor "vim"
```

## 🚨 Emergency Recovery

### 1. Lost Changes

#### Recover Staged Changes
```bash
# View staged changes
git diff --cached

# Recover from index
git reset HEAD <file>
```

#### Recover Unstaged Changes
```bash
# View unstaged changes
git diff

# Recover from working directory
git checkout -- <file>
```

### 2. Accidentally Deleted Branch

#### Recover Branch
```bash
# Find commit
git reflog

# Recreate branch
git checkout -b <branch> <commit>
```

## 📱 Common Client Issues

### 1. GitHub Desktop

#### Reset GitHub Desktop
1. Close GitHub Desktop
2. Delete cache:
   - Windows: `%APPDATA%\GitHub Desktop`
   - Mac: `~/Library/Application Support/GitHub Desktop`
3. Restart GitHub Desktop

### 2. VS Code

#### Reset Git Integration
1. Close VS Code
2. Delete Git cache:
   - Windows: `%USERPROFILE%\.git`
   - Mac/Linux: `~/.git`
3. Restart VS Code

## 🆘 Getting Help

### 1. Official Resources
- [Git Documentation](https://git-scm.com/doc)
- [GitHub Help](https://help.github.com)
- [GitHub Community](https://github.community)

### 2. Community Support
- Stack Overflow
- GitHub Discussions
- Git mailing list

### 3. Professional Support
- GitHub Support
- Git consulting
- Training services

## 📝 Best Practices

### 1. Prevention
- Regular backups
- Clear commit messages
- Proper branching strategy
- Regular updates

### 2. Maintenance
- Regular cleanup
- Security updates
- Performance optimization
- Documentation updates

---

<div align="center">
  <p>Still having issues? Join our <a href="https://discord.gg/vihaya">Discord Community</a> for help!</p>
</div> 