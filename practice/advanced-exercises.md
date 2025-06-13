# Advanced Git & GitHub Exercises 🚀

These exercises will help you master advanced Git and GitHub concepts through hands-on practice.

## 🎯 Exercise 1: Git Workflow with Multiple Branches

### Goal
Create a complex branching structure and practice advanced Git operations.

### Steps
1. Create a new repository:
   ```bash
   mkdir advanced-git-practice
   cd advanced-git-practice
   git init
   ```

2. Create initial structure:
   ```bash
   echo "# Advanced Git Practice" > README.md
   git add README.md
   git commit -m "Initial commit"
   ```

3. Create feature branches:
   ```bash
   git checkout -b feature/auth
   echo "Authentication module" > auth.md
   git add auth.md
   git commit -m "Add authentication module"

   git checkout -b feature/database
   echo "Database module" > database.md
   git add database.md
   git commit -m "Add database module"
   ```

4. Practice rebasing:
   ```bash
   git checkout feature/auth
   git rebase main
   ```

5. Create a release branch:
   ```bash
   git checkout -b release/v1.0
   git merge feature/auth
   git merge feature/database
   ```

## 🎯 Exercise 2: Git Hooks

### Goal
Implement Git hooks to enforce code quality.

### Steps
1. Create pre-commit hook:
   ```bash
   # .git/hooks/pre-commit
   #!/bin/sh
   if git diff --cached | grep -i "debug"; then
       echo "Debug statements found. Aborting commit."
       exit 1
   fi
   ```

2. Make it executable:
   ```bash
   chmod +x .git/hooks/pre-commit
   ```

3. Test the hook:
   ```bash
   echo "debug: test" > test.md
   git add test.md
   git commit -m "Test hook"
   ```

## 🎯 Exercise 3: GitHub Actions

### Goal
Set up a CI/CD pipeline using GitHub Actions.

### Steps
1. Create workflow file:
   ```bash
   mkdir -p .github/workflows
   ```

2. Create CI workflow:
   ```yaml
   # .github/workflows/ci.yml
   name: CI
   on: [push, pull_request]
   jobs:
     test:
       runs-on: ubuntu-latest
       steps:
         - uses: actions/checkout@v2
         - name: Run tests
           run: echo "Running tests..."
   ```

3. Create deployment workflow:
   ```yaml
   # .github/workflows/deploy.yml
   name: Deploy
   on:
     push:
       branches: [main]
   jobs:
     deploy:
       runs-on: ubuntu-latest
       steps:
         - uses: actions/checkout@v2
         - name: Deploy
           run: echo "Deploying..."
   ```

## 🎯 Exercise 4: Git Submodules

### Goal
Practice working with Git submodules.

### Steps
1. Create main repository:
   ```bash
   mkdir main-project
   cd main-project
   git init
   ```

2. Add submodule:
   ```bash
   git submodule add https://github.com/username/submodule-repo
   ```

3. Update submodule:
   ```bash
   git submodule update --init --recursive
   ```

## 🎯 Exercise 5: Git LFS

### Goal
Set up Git LFS for large file management.

### Steps
1. Install Git LFS:
   ```bash
   git lfs install
   ```

2. Track large files:
   ```bash
   git lfs track "*.psd"
   git lfs track "*.zip"
   ```

3. Test LFS:
   ```bash
   # Create large file
   dd if=/dev/zero of=large.zip bs=1M count=100
   git add large.zip
   git commit -m "Add large file"
   ```

## 🎯 Exercise 6: Advanced Git Operations

### Goal
Practice advanced Git operations and recovery techniques.

### Steps
1. Create complex history:
   ```bash
   # Create multiple commits
   for i in {1..5}; do
     echo "Commit $i" > file$i.txt
     git add file$i.txt
     git commit -m "Add file $i"
   done
   ```

2. Practice interactive rebase:
   ```bash
   git rebase -i HEAD~5
   ```

3. Create and recover from detached HEAD:
   ```bash
   git checkout HEAD~3
   git checkout -b recovery-branch
   ```

## 🎯 Exercise 7: GitHub Pages

### Goal
Deploy a static website using GitHub Pages.

### Steps
1. Create website files:
   ```bash
   mkdir docs
   echo "<h1>My Website</h1>" > docs/index.html
   ```

2. Configure GitHub Pages:
   - Go to repository settings
   - Enable GitHub Pages
   - Select docs folder as source

3. Add custom domain (optional):
   - Add CNAME file
   - Configure DNS settings

## 🎯 Exercise 8: Security Practices

### Goal
Implement security best practices in Git.

### Steps
1. Set up GPG signing:
   ```bash
   # Generate GPG key
   gpg --full-generate-key

   # Configure Git
   git config --global user.signingkey <key>
   ```

2. Sign commits:
   ```bash
   git commit -S -m "Signed commit"
   ```

3. Set up branch protection:
   - Enable branch protection rules
   - Require pull request reviews
   - Require status checks

## 📋 Verification Steps

For each exercise:
1. Verify the changes
2. Check the Git history
3. Test the functionality
4. Document the results

## 🎓 Learning Points

- Advanced branching strategies
- Git hooks implementation
- CI/CD with GitHub Actions
- Submodule management
- Large file handling
- Security practices
- Website deployment

## 🆘 Need Help?

1. Check the [Advanced Topics Guide](../docs/advanced-topics.md)
2. Review the [Troubleshooting Guide](../docs/troubleshooting.md)
3. Join our [Discord Community](https://discord.gg/vihaya)

---

<div align="center">
  <p>Ready for more? Check out our <a href="expert-exercises.md">Expert Exercises</a>!</p>
</div> 