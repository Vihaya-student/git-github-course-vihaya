# Collaborative Git Workflow Example 👥

This example demonstrates how to work collaboratively on a project using Git and GitHub. Learn how to handle multiple developers, pull requests, and code reviews.

## 🎯 Project Overview

A collaborative blog platform that demonstrates:
- Team collaboration
- Pull request workflow
- Code review process
- Conflict resolution
- Branch protection

## 📁 Project Structure

```
blog-platform/
├── README.md
├── src/
│   ├── components/
│   │   ├── Header.js
│   │   ├── Footer.js
│   │   └── Post.js
│   ├── pages/
│   │   ├── Home.js
│   │   └── Post.js
│   └── styles/
│       └── main.css
├── tests/
│   └── components.test.js
└── package.json
```

## 👥 Team Setup

### 1. Repository Setup
```bash
# Create repository
git init
git add .
git commit -m "Initial commit: Project structure"
git remote add origin https://github.com/team/blog-platform.git
git push -u origin main
```

### 2. Branch Protection
1. Go to repository settings
2. Enable branch protection for `main`
3. Require pull request reviews
4. Require status checks

## 🔄 Collaborative Workflow

### 1. Feature Development
```bash
# Create feature branch
git checkout -b feature/user-authentication

# Make changes
# ... work on feature ...

# Commit changes
git add .
git commit -m "Add user authentication"

# Push to remote
git push origin feature/user-authentication
```

### 2. Pull Request Process
1. Create pull request on GitHub
2. Add description and reviewers
3. Link related issues
4. Request review from team members

### 3. Code Review
- Review changes
- Add comments
- Request changes if needed
- Approve when ready

### 4. Merge Process
```bash
# Update local main
git checkout main
git pull origin main

# Merge feature
git merge feature/user-authentication

# Push changes
git push origin main
```

## 🛠️ Common Scenarios

### 1. Resolving Conflicts
```bash
# Update feature branch
git checkout feature/user-authentication
git pull origin main

# Resolve conflicts
# ... edit files ...

# Commit resolution
git add .
git commit -m "Resolve merge conflicts"

# Push changes
git push origin feature/user-authentication
```

### 2. Code Review Feedback
```bash
# Make requested changes
git add .
git commit -m "Address review feedback"

# Push updates
git push origin feature/user-authentication
```

### 3. Rebase Feature Branch
```bash
# Update feature branch
git checkout feature/user-authentication
git rebase main

# Resolve conflicts if any
# ... resolve conflicts ...

# Force push (if needed)
git push -f origin feature/user-authentication
```

## 📝 Best Practices

### 1. Branch Naming
- `feature/` - New features
- `bugfix/` - Bug fixes
- `hotfix/` - Urgent fixes
- `release/` - Release preparation

### 2. Commit Messages
- Use present tense
- Be descriptive
- Reference issues
- Keep it concise

### 3. Pull Requests
- Clear description
- Link related issues
- Add screenshots if needed
- Request specific reviewers

## 🎯 Team Roles

### 1. Developer
- Create feature branches
- Write code
- Create pull requests
- Address feedback

### 2. Reviewer
- Review code
- Provide feedback
- Approve changes
- Ensure quality

### 3. Maintainer
- Merge pull requests
- Manage releases
- Handle conflicts
- Maintain documentation

## 📋 Verification Steps

1. Check branch protection:
   - Verify main branch is protected
   - Confirm review requirements
   - Test status checks

2. Test collaboration:
   - Create feature branch
   - Make changes
   - Create pull request
   - Complete review process

3. Verify merge:
   - Check commit history
   - Verify changes
   - Test functionality

## 🆘 Need Help?

1. Check the [Advanced Topics Guide](../../docs/advanced-topics.md)
2. Review the [Troubleshooting Guide](../../docs/troubleshooting.md)
3. Join our [Discord Community](https://discord.gg/vihaya)

---

<div align="center">
  <p>Ready for more? Try our <a href="../03-git-flow/README.md">Git Flow Example</a>!</p>
</div> 