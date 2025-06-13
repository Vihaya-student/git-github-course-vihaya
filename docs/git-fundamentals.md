# Git Fundamentals 📚

This guide covers the core concepts and principles of Git that every developer should understand.

## 🔄 What is Git?

Git is a distributed version control system that helps you track changes in your code, collaborate with others, and maintain a history of your project's development.

## 🎯 Core Concepts

### 1. Repository (Repo)
- A storage location for your project
- Contains all project files and their history
- Can be local or remote (on GitHub)

### 2. Commit
- A snapshot of your project at a specific point in time
- Contains:
  - Changes made
  - Author information
  - Timestamp
  - Commit message

### 3. Branch
- A separate line of development
- Allows working on features without affecting the main code
- Can be merged back into the main branch

### 4. Working Directory
- The folder where you make changes
- Contains the actual files you're working with

### 5. Staging Area (Index)
- A middle ground between working directory and repository
- Where you prepare changes for commit

## 📊 Git Workflow

### Basic Workflow
1. Make changes in working directory
2. Stage changes (`git add`)
3. Commit changes (`git commit`)
4. Push to remote (`git push`)

### Branching Workflow
1. Create feature branch
2. Make changes
3. Commit changes
4. Switch to main branch
5. Merge feature branch

## 🔑 Key Commands Explained

### Repository Setup
```bash
# Initialize new repository
git init

# Clone existing repository
git clone <url>
```

### Basic Operations
```bash
# Check status
git status

# Stage changes
git add <file>
git add .

# Commit changes
git commit -m "message"

# View history
git log
```

### Branching
```bash
# Create branch
git branch <name>

# Switch branch
git checkout <branch>

# Create and switch
git checkout -b <name>

# Merge branch
git merge <branch>
```

## 📦 Understanding Git Objects

### 1. Blob
- Stores file content
- Identified by SHA-1 hash

### 2. Tree
- Directory structure
- Points to blobs and other trees

### 3. Commit
- Points to a tree
- Contains metadata
- Links to parent commit(s)

### 4. Tag
- Points to a specific commit
- Used for versioning

## 🔄 Remote Operations

### 1. Remote Repository
- Hosted on a server (e.g., GitHub)
- Shared with team members

### 2. Common Operations
```bash
# Add remote
git remote add origin <url>

# Push changes
git push origin <branch>

# Pull changes
git pull origin <branch>

# Fetch changes
git fetch origin
```

## 🛠️ Best Practices

### 1. Commit Messages
- Be descriptive
- Use present tense
- Keep it concise
- Reference issues if applicable

### 2. Branching Strategy
- Use meaningful branch names
- Keep branches short-lived
- Delete merged branches
- Use feature branches

### 3. Workflow
- Commit often
- Pull before pushing
- Review changes before committing
- Use .gitignore appropriately

## 🔍 Advanced Concepts

### 1. Rebase
- Alternative to merge
- Creates linear history
- Use with caution

### 2. Stash
- Temporarily store changes
- Useful for switching branches

### 3. Reset vs Revert
- Reset: Move branch pointer
- Revert: Create new commit

## 🎯 Common Scenarios

### 1. Undoing Changes
```bash
# Discard working changes
git checkout -- <file>

# Unstage changes
git reset HEAD <file>

# Undo last commit
git reset --soft HEAD~1
```

### 2. Resolving Conflicts
1. Identify conflicting files
2. Edit files to resolve conflicts
3. Stage resolved files
4. Complete merge/rebase

### 3. Recovering Lost Commits
```bash
# View reflog
git reflog

# Recover commit
git checkout -b recovery <commit>
```

## 📚 Additional Resources

- [Pro Git Book](https://git-scm.com/book/en/v2)
- [Git Documentation](https://git-scm.com/doc)
- [GitHub Guides](https://guides.github.com)

---

<div align="center">
  <p>Ready to practice? Try our <a href="../practice/first-steps.md">First Steps Exercise</a>!</p>
</div> 