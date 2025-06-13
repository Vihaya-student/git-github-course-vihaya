# Your First Git Project 🎯

This exercise will guide you through creating your first Git repository and practicing basic Git commands. Follow each step carefully and try to understand what each command does.

## 🎯 Exercise Goals

- Create a new Git repository
- Make your first commit
- Create and switch branches
- Make changes and merge them
- Push to GitHub

## 📝 Step-by-Step Guide

### 1. Create a New Repository

```bash
# Create a new directory
mkdir my-first-git-project
cd my-first-git-project

# Initialize Git repository
git init
```

### 2. Create Your First File

Create a file named `hello.txt` with the following content:
```
Hello, Git!
This is my first repository.
```

### 3. Make Your First Commit

```bash
# Check status
git status

# Add the file
git add hello.txt

# Make the commit
git commit -m "Add hello.txt with initial content"
```

### 4. Create and Switch to a New Branch

```bash
# Create and switch to a new branch
git checkout -b feature/new-content
```

### 5. Make Changes in the New Branch

Add a new line to `hello.txt`:
```
Hello, Git!
This is my first repository.
I'm learning about branches!
```

### 6. Commit Your Changes

```bash
# Add and commit changes
git add hello.txt
git commit -m "Add new line about branches"
```

### 7. Switch Back to Main Branch

```bash
git checkout main
```

### 8. Merge Your Changes

```bash
git merge feature/new-content
```

### 9. Create a GitHub Repository

1. Go to [GitHub](https://github.com)
2. Click the "+" icon in the top right
3. Select "New repository"
4. Name it "my-first-git-project"
5. Don't initialize with README
6. Click "Create repository"

### 10. Push to GitHub

```bash
# Add the remote repository
git remote add origin https://github.com/YOUR_USERNAME/my-first-git-project.git

# Push your code
git push -u origin main
```

## 🎓 Learning Points

- `git init`: Initializes a new Git repository
- `git status`: Shows the status of your working directory
- `git add`: Stages changes for commit
- `git commit`: Creates a commit with staged changes
- `git checkout -b`: Creates and switches to a new branch
- `git merge`: Merges changes from one branch to another
- `git remote add`: Adds a remote repository
- `git push`: Pushes commits to a remote repository

## 📋 Verification Steps

1. Check your repository status:
   ```bash
   git status
   ```
   Should show "nothing to commit, working tree clean"

2. View your commit history:
   ```bash
   git log --oneline
   ```
   Should show at least two commits

3. Check your branches:
   ```bash
   git branch
   ```
   Should show both `main` and `feature/new-content`

## 🎯 Challenge

Try these additional tasks:

1. Create another branch called `feature/readme`
2. Add a README.md file with project information
3. Merge it back to main
4. Push all branches to GitHub

## 🆘 Need Help?

If you get stuck:
1. Check the [Basic Commands Cheat Sheet](../cheat-sheets/basic-commands.md)
2. Review the [Getting Started Guide](../docs/getting-started.md)
3. Join our [Discord Community](https://discord.gg/vihaya) (placeholder link)

---

<div align="center">
  <p>Ready for more? Try our <a href="intermediate-exercises.md">Intermediate Exercises</a>!</p>
</div> 