# Advanced Git & GitHub Topics 🚀

This guide covers advanced concepts and techniques for Git and GitHub power users.

## 🔄 Advanced Git Concepts

### 1. Git Internals
- Object Database
- References
- Packfiles
- Loose Objects
- Git References

### 2. Advanced Branching
```bash
# Create orphan branch
git checkout --orphan <branch>

# Track remote branch
git branch --set-upstream-to=origin/<branch> <branch>

# Delete remote branch
git push origin --delete <branch>
```

### 3. Advanced Merging
```bash
# Merge with specific strategy
git merge -X theirs <branch>

# Merge without fast-forward
git merge --no-ff <branch>

# Abort merge
git merge --abort
```

## 🔧 Advanced Git Operations

### 1. Interactive Rebase
```bash
# Start interactive rebase
git rebase -i HEAD~3

# Squash commits
git rebase -i --root

# Edit commit messages
git rebase -i --root
```

### 2. Advanced Stashing
```bash
# Stash with message
git stash push -m "message"

# Stash specific files
git stash push <file>

# Create branch from stash
git stash branch <branch>
```

### 3. Advanced Logging
```bash
# Show merge commits
git log --merges

# Show commit differences
git log -p

# Show commit statistics
git log --stat
```

## 🛠️ Git Hooks

### 1. Local Hooks
- pre-commit
- post-commit
- pre-push
- post-merge

### 2. Server Hooks
- pre-receive
- post-receive
- update

### 3. Example Hook
```bash
#!/bin/sh
# pre-commit hook
if git diff --cached | grep -i "debug"; then
    echo "Debug statements found. Aborting commit."
    exit 1
fi
```

## 🔍 Advanced GitHub Features

### 1. GitHub Actions
```yaml
name: CI
on: [push, pull_request]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Run tests
        run: npm test
```

### 2. GitHub Pages
- Custom domains
- HTTPS
- Jekyll themes
- Custom 404 pages

### 3. GitHub Packages
- npm packages
- Docker images
- Maven artifacts
- NuGet packages

## 📦 Advanced Repository Management

### 1. Submodules
```bash
# Add submodule
git submodule add <url>

# Update submodules
git submodule update --init --recursive

# Remove submodule
git submodule deinit <path>
```

### 2. Git LFS
```bash
# Install Git LFS
git lfs install

# Track large files
git lfs track "*.psd"

# List tracked files
git lfs ls-files
```

### 3. Git Worktree
```bash
# Add worktree
git worktree add ../hotfix hotfix

# List worktrees
git worktree list

# Remove worktree
git worktree remove hotfix
```

## 🔐 Security Best Practices

### 1. GPG Signing
```bash
# Configure GPG
git config --global user.signingkey <key>

# Sign commits
git commit -S -m "Signed commit"

# Verify signatures
git log --show-signature
```

### 2. Branch Protection
- Require reviews
- Require status checks
- Require signatures
- Require linear history

### 3. Security Scanning
- Code scanning
- Secret scanning
- Dependency scanning
- Container scanning

## 🎯 Advanced Workflows

### 1. Git Flow
```bash
# Start feature
git flow feature start <name>

# Finish feature
git flow feature finish <name>

# Start release
git flow release start <version>
```

### 2. GitHub Flow
- Branch from main
- Make changes
- Create PR
- Review and merge
- Deploy

### 3. Trunk-Based Development
- Short-lived branches
- Continuous integration
- Feature flags
- Automated testing

## 📚 Advanced Resources

### 1. Git Books
- Pro Git
- Git Internals
- Git Workflows

### 2. GitHub Resources
- GitHub Actions
- GitHub Apps
- GitHub API

### 3. Tools
- GitKraken
- SourceTree
- GitLens

## 🎓 Learning Path

1. Master basic Git commands
2. Understand Git internals
3. Learn advanced workflows
4. Explore GitHub features
5. Implement security practices

## 🆘 Troubleshooting

### 1. Common Issues
- Merge conflicts
- Detached HEAD
- Lost commits
- Corrupted repository

### 2. Recovery Techniques
```bash
# Recover lost commit
git reflog
git checkout -b recovery <commit>

# Fix corrupted repository
git fsck
git gc
```

### 3. Performance Optimization
- Shallow clones
- Partial clones
- Git maintenance
- Repository cleanup

---

<div align="center">
  <p>Ready to master Git? Check out our <a href="practice/advanced-exercises.md">Advanced Exercises</a>!</p>
</div> 