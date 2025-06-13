# Basic Git Workflow Example 📝

This example demonstrates a basic Git workflow using a simple project. Follow along to learn essential Git commands and practices.

## 🎯 Project Overview

A simple task management application that demonstrates:
- Basic Git commands
- Branch management
- Commit practices
- Remote repository interaction

## 📁 Project Structure

```
task-manager/
├── README.md
├── index.html
├── styles.css
└── app.js
```

## 🚀 Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/task-manager.git
   cd task-manager
   ```

2. Create initial files:
   ```bash
   # Create HTML file
   echo "<!DOCTYPE html>
   <html>
   <head>
       <title>Task Manager</title>
       <link rel='stylesheet' href='styles.css'>
   </head>
   <body>
       <h1>Task Manager</h1>
       <div id='app'></div>
       <script src='app.js'></script>
   </body>
   </html>" > index.html

   # Create CSS file
   echo "body {
       font-family: Arial, sans-serif;
       margin: 20px;
   }" > styles.css

   # Create JavaScript file
   echo "// Task Manager Application
   const app = {
       tasks: [],
       init() {
           console.log('Task Manager initialized');
       }
   };

   app.init();" > app.js
   ```

3. Initialize Git repository:
   ```bash
   git init
   git add .
   git commit -m "Initial commit: Basic project structure"
   ```

## 📝 Basic Workflow

### 1. Create a Feature Branch
```bash
git checkout -b feature/add-task
```

### 2. Make Changes
Add task functionality to `app.js`:
```javascript
// Add to app.js
app.addTask = function(task) {
    this.tasks.push(task);
    console.log('Task added:', task);
};
```

### 3. Commit Changes
```bash
git add app.js
git commit -m "Add task functionality"
```

### 4. Switch to Main Branch
```bash
git checkout main
```

### 5. Merge Feature
```bash
git merge feature/add-task
```

## 🔄 Common Operations

### 1. View Status
```bash
git status
```

### 2. View History
```bash
git log --oneline
```

### 3. View Changes
```bash
git diff
```

## 📚 Learning Points

- Repository initialization
- Basic Git commands
- Branch management
- Commit practices
- Merge operations

## 🎯 Practice Exercises

1. Add a new feature branch
2. Make changes to the CSS
3. Commit your changes
4. Merge back to main
5. Push to remote repository

## 📋 Verification Steps

1. Check repository status:
   ```bash
   git status
   ```

2. View commit history:
   ```bash
   git log --oneline
   ```

3. Test the application:
   - Open `index.html` in a browser
   - Check browser console for output

## 🆘 Need Help?

1. Check the [Basic Commands Cheat Sheet](../../cheat-sheets/basic-commands.md)
2. Review the [Getting Started Guide](../../docs/getting-started.md)
3. Join our [Discord Community](https://discord.gg/vihaya)

---

<div align="center">
  <p>Ready for more? Try our <a href="../02-collaborative-workflow/README.md">Collaborative Workflow Example</a>!</p>
</div> 