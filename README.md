# Vihaya Github Guide  🚀

Welcome to the official companion repository for the **"Git & GitHub Full Course for Beginners – 2025 Edition"** YouTube tutorial series by [Vishnu S](https://youtube.com/@Vihayaa), Founder of Vihaya. Connect with me on [LinkedIn](https://www.linkedin.com/in/vishnumeta/)!

This is an open-source project, and we welcome contributions from anyone! Whether you're a beginner or an expert, your input can help improve this resource for everyone.

## 📚 What's Inside?

This repository is your all-in-one learning hub for mastering Git and GitHub. Whether you're a complete beginner or looking to refresh your skills, you'll find everything you need here—step-by-step guides, real-world examples, hands-on exercises, and more.

---

## 🗂️ Repository Structure & Contents

```
├── 📁 docs/                  # In-depth guides and documentation
│   ├── getting-started.md         # Beginner setup and first steps
│   ├── git-fundamentals.md        # Core Git concepts and commands
│   ├── github-basics.md           # Introduction to GitHub features
│   ├── advanced-topics.md         # Advanced Git & GitHub workflows
│   ├── troubleshooting.md         # Solutions to common issues
│   └── best-practices.md          # Pro tips for effective usage
│
├── 📁 examples/             # Practical, real-world workflow examples
│   ├── 01-basic-workflow/         # Solo developer: basic Git workflow
│   ├── 02-collaborative-workflow/ # Team collaboration, PRs, code review
│   ├── 03-git-flow/               # Git Flow branching strategy
│   ├── 04-github-actions/         # CI/CD automation with GitHub Actions
│   ├── 05-git-hooks/              # Automating tasks with Git hooks
│   ├── 06-git-lfs/                # Managing large files with Git LFS
│   └── 07-git-submodules/         # Using submodules for dependencies
│
├── 📁 cheat-sheets/         # Quick reference guides
│   └── basic-commands.md          # Essential Git commands cheat sheet
│
├── 📁 practice/             # Hands-on exercises and challenges
│   ├── first-steps.md             # Beginner practice tasks
│   └── advanced-exercises.md      # Advanced Git & GitHub exercises
│
├── 📁 resources/            # Additional learning materials (links, books, tools)
│
├── .gitignore              # Recommended ignores for all major languages/tools
├── LICENSE                 # MIT License
├── CONTRIBUTING.md         # How to contribute to this repo
└── README.md               # You are here!
```

---

## 🚀 Getting Started

### What is Git?

Git is a distributed version control system that helps you track changes in your code. It allows you to collaborate with others, manage different versions of your project, and revert to previous states if needed.

### What is GitHub?

GitHub is a web-based platform that uses Git for version control. It provides a place to host your Git repositories, collaborate with others, and manage projects. GitHub also offers features like issues, pull requests, and GitHub Actions for automation.

### How to Download and Install Git

1. **Download Git**:
   - Visit the [official Git website](https://git-scm.com/downloads).
   - Choose your operating system (Windows, macOS, or Linux) and follow the installation instructions.

2. **Verify Installation**:
   - Open your terminal or command prompt and run:
     ```bash
     git --version
     ```
   - You should see the installed Git version.

### How to Get Started with GitHub

1. **Create a GitHub Account**:
   - Go to [GitHub](https://github.com/) and sign up for a free account.

2. **Set Up SSH Keys** (Optional but recommended):
   - Follow the [GitHub guide on SSH keys](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) to secure your connection.

3. **Create Your First Repository**:
   - Click on the "+" icon in the top right corner of GitHub and select "New repository."
   - Follow the prompts to create a new repository.

4. **Clone This Repository**:
   - Use the command:
     ```bash
     git clone https://github.com/yourusername/git-github-mastery.git
     ```

5. **Follow the Documentation**:
   - Start with the [Getting Started Guide](docs/getting-started.md) to learn the basics.

## 💻 Git Commands for Beginners

Here are the essential Git commands you'll need to get started. Copy and paste these commands in order as you follow along with the tutorial:

```bash
# Check Git version
git --version

# Set your name
git config --global user.name "Your Name"

# Set your email
git config --global user.email "your@email.com"

# Check your settings
git config --list

# Clone a repository from GitHub
git clone <paste link here>

# Check what has changed in your repository
git status

# Add files to staging area
git add filename.txt
git add .  # Add all files

# Commit your changes
git commit -m "Your commit message"

# Push your changes to GitHub
git push
```

# Init Commands – used to create a new git repo

```bash
# Initialize a new Git repository
git init

# Add remote origin
git remote add origin <link>

# Verify remote
git remote -v

# Check current branch
git branch

# Rename branch to main
git branch -M main

# Push to main branch
git push origin main
```

# Branch Commands

```bash
# Check branch
git branch

# Rename branch to main
git branch -M main

# Navigate to a branch
git checkout <branch name>

# Create and switch to a new branch
git checkout -b <new branch name>

# Delete a branch
git branch -d <branch name>
```

# Merging Code

## Way 1: Using Git Commands
```bash
# Compare commits, branches, files, and more
git diff <branch name>

# Merge two branches
git merge <branch name>
```

## Way 2: Using GitHub
- Create a Pull Request (PR)

# Pull Request

- To contribute your changes to a project, create a Pull Request (PR) on GitHub. This allows others to review and merge your changes.

# Pull Command

```bash
# Pull the latest changes from the remote repository
git pull
```

# Undoing Changes

## Case 1: Undo staged changes
```bash
# Unstage a specific file
git reset <file name>

# Unstage all files
git reset
```

## Case 2: Undo committed changes (for one commit)
```bash
git reset HEAD~1
```

## Case 3: Undo committed changes (for many commits)
```bash
# Reset to a specific commit (soft reset)
git reset <commit hash>

# Reset to a specific commit and discard all changes (hard reset)
git reset --hard <commit hash>
```

---

## 📝 Table of Contents

- [Getting Started Guide](docs/getting-started.md): Install Git, set up GitHub, and make your first commit
- [Git Fundamentals](docs/git-fundamentals.md): Understand branches, merges, rebases, and more
- [GitHub Basics](docs/github-basics.md): Learn about repositories, issues, pull requests, and collaboration
- [Advanced Topics](docs/advanced-topics.md): Explore Git Flow, submodules, LFS, hooks, and CI/CD
- [Best Practices](docs/best-practices.md): Tips for clean commits, branching, and team workflows
- [Troubleshooting Guide](docs/troubleshooting.md): Fix common Git and GitHub problems
- [Cheat Sheet](cheat-sheets/basic-commands.md): Quick reference for essential commands
- [Practice Exercises](practice/): Step-by-step tasks to build your skills
- [Examples](examples/): Realistic project scenarios for solo and team workflows

---

## 🤝 Contributing

We welcome contributions! Please read our [Contributing Guidelines](CONTRIBUTING.md) before submitting pull requests.

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

Special thanks to all contributors and the open-source community for their valuable input and support.

---

<div align="center">
  <p>Made with ❤️ by <a href="https://youtube.com/@Vihayaa">Vihaya</a></p>
  <p>Don't forget to ⭐ this repository!</p>
</div> 
