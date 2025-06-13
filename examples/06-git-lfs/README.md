# Git LFS Example 📦

This example demonstrates how to handle large files in Git using Git Large File Storage (LFS). Learn how to manage large files efficiently in your Git repository.

## 🎯 Project Overview

A game development project that demonstrates:
- Large file management
- Git LFS setup
- File tracking
- LFS operations
- Best practices

## 📁 Project Structure

```
game-project/
├── assets/
│   ├── textures/
│   │   ├── character.png
│   │   └── background.jpg
│   ├── models/
│   │   ├── character.fbx
│   │   └── environment.obj
│   └── audio/
│       ├── music.mp3
│       └── effects.wav
├── src/
│   ├── main.cpp
│   └── utils.cpp
├── .gitattributes
└── README.md
```

## 🚀 Getting Started

### 1. Install Git LFS
```bash
# macOS
brew install git-lfs

# Linux
sudo apt-get install git-lfs

# Windows
# Download from https://git-lfs.github.com/
```

### 2. Initialize Git LFS
```bash
# Initialize Git LFS
git lfs install

# Verify installation
git lfs version
```

### 3. Configure File Tracking
Create `.gitattributes`:
```
# Track all PNG files
*.png filter=lfs diff=lfs merge=lfs -text

# Track all JPG files
*.jpg filter=lfs diff=lfs merge=lfs -text

# Track all FBX files
*.fbx filter=lfs diff=lfs merge=lfs -text

# Track all OBJ files
*.obj filter=lfs diff=lfs merge=lfs -text

# Track all audio files
*.mp3 filter=lfs diff=lfs merge=lfs -text
*.wav filter=lfs diff=lfs merge=lfs -text
```

## 📝 Common Scenarios

### 1. Tracking Large Files
```bash
# Track specific file
git lfs track "assets/textures/character.png"

# Track file pattern
git lfs track "*.png"

# Track directory
git lfs track "assets/models/**"

# List tracked files
git lfs ls-files
```

### 2. Managing Large Files
```bash
# Add large file
git add assets/textures/character.png

# Commit changes
git commit -m "Add character texture"

# Push to remote
git push origin main

# Pull from remote
git pull origin main
```

### 3. LFS Operations
```bash
# Check LFS status
git lfs status

# List LFS objects
git lfs ls-files

# Clean LFS cache
git lfs prune

# Verify LFS files
git lfs verify
```

## 🛠️ Best Practices

### 1. File Management
- Track only necessary files
- Use appropriate file formats
- Compress when possible
- Regular cleanup

### 2. Performance
- Optimize file sizes
- Use LFS efficiently
- Regular maintenance
- Monitor storage

### 3. Collaboration
- Document LFS usage
- Share LFS config
- Coordinate updates
- Regular sync

## 📋 Verification Steps

### 1. LFS Setup Verification
```bash
# Check LFS installation
git lfs version

# Verify tracking
git lfs track

# Check .gitattributes
cat .gitattributes
```

### 2. File Tracking Verification
```bash
# List tracked files
git lfs ls-files

# Check file status
git lfs status

# Verify file pointers
git lfs verify
```

### 3. Operation Verification
```bash
# Test file addition
git add assets/textures/test.png
git commit -m "Test LFS"

# Test file retrieval
git lfs pull
git lfs checkout
```

## 🎯 Common Commands

### 1. LFS Management
```bash
# Initialize LFS
git lfs install

# Track files
git lfs track "*.png"

# List tracked files
git lfs ls-files

# Clean up
git lfs prune
```

### 2. File Operations
```bash
# Add file
git add large-file.png

# Commit changes
git commit -m "Add large file"

# Push to remote
git push origin main

# Pull from remote
git pull origin main
```

### 3. Maintenance
```bash
# Check status
git lfs status

# Verify files
git lfs verify

# Clean cache
git lfs prune

# Update LFS
git lfs update
```

## 🔧 LFS Examples

### 1. Basic Setup
```bash
# Initialize repository
git init
git lfs install

# Configure tracking
git lfs track "*.png"
git lfs track "*.jpg"
git lfs track "*.fbx"

# Add and commit
git add .gitattributes
git commit -m "Configure Git LFS"
```

### 2. File Management
```bash
# Add large files
git add assets/textures/character.png
git add assets/models/character.fbx

# Commit changes
git commit -m "Add character assets"

# Push to remote
git push origin main
```

### 3. Maintenance
```bash
# Check status
git lfs status

# List tracked files
git lfs ls-files

# Clean up
git lfs prune
```

## 🆘 Need Help?

1. Check the [Advanced Topics Guide](../../docs/advanced-topics.md)
2. Review the [Troubleshooting Guide](../../docs/troubleshooting.md)
3. Join our [Discord Community](https://discord.gg/vihaya)

---

<div align="center">
  <p>Ready for more? Try our <a href="../07-git-submodules/README.md">Git Submodules Example</a>!</p>
</div> 