# Getting Started with Git & GitHub 🚀

Welcome to your journey of learning Git and GitHub! This guide will help you set up your development environment and take your first steps into version control.

## 📋 Prerequisites

Before you begin, make sure you have:

- A computer running Windows, macOS, or Linux
- Basic understanding of command line/terminal usage
- Internet connection
- A GitHub account (we'll help you create one if you don't have it)

## 🛠️ Installation

### Installing Git

#### Windows
1. Download Git from [git-scm.com](https://git-scm.com/download/win)
2. Run the installer and follow the setup wizard
3. Verify installation by opening PowerShell and typing:
   ```bash
   git --version
   ```

#### macOS
1. Install via Homebrew:
   ```bash
   brew install git
   ```
2. Or download from [git-scm.com](https://git-scm.com/download/mac)

#### Linux (Ubuntu/Debian)
```bash
sudo apt-get update
sudo apt-get install git
```

### Creating a GitHub Account

1. Visit [github.com](https://github.com)
2. Click "Sign Up"
3. Follow the registration process
4. Verify your email address

## 🔑 Initial Setup

### Configure Git

Set up your identity:
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

### Connect to GitHub

1. Generate an SSH key:
   ```bash
   ssh-keygen -t ed25519 -C "your.email@example.com"
   ```

2. Add the SSH key to your GitHub account:
   - Copy your public key:
     ```bash
     cat ~/.ssh/id_ed25519.pub
     ```
   - Go to GitHub → Settings → SSH and GPG keys
   - Click "New SSH key"
   - Paste your key and save

## 🎯 Your First Repository

1. Create a new repository on GitHub:
   - Click the "+" icon in the top right
   - Select "New repository"
   - Name your repository
   - Choose public or private
   - Click "Create repository"

2. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/your-repo.git
   ```

3. Make your first commit:
   ```bash
   cd your-repo
   echo "# My First Repository" > README.md
   git add README.md
   git commit -m "Initial commit"
   git push origin main
   ```

## 📚 Next Steps

1. Read through the [Git Fundamentals](git-fundamentals.md) guide
2. Try the [Basic Git Commands](cheat-sheets/basic-commands.md) cheat sheet
3. Complete the [First Steps](practice/first-steps.md) practice exercise

## 🆘 Need Help?

- Check our [Troubleshooting Guide](troubleshooting.md)
- Visit [GitHub Help](https://help.github.com)
- Join our [Discord Community](https://discord.gg/vihaya) (placeholder link)

## 📝 Additional Resources

- [Git Documentation](https://git-scm.com/doc)
- [GitHub Learning Lab](https://lab.github.com)
- [GitHub Skills](https://skills.github.com)

---

<div align="center">
  <p>Ready to start your Git journey? Let's move on to <a href="git-fundamentals.md">Git Fundamentals</a>!</p>
</div> 