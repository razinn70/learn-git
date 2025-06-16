# The Complete Git & GitHub Mastery Course

> *"Version control is not just a tool—it's the foundation of modern software development. Master it, and you master the art of collaborative innovation."*  
> — **Dr. Rajin Uddin**, Stanford Computer Science

---

## 📚 Course Overview

**Welcome to the most comprehensive Git and GitHub course designed for the next generation of developers.**

This course transforms beginners into Git professionals through hands-on learning, real-world scenarios, and industry best practices. Whether you're a computer science student, bootcamp graduate, or self-taught developer, this curriculum will elevate your version control expertise to enterprise level.

### 🎯 What You'll Master

- **Core Git Concepts**: From init to advanced workflows
- **GitHub Integration**: Seamless collaboration and project management
- **Authentication Mastery**: SSH keys, Personal Access Tokens, and security
- **Branching Strategies**: Industry-standard workflows and merge techniques
- **Collaboration Patterns**: Pull requests, code reviews, and team workflows
- **Performance Optimization**: Understanding Git's efficiency and best practices
- **Professional Development**: Enterprise-grade version control skills

### 🏆 Course Value

**Investment**: $5,000  
**Value Delivered**: Career-changing Git expertise used by 100M+ developers worldwide  
**Outcome**: Master the tool that powers Google, Microsoft, Facebook, and every modern tech company

---

## 📋 Table of Contents

### **Module 1: Foundations**
1. [Understanding Version Control](#understanding-version-control)
2. [Git vs GitHub: The Essential Distinction](#git-vs-github-the-essential-distinction)
3. [Installation and Initial Setup](#installation-and-initial-setup)
4. [Your First Repository](#your-first-repository)

### **Module 2: Core Operations**
5. [The Git Workflow Trinity: Add, Commit, Push](#the-git-workflow-trinity)
6. [Understanding Git's Three States](#understanding-gits-three-states)
7. [Remote Repositories and Cloning](#remote-repositories-and-cloning)
8. [Pull vs Fetch: The Critical Difference](#pull-vs-fetch-the-critical-difference)

### **Module 3: Authentication Mastery**
9. [HTTPS Authentication with Personal Access Tokens](#https-authentication-with-personal-access-tokens)
10. [SSH Key Authentication](#ssh-key-authentication)
11. [Security Best Practices](#security-best-practices)
12. [Multi-Device Authentication Strategies](#multi-device-authentication-strategies)

### **Module 4: Branching and Merging**
13. [Branch Theory and Practice](#branch-theory-and-practice)
14. [Merge Strategies and Conflict Resolution](#merge-strategies-and-conflict-resolution)
15. [Advanced Branching Workflows](#advanced-branching-workflows)
16. [Pull Requests: Code Review Excellence](#pull-requests-code-review-excellence)

### **Module 5: Performance and Optimization**
17. [Git's Efficiency Engine](#gits-efficiency-engine)
18. [Repository Management](#repository-management)
19. [Large File Handling](#large-file-handling)
20. [Performance Monitoring](#performance-monitoring)

### **Module 6: Professional Workflows**
21. [Industry Standard Workflows](#industry-standard-workflows)
22. [Team Collaboration Patterns](#team-collaboration-patterns)
23. [CI/CD Integration](#cicd-integration)
24. [Advanced Git Commands](#advanced-git-commands)

---

## Module 1: Foundations

### Understanding Version Control

#### The Problem Version Control Solves

Imagine you're writing a novel. You have:
- `novel_draft1.doc`
- `novel_draft2_revised.doc`
- `novel_draft2_revised_FINAL.doc`
- `novel_draft2_revised_FINAL_actually_final.doc`
- `novel_draft2_revised_FINAL_actually_final_v2.doc`

This chaos is exactly what version control prevents in software development.

#### What is Version Control?

Version control is a system that:
- **Tracks changes** to files over time
- **Stores complete history** of modifications
- **Enables collaboration** without conflicts
- **Provides backup** and recovery mechanisms
- **Supports branching** for parallel development

#### Why Git Dominates

**Git Market Share**: 95%+ of developers worldwide  
**Used By**: Google, Microsoft, Facebook, Netflix, Tesla, SpaceX  
**Repository Count**: 200M+ repositories on GitHub alone

**Key Advantages**:
- **Distributed**: Every developer has complete history
- **Fast**: Optimized for speed and efficiency
- **Reliable**: Cryptographic integrity of data
- **Flexible**: Supports any workflow
- **Industry Standard**: Required skill for modern development

---

### Git vs GitHub: The Essential Distinction

#### Git: The Version Control System

```bash
# Git is the command-line tool
git init
git add .
git commit -m "Initial commit"
git push origin main
```

**Git is**:
- Software installed on your computer
- Works entirely offline
- Tracks changes in local repositories
- Created by Linus Torvalds (Linux creator)

#### GitHub: The Cloud Platform

**GitHub is**:
- Web-based hosting service for Git repositories
- Adds collaboration features (pull requests, issues, wikis)
- Provides remote backup for your code
- Social network for developers
- Owned by Microsoft (acquired for $7.5 billion)

#### The Relationship

```
┌─────────────────┐    git push     ┌─────────────────┐
│   Local Git     │ ──────────────→ │     GitHub      │
│   Repository    │                 │   (Remote)      │
│                 │ ←────────────── │                 │
└─────────────────┘    git pull     └─────────────────┘
```

**Analogy**: Git is like Microsoft Word (the software), GitHub is like Google Drive (the cloud storage).

---

### Installation and Initial Setup

#### Installing Git

**Windows**:
1. Download from [git-scm.com](https://git-scm.com/download/win)
2. Run installer with default options
3. Ensure "Git Bash" is selected

**macOS**:
```bash
# Using Homebrew
brew install git

# Or download from git-scm.com
```

**Linux (Ubuntu/Debian)**:
```bash
sudo apt update
sudo apt install git
```

#### Verification

```bash
git --version
# Should output: git version 2.x.x
```

#### Essential Configuration

```bash
# Set your identity (required for commits)
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

# Set default branch name
git config --global init.defaultBranch main

# Enable colored output
git config --global color.ui auto

# Set default editor (optional)
git config --global core.editor "code --wait"  # VS Code

# View all configuration
git config --global --list
```

#### Understanding Configuration Levels

```bash
# System-wide (all users)
git config --system

# User-specific (your account)
git config --global

# Repository-specific (current project only)
git config --local
```

**Priority**: Local > Global > System

---

### Your First Repository

#### Method 1: Starting from Scratch

```bash
# Create project directory
mkdir my-first-project
cd my-first-project

# Initialize Git repository
git init

# Create a file
echo "# My First Project" > README.md

# Check status
git status

# Stage the file
git add README.md

# Commit the change
git commit -m "Initial commit: Add README"

# View history
git log --oneline
```

#### Method 2: Cloning from GitHub

```bash
# Clone existing repository
git clone https://github.com/username/repository.git

# Navigate into the cloned directory
cd repository

# Check remote connection
git remote -v
```

#### Understanding the .git Directory

```bash
# View hidden .git directory
ls -la

# Explore Git's internal structure
ls .git/
```

**What's inside .git/**:
- `config`: Repository-specific configuration
- `HEAD`: Points to current branch
- `objects/`: All file contents and commits
- `refs/`: Branch and tag references
- `index`: Staging area contents

---

## Module 2: Core Operations

### The Git Workflow Trinity

The three fundamental operations that power all Git workflows:

#### 1. Add (Staging)

```bash
# Stage specific file
git add filename.txt

# Stage all changes
git add .

# Stage all files of specific type
git add *.js

# Interactive staging
git add -i

# Stage only tracked files
git add -u
```

#### 2. Commit (Saving)

```bash
# Commit with message
git commit -m "Add user authentication feature"

# Commit with detailed message
git commit -m "Add user authentication" -m "- Implement login/logout\n- Add password hashing\n- Create user sessions"

# Commit and stage all tracked files
git commit -am "Quick fix for bug #123"

# Amend last commit
git commit --amend -m "Corrected commit message"
```

#### 3. Push (Sharing)

```bash
# Push to default remote and branch
git push

# Push to specific remote and branch
git push origin main

# Push new branch to remote
git push -u origin feature-branch

# Force push (dangerous!)
git push --force-with-lease
```

### Understanding Git's Three States

```
┌─────────────┐    git add    ┌─────────────┐   git commit   ┌─────────────┐
│  Working    │ ─────────────→│   Staging   │ ─────────────→│ Repository  │
│ Directory   │               │    Area     │               │ (.git dir)  │
│             │←─────────────│             │←─────────────│             │
└─────────────┘   checkout    └─────────────┘   git reset   └─────────────┘
   (Modified)                    (Staged)                    (Committed)
```

#### Working Directory
- Files you're currently editing
- Can be modified, untracked, or ignored
- This is where you make changes

#### Staging Area (Index)
- Prepared changes ready for commit
- Allows selective committing
- Think of it as a "shopping cart" for commits

#### Repository (.git directory)
- Committed changes with complete history
- Permanent record of your project evolution
- Safe, version-controlled storage

### Checking Status and History

```bash
# See current state
git status

# Concise status
git status -s

# View commit history
git log

# Compact history
git log --oneline

# Graphical history
git log --graph --oneline --all

# History with file changes
git log --stat

# History with actual changes
git log -p
```

---

### Remote Repositories and Cloning

#### Understanding Remotes

A remote is a version of your repository hosted somewhere else (GitHub, GitLab, etc.).

```bash
# View remotes
git remote -v

# Add remote
git remote add origin https://github.com/username/repo.git

# Change remote URL
git remote set-url origin https://github.com/username/new-repo.git

# Remove remote
git remote remove origin
```

#### Cloning Strategies

```bash
# Full clone
git clone https://github.com/username/repo.git

# Clone to specific directory
git clone https://github.com/username/repo.git my-project

# Shallow clone (recent history only)
git clone --depth 1 https://github.com/username/repo.git

# Clone specific branch
git clone -b feature-branch https://github.com/username/repo.git
```

---

### Pull vs Fetch: The Critical Difference

This distinction separates beginners from professionals.

#### Fetch: Download Only

```bash
# Download changes without merging
git fetch origin

# Fetch specific branch
git fetch origin main

# Fetch all remotes
git fetch --all
```

**What fetch does**:
- Downloads commits from remote
- Updates remote-tracking branches (origin/main)
- **Does NOT** modify your working directory
- **Does NOT** merge changes automatically

#### Pull: Download + Merge

```bash
# Fetch and merge in one command
git pull origin main

# Pull with rebase instead of merge
git pull --rebase origin main

# Pull current branch from default remote
git pull
```

**What pull does**:
- Executes `git fetch` first
- Then executes `git merge` (or `git rebase`)
- Modifies your working directory
- Can create merge conflicts

#### Professional Workflow Recommendation

```bash
# Recommended: Fetch first, review, then merge
git fetch origin
git log HEAD..origin/main --oneline  # See what's new
git diff HEAD..origin/main           # See changes
git merge origin/main                # Merge when ready

# Alternative: Use pull for simple cases
git pull origin main  # When you trust the changes
```

#### Visualizing the Difference

**Before Fetch/Pull**:
```
(local)  A---B---C main
                \
(remote)         D---E origin/main
```

**After Fetch**:
```
(local)  A---B---C main
                \
(remote)         D---E origin/main (updated locally)
```

**After Pull**:
```
(local)  A---B---C---F main (F is merge commit)
                \   /
(remote)         D-E origin/main
```

---

## Module 3: Authentication Mastery

### HTTPS Authentication with Personal Access Tokens

#### Why Personal Access Tokens?

GitHub discontinued password authentication for security reasons. Personal Access Tokens (PATs) provide:

- **Enhanced Security**: Scoped permissions
- **Revocable Access**: Delete without changing account password
- **Audit Trail**: Track which token performed actions
- **Expiration Control**: Automatic security through expiry

#### Creating Personal Access Tokens

1. **Navigate to GitHub Settings**:
   - Go to `https://github.com/settings/tokens`
   - Click "Generate new token" → "Generate new token (classic)"

2. **Configure Token**:
   ```
   Note: "Development Laptop - Git Operations"
   Expiration: 90 days (recommended)
   Scopes: ✓ repo (for full repository access)
   ```

3. **Copy Token Immediately**:
   - GitHub shows it only once
   - Store securely (password manager recommended)

#### Using Tokens with Git

```bash
# Configure repository for HTTPS
git remote add origin https://github.com/username/repo.git

# First push will prompt for credentials
git push origin main
# Username: your-github-username
# Password: ghp_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx

# Enable credential storage
git config --global credential.helper store
```

#### Token Security Best Practices

```bash
# Device-specific tokens
"Work Laptop - Git Operations - June 2025"
"Home Desktop - Development - June 2025"
"MacBook Pro - Travel - June 2025"

# Regular rotation (before expiry)
# Minimal scope (only required permissions)
# Immediate revocation if compromised
```

#### Multi-Device Token Strategy

**Option 1: Separate Tokens (Recommended)**
```bash
# Benefits:
# - Enhanced security
# - Device-specific tracking
# - Granular revocation
# - Audit trail clarity
```

**Option 2: Shared Token (Simpler)**
```bash
# Benefits:
# - Single token management
# - Immediate cross-device access
# 
# Drawbacks:
# - Security risk if one device compromised
# - No device-specific tracking
```

---

### SSH Key Authentication

#### Understanding SSH Keys

SSH (Secure Shell) uses public-key cryptography:

```
┌─────────────────┐                    ┌─────────────────┐
│   Your Device   │                    │     GitHub      │
│                 │                    │                 │
│ Private Key     │ ←──── Secure ────→ │ Public Key      │
│ (Keep Secret!)  │      Channel       │ (Safe to Share) │
└─────────────────┘                    └─────────────────┘
```

#### SSH Key Generation

```bash
# Generate ED25519 key (recommended)
ssh-keygen -t ed25519 -C "your.email@example.com" -f ~/.ssh/id_ed25519

# Alternative: RSA key (if ED25519 not supported)
ssh-keygen -t rsa -b 4096 -C "your.email@example.com" -f ~/.ssh/id_rsa

# View public key
cat ~/.ssh/id_ed25519.pub
```

#### Adding SSH Key to GitHub

1. **Copy Public Key**:
   ```bash
   cat ~/.ssh/id_ed25519.pub
   # Copy the entire output
   ```

2. **Add to GitHub**:
   - Go to `https://github.com/settings/keys`
   - Click "New SSH key"
   - Title: "Development Laptop - June 2025"
   - Key: Paste your public key
   - Click "Add SSH key"

#### Testing SSH Connection

```bash
# Test authentication
ssh -T git@github.com

# Expected output:
# Hi username! You've successfully authenticated, but GitHub does not provide shell access.
```

#### Using SSH with Git

```bash
# Clone with SSH
git clone git@github.com:username/repo.git

# Change existing repository to SSH
git remote set-url origin git@github.com:username/repo.git

# Verify remote URL
git remote -v
# Should show: git@github.com:username/repo.git
```

#### SSH vs HTTPS Comparison

| Feature | SSH | HTTPS |
|---------|-----|-------|
| **Setup Complexity** | Moderate | Simple |
| **Security** | Excellent | Good |
| **Firewall Issues** | Sometimes | Rarely |
| **Token Expiry** | Never | Yes |
| **Enterprise Support** | Universal | Universal |
| **Recommended For** | Power Users | Beginners |

---

### Security Best Practices

#### Token Management

```bash
# Regular audit of active tokens
# Visit: https://github.com/settings/tokens

# Remove unused tokens immediately
# Set expiration dates (90 days recommended)
# Use descriptive names with device and date
# Store tokens in password managers, not plain text
```

#### SSH Key Security

```bash
# Set proper permissions
chmod 700 ~/.ssh
chmod 600 ~/.ssh/id_ed25519
chmod 644 ~/.ssh/id_ed25519.pub

# Use passphrase for private keys
ssh-keygen -p -f ~/.ssh/id_ed25519

# Enable SSH agent for convenience
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

#### Environment-Specific Security

**Development Environment**:
```bash
# Use separate tokens/keys for development
# Regular rotation (90 days)
# Minimal required permissions
```

**Production Environment**:
```bash
# Dedicated service accounts
# Restricted IP access
# Audit logging enabled
# Emergency revocation procedures
```

---

## Module 4: Branching and Merging

### Branch Theory and Practice

#### Understanding Branches

Branches are parallel universes of your codebase:

```
        A---B---C main
             \
              D---E feature-login
                   \
                    F---G feature-ui-update
```

Each branch represents an independent line of development.

#### Why Branches Matter

1. **Isolation**: Work on features without affecting main code
2. **Collaboration**: Multiple developers work simultaneously
3. **Experimentation**: Try ideas without risk
4. **Release Management**: Maintain stable releases
5. **Code Review**: Structured review process through pull requests

#### Basic Branch Operations

```bash
# View all branches
git branch -a

# Create new branch
git branch feature-user-auth

# Switch to branch
git checkout feature-user-auth

# Create and switch in one command
git checkout -b feature-user-auth

# Modern syntax (Git 2.23+)
git switch feature-user-auth
git switch -c feature-user-auth  # create and switch

# Delete branch
git branch -d feature-user-auth

# Force delete (unmerged changes)
git branch -D feature-user-auth
```

#### Professional Branching Workflow

```bash
# 1. Start from main branch
git checkout main
git pull origin main

# 2. Create feature branch
git checkout -b feature/add-payment-processing

# 3. Work on feature
# ... make changes ...
git add .
git commit -m "Add payment gateway integration"

# 4. Push feature branch
git push -u origin feature/add-payment-processing

# 5. Create pull request on GitHub
# 6. After review and approval, merge
# 7. Delete feature branch
git branch -d feature/add-payment-processing
```

---

### Merge Strategies and Conflict Resolution

#### Types of Merges

**1. Fast-Forward Merge**:
```
Before:  A---B---C main
              \
               D---E feature

After:   A---B---C---D---E main
```

**2. Merge Commit**:
```
Before:  A---B---C main
              \
               D---E feature

After:   A---B---C---F main
              \     /
               D---E
```

**3. Rebase**:
```
Before:  A---B---C main
              \
               D---E feature

After:   A---B---C---D'---E' main
```

#### Merge Commands

```bash
# Basic merge
git checkout main
git merge feature-branch

# No fast-forward (always create merge commit)
git merge --no-ff feature-branch

# Squash merge (combine all commits)
git merge --squash feature-branch

# Rebase instead of merge
git rebase main feature-branch
```

#### Conflict Resolution

Conflicts occur when Git can't automatically merge changes:

```bash
# When conflict occurs
git status  # Shows conflicted files

# Open conflicted file - you'll see:
<<<<<<< HEAD
Your changes
=======
Incoming changes
>>>>>>> feature-branch

# Resolve manually:
# 1. Edit file to desired state
# 2. Remove conflict markers
# 3. Stage resolved file
git add conflicted-file.txt

# Complete the merge
git commit -m "Resolve merge conflict in user authentication"
```

#### Professional Conflict Resolution

```bash
# Use merge tool
git mergetool

# Abort merge if needed
git merge --abort

# View conflicts clearly
git diff --name-only --diff-filter=U  # List conflicted files
git show :1:filename  # Common ancestor
git show :2:filename  # Your version
git show :3:filename  # Their version
```

---

### Advanced Branching Workflows

#### Git Flow

A popular branching model for release management:

```
main     ────────o────────o────────o────────
                /          /        /
develop  ──────o────o────o────o────o────o───
               \    /      \    /
feature   ───────o─o        o──o
                /
release  ──────o─────────o──
                         /
hotfix   ───────────────o
```

**Branch Types**:
- **main**: Production-ready code
- **develop**: Integration branch for features
- **feature/***: Individual features
- **release/***: Release preparation
- **hotfix/***: Critical production fixes

#### GitHub Flow (Simpler)

```
main     ────o─────o─────o─────o─────o────
             \     /     /     /
feature   ────o───o ────o ────o
```

**Workflow**:
1. Create branch from main
2. Develop feature
3. Open pull request
4. Review and discuss
5. Merge to main
6. Delete feature branch

#### Feature Branch Naming Conventions

```bash
# Good examples:
feature/user-authentication
feature/payment-gateway
bugfix/login-validation-error
hotfix/security-vulnerability
improvement/loading-performance

# Branch prefixes:
feature/    # New features
bugfix/     # Bug fixes
hotfix/     # Critical fixes
improvement/# Enhancements
refactor/   # Code refactoring
docs/       # Documentation
test/       # Testing
```

---

### Pull Requests: Code Review Excellence

#### What is a Pull Request?

A pull request (PR) is a request to merge code from one branch into another, with:
- **Code Review**: Team members examine changes
- **Discussion**: Comments and suggestions
- **Testing**: Automated checks and manual testing
- **Documentation**: Description of changes and rationale

#### Creating Effective Pull Requests

**1. Preparation**:
```bash
# Ensure branch is up to date
git checkout main
git pull origin main
git checkout feature-branch
git rebase main

# Clean commit history
git log --oneline  # Review commits
git rebase -i HEAD~3  # Interactive rebase to clean up

# Push feature branch
git push origin feature-branch
```

**2. PR Description Template**:
```markdown
## Description
Brief summary of changes and motivation.

## Changes Made
- [ ] Added user authentication system
- [ ] Implemented password hashing
- [ ] Created login/logout endpoints
- [ ] Added user session management

## Testing
- [ ] Unit tests pass
- [ ] Integration tests pass
- [ ] Manual testing completed

## Screenshots
![Login Page](screenshot.png)

## Related Issues
Closes #123
References #456
```

#### Code Review Best Practices

**For Authors**:
```bash
# Small, focused PRs
# Clear commit messages
# Self-review before submitting
# Respond promptly to feedback
# Test thoroughly
```

**For Reviewers**:
```bash
# Be constructive and respectful
# Focus on code, not person
# Explain reasoning for suggestions
# Approve when ready
# Request changes when needed
```

#### PR Workflow Commands

```bash
# Check out PR locally for testing
git fetch origin pull/123/head:pr-123
git checkout pr-123

# Update PR branch
git checkout feature-branch
git rebase main
git push --force-with-lease origin feature-branch

# Clean up after merge
git checkout main
git pull origin main
git branch -d feature-branch
git push origin --delete feature-branch
```

---

## Module 5: Performance and Optimization

### Git's Efficiency Engine

#### How Git Stores Data

Unlike other VCS, Git doesn't store file differences—it stores snapshots:

```
Version 1: [File A] [File B] [File C]
Version 2: [File A] [File B'] [File C]  # Only B changed
Version 3: [File A'] [File B'] [File C]  # Only A changed
```

Git creates a snapshot of all files for each commit, but uses:
- **Object deduplication**: Identical files stored once
- **Delta compression**: Similar files compressed together
- **Pack files**: Efficient storage format

#### Understanding Git Objects

```bash
# View object database
find .git/objects -type f

# Examine object content
git cat-file -t <hash>  # Type
git cat-file -p <hash>  # Content

# Object types:
# blob - file content
# tree - directory structure
# commit - commit information
# tag - annotated tags
```

#### Push/Pull Efficiency

**First Push (Complete Transfer)**:
```bash
# Full repository uploaded
Enumerating objects: 100, done.
Counting objects: 100% (100/100), done.
Compressing objects: 100% (80/80), done.
Writing objects: 100% (100/100), 1.2 MiB | 2.1 MiB/s, done.
```

**Subsequent Pushes (Delta Transfer)**:
```bash
# Only changes uploaded
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 435 bytes | 435.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0)
```

#### Performance Monitoring

```bash
# Repository size
du -sh .git/

# Object count and size
git count-objects -v

# Verify repository integrity
git fsck

# Optimize repository
git gc --aggressive

# Prune unreachable objects
git prune
```

---

### Repository Management

#### Cleaning Up Repository

```bash
# Remove untracked files
git clean -n  # Dry run
git clean -f  # Force removal
git clean -fd # Remove directories too

# Remove remote tracking branches
git remote prune origin

# Compress repository
git gc

# Aggressive optimization (slower)
git gc --aggressive --prune=now
```

#### Managing Large Files

**Git LFS (Large File Storage)**:
```bash
# Install Git LFS
git lfs install

# Track large files
git lfs track "*.psd"
git lfs track "*.zip"
git lfs track "videos/*"

# Add .gitattributes
git add .gitattributes

# Normal Git workflow
git add large-file.psd
git commit -m "Add design files"
git push origin main
```

#### .gitignore Best Practices

```bash
# Common patterns
*.log
*.tmp
.env
node_modules/
.DS_Store
Thumbs.db
build/
dist/

# IDE files
.vscode/
.idea/
*.swp
*.swo

# Language-specific
__pycache__/
*.pyc
target/
*.class
```

---

## Module 6: Professional Workflows

### Industry Standard Workflows

#### Continuous Integration Workflow

```yaml
# .github/workflows/ci.yml
name: CI
on:
  push:
    branches: [ main, develop ]
  pull_request:
    branches: [ main ]

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v2
    - name: Setup Node.js
      uses: actions/setup-node@v2
      with:
        node-version: '16'
    - run: npm install
    - run: npm test
    - run: npm run lint
```

#### Release Workflow

```bash
# 1. Prepare release branch
git checkout -b release/v1.2.0

# 2. Update version numbers
# Edit package.json, version files, etc.

# 3. Create release commit
git commit -m "Bump version to 1.2.0"

# 4. Create tag
git tag -a v1.2.0 -m "Release version 1.2.0"

# 5. Push tag
git push origin v1.2.0

# 6. Merge to main
git checkout main
git merge release/v1.2.0
git push origin main
```

#### Hotfix Workflow

```bash
# 1. Create hotfix from main
git checkout main
git checkout -b hotfix/security-fix

# 2. Apply fix
# ... make changes ...
git commit -m "Fix security vulnerability CVE-2023-1234"

# 3. Create patch version
git tag -a v1.2.1 -m "Security hotfix 1.2.1"

# 4. Merge to main and develop
git checkout main
git merge hotfix/security-fix
git checkout develop
git merge hotfix/security-fix

# 5. Push everything
git push origin main develop v1.2.1
```

---

### Team Collaboration Patterns

#### Forking Workflow (Open Source)

```bash
# 1. Fork repository on GitHub
# 2. Clone your fork
git clone git@github.com:yourusername/project.git

# 3. Add upstream remote
git remote add upstream git@github.com:originalowner/project.git

# 4. Create feature branch
git checkout -b feature/awesome-feature

# 5. Work and commit
git commit -m "Add awesome feature"

# 6. Push to your fork
git push origin feature/awesome-feature

# 7. Create pull request from your fork to upstream

# 8. Keep fork synchronized
git fetch upstream
git checkout main
git merge upstream/main
git push origin main
```

#### Feature Branch Workflow (Teams)

```bash
# 1. Everyone works on shared repository
# 2. Each feature gets its own branch
# 3. Pull requests for code review
# 4. Merge to main after approval
# 5. Delete feature branches
```

#### Shared Repository Best Practices

```bash
# Branch protection rules
# - Require pull requests
# - Require status checks
# - Require up-to-date branches
# - Restrict who can push to main

# Code review requirements
# - At least 2 reviewers
# - No self-approval
# - Dismiss stale reviews
# - Require review from code owners
```

---

### Advanced Git Commands

#### Interactive Rebase

```bash
# Rewrite commit history
git rebase -i HEAD~3

# Interactive options:
# pick = use commit
# reword = change commit message
# edit = amend commit
# squash = combine with previous
# drop = remove commit
```

#### Advanced Searching

```bash
# Search commit messages
git log --grep="bug fix"

# Search code content
git log -S "function_name"

# Search by author
git log --author="John Doe"

# Search by date
git log --since="2023-01-01" --until="2023-12-31"

# Search in specific file
git log -p -- filename.js
```

#### Stashing Work

```bash
# Save current work
git stash
git stash save "Work in progress on feature X"

# List stashes
git stash list

# Apply stash
git stash apply
git stash apply stash@{2}

# Pop stash (apply and remove)
git stash pop

# Delete stash
git stash drop stash@{1}
```

#### Cherry-picking

```bash
# Apply specific commit to current branch
git cherry-pick <commit-hash>

# Cherry-pick multiple commits
git cherry-pick A..B

# Cherry-pick without committing
git cherry-pick --no-commit <commit-hash>
```

#### Bisecting (Finding Bugs)

```bash
# Start bisect session
git bisect start

# Mark current commit as bad
git bisect bad

# Mark known good commit
git bisect good v1.0.0

# Git will checkout middle commit
# Test and mark as good or bad
git bisect good  # or git bisect bad

# Continue until bug is found
# Reset when done
git bisect reset
```

---

## 🎓 Course Completion

### Mastery Checklist

#### Core Concepts ✅
- [ ] Understand distributed version control
- [ ] Distinguish between Git and GitHub
- [ ] Master the three-state model (working/staging/repository)
- [ ] Navigate Git history effectively

#### Authentication ✅
- [ ] Set up SSH keys with proper security
- [ ] Configure Personal Access Tokens
- [ ] Implement multi-device authentication strategy
- [ ] Apply security best practices

#### Collaboration ✅
- [ ] Create and manage branches effectively
- [ ] Resolve merge conflicts professionally
- [ ] Write excellent pull requests
- [ ] Conduct thorough code reviews

#### Performance ✅
- [ ] Understand Git's efficiency mechanisms
- [ ] Optimize repository performance
- [ ] Manage large files appropriately
- [ ] Monitor repository health

#### Professional Workflows ✅
- [ ] Implement industry-standard workflows
- [ ] Integrate with CI/CD systems
- [ ] Lead team collaboration
- [ ] Troubleshoot complex Git issues

### Your Git Journey Continues

**Congratulations!** You've completed a comprehensive journey through Git and GitHub mastery. You now possess:

- **Technical Expertise**: Deep understanding of Git's internal mechanisms
- **Professional Skills**: Industry-standard workflows and best practices
- **Security Knowledge**: Proper authentication and access management
- **Team Leadership**: Ability to guide teams in version control excellence

#### Next Steps

1. **Practice Daily**: Use Git for all your projects
2. **Teach Others**: Share knowledge with teammates
3. **Stay Updated**: Follow Git and GitHub feature releases
4. **Contribute**: Participate in open source projects
5. **Specialize**: Explore advanced topics like Git hooks, custom workflows

#### Resources for Continued Learning

- **Official Documentation**: [git-scm.com](https://git-scm.com/doc)
- **GitHub Guides**: [guides.github.com](https://guides.github.com)
- **Pro Git Book**: Free comprehensive reference
- **Git Tutorials**: Interactive learning platforms
- **Community**: Stack Overflow, GitHub Community

---

## 📞 Support & Community

### Getting Help

**When you encounter issues**:
1. Check Git status: `git status`
2. Review recent history: `git log --oneline -10`
3. Search documentation: `git help <command>`
4. Ask the community: Stack Overflow with `git` tag

### Contributing Back

**Share your knowledge**:
- Answer questions in forums
- Write blog posts about your Git experiences
- Contribute to open source projects
- Mentor other developers

### Course Updates

This course evolves with the industry. Check for updates covering:
- New Git features
- GitHub platform updates
- Emerging workflow patterns
- Security best practices

---

*"The journey of a thousand commits begins with a single `git init`. You now have the knowledge to build, collaborate, and lead in the world of modern software development."*

**Happy coding! 🚀**

---

## 📜 License

© 2025 Git & GitHub Mastery Course. All rights reserved.

This course content is proprietary and designed for educational excellence. Unauthorized distribution is prohibited.

**Course Value**: $5,000  
**Your Investment in Excellence**: Priceless

---

