# Git Submodules Example 📚

This example demonstrates how to work with Git submodules. Learn how to manage dependencies, share code between projects, and maintain submodule versions.

## 🎯 Project Overview

A microservices project that demonstrates:
- Submodule management
- Dependency tracking
- Code sharing
- Version control
- Best practices

## 📁 Project Structure

```
microservices/
├── api-gateway/
│   ├── src/
│   │   └── main.go
│   └── go.mod
├── auth-service/
│   ├── src/
│   │   └── main.go
│   └── go.mod
├── shared-libs/
│   ├── common/
│   │   └── utils.go
│   └── go.mod
├── .gitmodules
└── README.md
```

## 🚀 Getting Started

### 1. Initialize Repository
```bash
# Create main repository
mkdir microservices
cd microservices
git init

# Create .gitmodules file
touch .gitmodules
```

### 2. Add Submodules
```bash
# Add shared library as submodule
git submodule add https://github.com/your-org/shared-libs.git shared-libs

# Add service repositories
git submodule add https://github.com/your-org/api-gateway.git api-gateway
git submodule add https://github.com/your-org/auth-service.git auth-service
```

### 3. Configure Submodules
Create `.gitmodules`:
```
[submodule "shared-libs"]
    path = shared-libs
    url = https://github.com/your-org/shared-libs.git
    branch = main

[submodule "api-gateway"]
    path = api-gateway
    url = https://github.com/your-org/api-gateway.git
    branch = main

[submodule "auth-service"]
    path = auth-service
    url = https://github.com/your-org/auth-service.git
    branch = main
```

## 📝 Common Scenarios

### 1. Cloning with Submodules
```bash
# Clone repository with submodules
git clone --recursive https://github.com/your-org/microservices.git

# Or clone and update submodules
git clone https://github.com/your-org/microservices.git
cd microservices
git submodule update --init --recursive
```

### 2. Updating Submodules
```bash
# Update all submodules
git submodule update --remote

# Update specific submodule
git submodule update --remote shared-libs

# Pull changes in submodule
cd shared-libs
git pull origin main
cd ..
git add shared-libs
git commit -m "Update shared-libs submodule"
```

### 3. Working with Submodules
```bash
# Check submodule status
git submodule status

# Initialize submodules
git submodule init

# Update submodules
git submodule update

# Deinitialize submodule
git submodule deinit shared-libs
```

## 🛠️ Best Practices

### 1. Submodule Management
- Keep submodules up to date
- Use specific versions
- Document dependencies
- Regular maintenance

### 2. Version Control
- Pin submodule versions
- Track submodule changes
- Coordinate updates
- Test after updates

### 3. Collaboration
- Share submodule config
- Document setup steps
- Coordinate changes
- Regular sync

## 📋 Verification Steps

### 1. Setup Verification
```bash
# Check submodule status
git submodule status

# Verify .gitmodules
cat .gitmodules

# Check submodule paths
ls -la shared-libs
```

### 2. Update Verification
```bash
# Check for updates
git submodule update --remote --dry-run

# Verify changes
git diff shared-libs

# Test after update
cd shared-libs
go test ./...
```

### 3. Integration Verification
```bash
# Build with submodules
go build ./...

# Run tests
go test ./...

# Check dependencies
go mod tidy
```

## 🎯 Common Commands

### 1. Submodule Management
```bash
# Add submodule
git submodule add <repository-url> <path>

# Initialize submodules
git submodule init

# Update submodules
git submodule update

# Remove submodule
git submodule deinit <path>
git rm <path>
```

### 2. Version Control
```bash
# Check status
git submodule status

# Update to specific version
cd shared-libs
git checkout v1.0.0
cd ..
git add shared-libs
git commit -m "Pin shared-libs to v1.0.0"
```

### 3. Maintenance
```bash
# Update all submodules
git submodule update --remote

# Clean submodules
git submodule foreach git clean -fd

# Reset submodules
git submodule foreach git reset --hard
```

## 🔧 Submodule Examples

### 1. Basic Setup
```bash
# Initialize repository
git init
touch .gitmodules

# Add submodules
git submodule add https://github.com/your-org/shared-libs.git shared-libs
git submodule add https://github.com/your-org/api-gateway.git api-gateway

# Commit changes
git add .
git commit -m "Add submodules"
```

### 2. Update Process
```bash
# Update submodules
git submodule update --remote

# Check changes
git diff

# Commit updates
git add .
git commit -m "Update submodules"
```

### 3. Maintenance
```bash
# Check status
git submodule status

# Update submodules
git submodule update --remote

# Clean up
git submodule foreach git clean -fd
```

## 🆘 Need Help?

1. Check the [Advanced Topics Guide](../../docs/advanced-topics.md)
2. Review the [Troubleshooting Guide](../../docs/troubleshooting.md)
3. Join our [Discord Community](https://discord.gg/vihaya)

---

<div align="center">
  <p>Ready for more? Try our <a href="../08-git-worktree/README.md">Git Worktree Example</a>!</p>
</div> 