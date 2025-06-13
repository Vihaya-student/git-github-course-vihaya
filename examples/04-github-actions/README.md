# GitHub Actions Workflow Example ⚡

This example demonstrates how to implement CI/CD workflows using GitHub Actions. Learn how to automate testing, building, and deployment processes.

## 🎯 Project Overview

A Node.js application that demonstrates:
- Automated testing
- Continuous Integration
- Continuous Deployment
- Code quality checks
- Security scanning

## 📁 Project Structure

```
node-app/
├── .github/
│   └── workflows/
│       ├── ci.yml
│       ├── cd.yml
│       └── security.yml
├── src/
│   ├── index.js
│   └── utils.js
├── tests/
│   └── index.test.js
├── package.json
└── README.md
```

## 🚀 Getting Started

### 1. Create Workflow Directory
```bash
mkdir -p .github/workflows
```

### 2. Create CI Workflow
Create `.github/workflows/ci.yml`:
```yaml
name: CI

on:
  push:
    branches: [ main, develop ]
  pull_request:
    branches: [ main, develop ]

jobs:
  test:
    runs-on: ubuntu-latest
    
    strategy:
      matrix:
        node-version: [14.x, 16.x, 18.x]

    steps:
    - uses: actions/checkout@v3
    
    - name: Use Node.js ${{ matrix.node-version }}
      uses: actions/setup-node@v3
      with:
        node-version: ${{ matrix.node-version }}
        cache: 'npm'
    
    - name: Install dependencies
      run: npm ci
    
    - name: Run tests
      run: npm test
    
    - name: Run linting
      run: npm run lint
```

### 3. Create CD Workflow
Create `.github/workflows/cd.yml`:
```yaml
name: CD

on:
  push:
    tags:
      - 'v*'

jobs:
  deploy:
    runs-on: ubuntu-latest
    
    steps:
    - uses: actions/checkout@v3
    
    - name: Use Node.js
      uses: actions/setup-node@v3
      with:
        node-version: '18.x'
        cache: 'npm'
    
    - name: Install dependencies
      run: npm ci
    
    - name: Build
      run: npm run build
    
    - name: Deploy to production
      run: |
        echo "Deploying version ${{ github.ref_name }}"
        # Add your deployment commands here
```

### 4. Create Security Workflow
Create `.github/workflows/security.yml`:
```yaml
name: Security

on:
  push:
    branches: [ main, develop ]
  pull_request:
    branches: [ main, develop ]
  schedule:
    - cron: '0 0 * * 0'  # Run weekly

jobs:
  security:
    runs-on: ubuntu-latest
    
    steps:
    - uses: actions/checkout@v3
    
    - name: Run security audit
      run: npm audit
    
    - name: Run dependency check
      uses: snyk/actions/node@master
      env:
        SNYK_TOKEN: ${{ secrets.SNYK_TOKEN }}
```

## 📝 Common Scenarios

### 1. Running Tests
```bash
# Local testing
npm test

# View test coverage
npm run test:coverage
```

### 2. Building Application
```bash
# Local build
npm run build

# Production build
NODE_ENV=production npm run build
```

### 3. Security Checks
```bash
# Run security audit
npm audit

# Fix vulnerabilities
npm audit fix
```

## 🛠️ Best Practices

### 1. Workflow Organization
- Separate CI and CD workflows
- Use reusable workflows
- Implement proper caching
- Set up branch protection

### 2. Security
- Regular security scans
- Dependency updates
- Secret management
- Code signing

### 3. Performance
- Optimize workflow speed
- Use matrix builds
- Implement caching
- Parallel jobs

## 📋 Verification Steps

### 1. CI Verification
```bash
# Check workflow runs
gh run list

# View workflow logs
gh run view <run-id>

# Check test results
npm test
```

### 2. CD Verification
```bash
# Check deployment status
gh run list --workflow=cd.yml

# Verify deployment
curl https://your-app-url/health
```

### 3. Security Verification
```bash
# Check security scan
gh run list --workflow=security.yml

# View security report
npm audit
```

## 🎯 Common Commands

### 1. GitHub CLI
```bash
# List workflows
gh workflow list

# View workflow runs
gh run list

# Rerun workflow
gh run rerun <run-id>
```

### 2. Local Testing
```bash
# Run tests
npm test

# Run linting
npm run lint

# Build application
npm run build
```

### 3. Security
```bash
# Audit dependencies
npm audit

# Fix vulnerabilities
npm audit fix

# Update dependencies
npm update
```

## 🔧 Workflow Examples

### 1. Node.js Application
```yaml
name: Node.js CI

on: [push, pull_request]

jobs:
  build:
    runs-on: ubuntu-latest
    
    steps:
    - uses: actions/checkout@v3
    - uses: actions/setup-node@v3
      with:
        node-version: '18.x'
    - run: npm ci
    - run: npm test
```

### 2. Docker Container
```yaml
name: Docker CI

on: [push, pull_request]

jobs:
  build:
    runs-on: ubuntu-latest
    
    steps:
    - uses: actions/checkout@v3
    - name: Build Docker image
      run: docker build -t myapp .
    - name: Run tests
      run: docker run myapp npm test
```

### 3. Deployment
```yaml
name: Deploy

on:
  push:
    tags:
      - 'v*'

jobs:
  deploy:
    runs-on: ubuntu-latest
    
    steps:
    - uses: actions/checkout@v3
    - name: Deploy to production
      run: |
        echo "Deploying ${{ github.ref_name }}"
        # Add deployment steps
```

## 🆘 Need Help?

1. Check the [Advanced Topics Guide](../../docs/advanced-topics.md)
2. Review the [Troubleshooting Guide](../../docs/troubleshooting.md)
3. Join our [Discord Community](https://discord.gg/vihaya)

---

<div align="center">
  <p>Ready for more? Try our <a href="../05-git-hooks/README.md">Git Hooks Example</a>!</p>
</div> 