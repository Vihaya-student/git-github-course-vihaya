# Git Flow Workflow Example 🌊

This example demonstrates how to implement the Git Flow branching strategy in a real project. Learn how to manage releases, features, and hotfixes effectively.

## 🎯 Project Overview

A product management system that demonstrates:
- Git Flow branching strategy
- Release management
- Feature development
- Hotfix handling
- Version control

## 📁 Project Structure

```
product-manager/
├── README.md
├── src/
│   ├── components/
│   │   ├── ProductList.js
│   │   ├── ProductForm.js
│   │   └── ProductDetail.js
│   ├── services/
│   │   └── api.js
│   └── utils/
│       └── helpers.js
├── tests/
│   └── product.test.js
└── package.json
```

## 🚀 Getting Started

### 1. Install Git Flow
```bash
# macOS
brew install git-flow

# Linux
sudo apt-get install git-flow

# Windows
# Install Git Flow AVH Edition via Git Bash
```

### 2. Initialize Repository
```bash
# Create repository
git init
git flow init

# Answer prompts:
# - Production branch: main
# - Development branch: develop
# - Feature prefix: feature/
# - Release prefix: release/
# - Hotfix prefix: hotfix/
# - Support prefix: support/
# - Version tag prefix: v
```

## 🔄 Git Flow Workflow

### 1. Feature Development
```bash
# Start feature
git flow feature start user-authentication

# Work on feature
# ... make changes ...

# Finish feature
git flow feature finish user-authentication
```

### 2. Release Management
```bash
# Start release
git flow release start v1.0.0

# Make release changes
# ... update version, changelog ...

# Finish release
git flow release finish v1.0.0
```

### 3. Hotfix Handling
```bash
# Start hotfix
git flow hotfix start security-patch

# Fix issue
# ... make changes ...

# Finish hotfix
git flow hotfix finish security-patch
```

## 📝 Common Scenarios

### 1. Feature Development
```bash
# Create feature branch
git flow feature start new-product

# Make changes
echo "// New product functionality" > src/components/NewProduct.js
git add src/components/NewProduct.js
git commit -m "Add new product component"

# Finish feature
git flow feature finish new-product
```

### 2. Release Preparation
```bash
# Start release
git flow release start v1.1.0

# Update version
echo "1.1.0" > VERSION
git add VERSION
git commit -m "Bump version to 1.1.0"

# Update changelog
echo "## 1.1.0\n- New features\n- Bug fixes" >> CHANGELOG.md
git add CHANGELOG.md
git commit -m "Update changelog for 1.1.0"

# Finish release
git flow release finish v1.1.0
```

### 3. Hotfix Process
```bash
# Start hotfix
git flow hotfix start critical-bug

# Fix issue
# ... make changes ...
git add .
git commit -m "Fix critical bug"

# Finish hotfix
git flow hotfix finish critical-bug
```

## 🛠️ Best Practices

### 1. Branch Management
- Keep feature branches short-lived
- Regular merges to develop
- Clean up finished branches
- Use meaningful branch names

### 2. Release Process
- Semantic versioning
- Update changelog
- Tag releases
- Test before release

### 3. Hotfix Handling
- Quick response
- Minimal changes
- Test thoroughly
- Update documentation

## 📋 Verification Steps

### 1. Feature Verification
```bash
# Check feature branch
git branch

# Verify changes
git log --oneline

# Test functionality
npm test
```

### 2. Release Verification
```bash
# Check release branch
git branch

# Verify version
cat VERSION

# Check changelog
cat CHANGELOG.md
```

### 3. Hotfix Verification
```bash
# Check hotfix branch
git branch

# Verify fix
git log --oneline

# Test fix
npm test
```

## 🎯 Common Commands

### 1. Feature Commands
```bash
# List features
git flow feature list

# Start feature
git flow feature start <name>

# Finish feature
git flow feature finish <name>

# Publish feature
git flow feature publish <name>
```

### 2. Release Commands
```bash
# List releases
git flow release list

# Start release
git flow release start <version>

# Finish release
git flow release finish <version>

# Publish release
git flow release publish <version>
```

### 3. Hotfix Commands
```bash
# List hotfixes
git flow hotfix list

# Start hotfix
git flow hotfix start <name>

# Finish hotfix
git flow hotfix finish <name>

# Publish hotfix
git flow hotfix publish <name>
```

## 🆘 Need Help?

1. Check the [Advanced Topics Guide](../../docs/advanced-topics.md)
2. Review the [Troubleshooting Guide](../../docs/troubleshooting.md)
3. Join our [Discord Community](https://discord.gg/vihaya)

---

<div align="center">
  <p>Ready for more? Try our <a href="../04-github-actions/README.md">GitHub Actions Example</a>!</p>
</div> 