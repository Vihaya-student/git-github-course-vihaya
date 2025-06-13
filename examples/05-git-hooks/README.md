# Git Hooks Example 🎣

This example demonstrates how to implement and use Git hooks for automation. Learn how to enforce code quality, run tests, and automate common tasks using Git hooks.

## 🎯 Project Overview

A Python project that demonstrates:
- Pre-commit hooks
- Post-commit hooks
- Pre-push hooks
- Custom hooks
- Hook management

## 📁 Project Structure

```
python-app/
├── .git/
│   └── hooks/
│       ├── pre-commit
│       ├── post-commit
│       ├── pre-push
│       └── commit-msg
├── src/
│   ├── main.py
│   └── utils.py
├── tests/
│   └── test_main.py
├── requirements.txt
└── README.md
```

## 🚀 Getting Started

### 1. Create Hooks Directory
```bash
# Navigate to your repository
cd your-repo

# Create hooks directory
mkdir -p .git/hooks
```

### 2. Create Pre-commit Hook
Create `.git/hooks/pre-commit`:
```bash
#!/bin/sh

# Run linter
echo "Running linter..."
flake8 src/

# Run tests
echo "Running tests..."
pytest tests/

# Check for debug statements
echo "Checking for debug statements..."
if git diff --cached | grep -i "debug\|print\|console.log"; then
    echo "Error: Debug statements found in code"
    exit 1
fi
```

### 3. Create Post-commit Hook
Create `.git/hooks/post-commit`:
```bash
#!/bin/sh

# Update documentation
echo "Updating documentation..."
python scripts/update_docs.py

# Notify team
echo "Sending notification..."
python scripts/notify_team.py
```

### 4. Create Pre-push Hook
Create `.git/hooks/pre-push`:
```bash
#!/bin/sh

# Run full test suite
echo "Running full test suite..."
pytest tests/ --cov=src/

# Check coverage
echo "Checking coverage..."
coverage report --fail-under=80
```

## 📝 Common Scenarios

### 1. Code Quality Hook
```bash
#!/bin/sh

# Run linter
echo "Running linter..."
flake8 src/

# Run type checker
echo "Running type checker..."
mypy src/

# Run formatter
echo "Running formatter..."
black src/
```

### 2. Test Hook
```bash
#!/bin/sh

# Run tests
echo "Running tests..."
pytest tests/

# Check coverage
echo "Checking coverage..."
coverage report --fail-under=80

# Exit if tests fail
if [ $? -ne 0 ]; then
    echo "Tests failed!"
    exit 1
fi
```

### 3. Documentation Hook
```bash
#!/bin/sh

# Update documentation
echo "Updating documentation..."
python scripts/update_docs.py

# Check documentation
echo "Checking documentation..."
python scripts/check_docs.py
```

## 🛠️ Best Practices

### 1. Hook Organization
- Keep hooks simple
- Use shell scripts
- Add error handling
- Include logging

### 2. Performance
- Optimize hook speed
- Use caching
- Run in parallel
- Skip when possible

### 3. Security
- Validate inputs
- Check permissions
- Handle secrets
- Log actions

## 📋 Verification Steps

### 1. Hook Verification
```bash
# Check hook permissions
ls -l .git/hooks/

# Test pre-commit hook
git commit -m "Test commit"

# Test pre-push hook
git push origin main
```

### 2. Hook Debugging
```bash
# Enable debug mode
export GIT_TRACE=1

# Run hook manually
.git/hooks/pre-commit

# Check hook logs
cat .git/hooks/logs/pre-commit.log
```

### 3. Hook Testing
```bash
# Test hook locally
bash .git/hooks/pre-commit

# Test hook with git
git commit -m "Test commit"

# Test hook with push
git push origin main
```

## 🎯 Common Commands

### 1. Hook Management
```bash
# List hooks
ls -l .git/hooks/

# Make hook executable
chmod +x .git/hooks/pre-commit

# Disable hook
mv .git/hooks/pre-commit .git/hooks/pre-commit.disabled
```

### 2. Hook Development
```bash
# Create hook
touch .git/hooks/pre-commit

# Edit hook
vim .git/hooks/pre-commit

# Test hook
bash .git/hooks/pre-commit
```

### 3. Hook Debugging
```bash
# Enable debug mode
export GIT_TRACE=1

# Run hook manually
.git/hooks/pre-commit

# Check hook logs
cat .git/hooks/logs/pre-commit.log
```

## 🔧 Hook Examples

### 1. Pre-commit Hook
```bash
#!/bin/sh

# Run linter
echo "Running linter..."
flake8 src/

# Run tests
echo "Running tests..."
pytest tests/

# Check for debug statements
echo "Checking for debug statements..."
if git diff --cached | grep -i "debug\|print\|console.log"; then
    echo "Error: Debug statements found in code"
    exit 1
fi
```

### 2. Post-commit Hook
```bash
#!/bin/sh

# Update documentation
echo "Updating documentation..."
python scripts/update_docs.py

# Notify team
echo "Sending notification..."
python scripts/notify_team.py
```

### 3. Pre-push Hook
```bash
#!/bin/sh

# Run full test suite
echo "Running full test suite..."
pytest tests/ --cov=src/

# Check coverage
echo "Checking coverage..."
coverage report --fail-under=80
```

## 🆘 Need Help?

1. Check the [Advanced Topics Guide](../../docs/advanced-topics.md)
2. Review the [Troubleshooting Guide](../../docs/troubleshooting.md)
3. Join our [Discord Community](https://discord.gg/vihaya)

---

<div align="center">
  <p>Ready for more? Try our <a href="../06-git-lfs/README.md">Git LFS Example</a>!</p>
</div> 