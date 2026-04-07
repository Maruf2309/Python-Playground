# Git Command
```bash

# ============================================
# 🚀 BASIC WORKFLOW (Daily Commands)- Pinned🚀
# ============================================

git add .
git commit -m "inital commmit"
git push origin main

# ============================================
# 🚀 GIT CHEATSHEET: FROM CLONE TO PUSH
# ============================================

# ┌─────────────────────────────────────────┐
# │ 1️⃣  INITIAL SETUP (First Time Only)    │
# └─────────────────────────────────────────┘

# Configure your identity (required before first commit)
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

# Check your configuration
git config --list

# Set default branch name to 'main'
git config --global init.defaultBranch main

# (Optional) Set up SSH key for GitHub
ssh-keygen -t ed25519 -C "your.email@example.com"
cat ~/.ssh/id_ed25519.pub  # Copy this to GitHub SSH settings


# ┌─────────────────────────────────────────┐
# │ 2️⃣  CLONE EXISTING REPOSITORY          │
# └─────────────────────────────────────────┘

# Clone via HTTPS
git clone https://github.com/yourusername/python-data-playground.git

# Clone via SSH (recommended)
git clone git@github.com:yourusername/python-data-playground.git

# Clone specific branch
git clone -b develop https://github.com/yourusername/python-data-playground.git

# Clone into specific directory
git clone https://github.com/yourusername/python-data-playground.git my-folder


# ┌─────────────────────────────────────────┐
# │ 3️⃣  CREATE NEW REPOSITORY              │
# └─────────────────────────────────────────┘

# Initialize new repository
cd D:/LD/Cloud/Python-Playground
git init

# Add remote origin (after creating repo on GitHub)
git remote add origin https://github.com/yourusername/python-data-playground.git

# Verify remote
git remote -v

# Rename default branch to main (if needed)
git branch -M main


# ┌─────────────────────────────────────────┐
# │ 4️⃣  BASIC WORKFLOW (Daily Commands)    │
# └─────────────────────────────────────────┘

# Check status of your files
git status

# See what changed (differences)
git diff                    # Unstaged changes
git diff --staged          # Staged changes

# Add files to staging area
git add filename.py         # Single file
git add folder/             # Entire folder
git add .                   # All files in current directory
git add *.py                # All Python files

# Remove files from staging
git reset filename.py       # Unstage specific file
git reset                   # Unstage everything

# Commit changes
git commit -m "Add data cleaning module"

# Commit with detailed message (multi-line)
git commit -m "Add feature: DataCleaner class

- Implement missing value handling
- Add outlier detection methods
- Include logging functionality"

# Commit all tracked files (skip git add)
git commit -am "Update documentation"

# Amend last commit (fix message or add forgotten files)
git commit --amend -m "Corrected commit message"
git commit --amend --no-edit  # Keep same message


# ┌─────────────────────────────────────────┐
# │ 5️⃣  WORKING WITH BRANCHES              │
# └─────────────────────────────────────────┘

# List branches
git branch                  # Local branches
git branch -r               # Remote branches
git branch -a               # All branches (local + remote)

# Create new branch
git branch feature-automation

# Switch to branch
git checkout feature-automation

# Create and switch (shortcut)
git checkout -b feature-visualization

# Switch to main branch
git checkout main

# Delete branch
git branch -d feature-old           # Safe delete (merged)
git branch -D feature-old           # Force delete

# Rename current branch
git branch -m new-branch-name


# ┌─────────────────────────────────────────┐
# │ 6️⃣  SYNC WITH REMOTE (Push/Pull)      │
# └─────────────────────────────────────────┘

# Pull latest changes (fetch + merge)
git pull origin main

# Pull with rebase (cleaner history)
git pull --rebase origin main

# Fetch changes without merging
git fetch origin

# Push to remote
git push origin main                # Push main branch
git push origin feature-branch      # Push feature branch

# Push and set upstream (first time)
git push -u origin feature-branch

# Force push (⚠️ use carefully - overwrites remote)
git push --force origin main

# Push all branches
git push --all origin

# Delete remote branch
git push origin --delete feature-old


# ┌─────────────────────────────────────────┐
# │ 7️⃣  VIEW HISTORY & LOGS               │
# └─────────────────────────────────────────┘

# View commit history
git log
git log --oneline               # Compact view
git log --graph --oneline       # Visual branch structure
git log --author="Your Name"    # Filter by author

# View last N commits
git log -5

# View changes in each commit
git log -p

# View who changed what (blame)
git blame filename.py

# View history of a specific file
git log --follow filename.py


# ┌─────────────────────────────────────────┐
# │ 8️⃣  UNDO CHANGES & RECOVERY           │
# └─────────────────────────────────────────┘

# Discard uncommitted changes (⚠️ irreversible)
git checkout -- filename.py     # Revert file to last commit
git restore filename.py          # Alternative (newer)

# Discard all uncommitted changes
git reset --hard HEAD

# Unstage files but keep changes
git reset HEAD filename.py

# Revert a commit (creates new commit)
git revert commit-hash

# Reset to previous commit (⚠️ rewrites history)
git reset --soft HEAD~1         # Keep changes in staging
git reset --mixed HEAD~1        # Keep changes but unstaged
git reset --hard HEAD~1         # Delete changes completely

# Get back deleted commit (find lost commits)
git reflog
git checkout commit-hash


# ┌─────────────────────────────────────────┐
# │ 9️⃣  STASHING (Temporary Save)         │
# └─────────────────────────────────────────┘

# Save current work without committing
git stash
git stash save "WIP: data cleaning"

# List stashes
git stash list

# Apply latest stash
git stash apply
git stash pop                   # Apply and remove from stash

# Apply specific stash
git stash apply stash@{1}

# Create branch from stash
git stash branch new-branch

# Clear all stashes
git stash clear


# ┌─────────────────────────────────────────┐
# │ 🔟  MERGING & REBASING                │
# └─────────────────────────────────────────┘

# Merge branch into current
git checkout main
git merge feature-branch

# Abort merge if conflicts
git merge --abort

# Rebase branch onto main
git checkout feature-branch
git rebase main

# Continue rebase after resolving conflicts
git add resolved-file.py
git rebase --continue

# Skip problematic commit during rebase
git rebase --skip


# ┌─────────────────────────────────────────┐
# │ 1️⃣1️⃣  .GITIGNORE (Exclude Files)     │
# └─────────────────────────────────────────┘

# Create .gitignore file
echo "# Python" > .gitignore
echo "__pycache__/" >> .gitignore
echo "*.pyc" >> .gitignore
echo ".env" >> .gitignore
echo "venv/" >> .gitignore
echo "data/raw/*.csv" >> .gitignore

# View ignored files
git status --ignored

# Force add ignored file
git add -f data/sample.csv


# ┌─────────────────────────────────────────┐
# │ 1️⃣2️⃣  TAG & RELEASE                   │
# └─────────────────────────────────────────┘

# Create lightweight tag
git tag v1.0.0

# Create annotated tag (recommended)
git tag -a v1.0.0 -m "Release version 1.0.0"

# List tags
git tag

# Push tags to remote
git push origin v1.0.0
git push --tags                   # Push all tags

# Delete tag
git tag -d v1.0.0                 # Local
git push origin --delete v1.0.0   # Remote


# ┌─────────────────────────────────────────┐
# │ 1️⃣3️⃣  COMPLETE WORKFLOW EXAMPLE      │
# └─────────────────────────────────────────┘

# START NEW FEATURE
git checkout main
git pull origin main
git checkout -b feature-data-cleaning

# MAKE CHANGES
# (edit files...)

# COMMIT CHANGES
git add data_handling/cleaner.py
git commit -m "Add outlier detection method"

# PUSH FEATURE
git push -u origin feature-data-cleaning

# CREATE PULL REQUEST on GitHub

# AFTER MERGE, UPDATE LOCAL
git checkout main
git pull origin main

# DELETE FEATURE BRANCH
git branch -d feature-data-cleaning


# ┌─────────────────────────────────────────┐
# │ 1️⃣4️⃣  QUICK REFERENCE (Most Used)     │
# └─────────────────────────────────────────┘

git status                    # What's changed?
git add .                     # Stage all changes
git commit -m "message"       # Commit staged changes
git push origin main          # Push to remote
git pull origin main          # Pull from remote
git checkout -b new-branch    # Create and switch branch
git log --oneline             # View commit history
git diff                      # See unstaged changes


# ┌─────────────────────────────────────────┐
# │ 1️⃣5️⃣  FIX COMMON ISSUES               │
# └─────────────────────────────────────────┘

# ❌ "failed to push some refs"
git pull origin main --rebase
git push origin main

# ❌ "Please tell me who you are"
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

# ❌ "Your branch is ahead of 'origin/main'"
git push origin main

# ❌ "Merge conflict in file.py"
# Edit file.py to resolve conflicts, then:
git add file.py
git commit -m "Resolve merge conflict"

# ❌ "Detached HEAD state"
git switch main
git branch -d temporary-branch

# ❌ Forgot to add file to last commit
git add forgotten-file.py
git commit --amend --no-edit


# ┌─────────────────────────────────────────┐
# │ 1️⃣6️⃣  ALIASES (Shortcuts)             │
# └─────────────────────────────────────────┘

# Create useful aliases
git config --global alias.st status
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.ci commit
git config --global alias.lg "log --oneline --graph --all"
git config --global alias.unstage "reset HEAD --"
git config --global alias.last "log -1 HEAD"
git config --global alias.tree "log --graph --pretty=oneline --abbrev-commit"

# Use aliases
git st          # instead of git status
git co main     # instead of git checkout main
git lg          # pretty log graph


# ┌─────────────────────────────────────────┐
# │ 1️⃣7️⃣  QUICK SETUP FOR NEW PROJECT     │
# └─────────────────────────────────────────┘

# Complete setup for your Python-Playground
cd D:/LD/Cloud/Python-Playground

# Initialize git
git init

# Create .gitignore for Python
cat > .gitignore << EOF
# Python
__pycache__/
*.py[cod]
*.so
.Python
env/
venv/
ENV/
.venv
*.egg-info/
dist/
build/

# Jupyter
.ipynb_checkpoints/
*.ipynb

# Data files (optional)
*.csv
*.xlsx
data/raw/

# Environment
.env
.env.local

# IDE
.vscode/
.idea/
*.swp

# OS
.DS_Store
Thumbs.db
EOF

# Initial commit
git add .
git commit -m "Initial commit: Python data playground setup"

# Add remote (replace with your repo URL)
git remote add origin https://github.com/yourusername/python-data-playground.git

# Push to GitHub
git branch -M main
git push -u origin main

# 🎉 Done!


# ┌─────────────────────────────────────────┐
# │ 1️⃣8️⃣  DAILY WORKFLOW CHEATSHEET       │
# └─────────────────────────────────────────┘

# START DAY
git checkout main
git pull origin main
git checkout -b feature/today-task

# DURING WORK
git add .
git commit -m "Progress: implemented function X"

# END DAY
git push -u origin feature/today-task

# CREATE PULL REQUEST on GitHub

# NEXT DAY (after PR approved)
git checkout main
git pull origin main
git branch -d feature/today-task


# ┌─────────────────────────────────────────┐
# │ 1️⃣9️⃣  EMERGENCY RECOVERY              │
# └─────────────────────────────────────────┘

# Oops! Deleted something important
git reflog                           # Find lost commit
git checkout <lost-commit-hash>      # Recover it

# Oops! Committed to wrong branch
git reset HEAD~1                     # Undo commit
git stash                            # Save changes
git checkout correct-branch
git stash pop                        # Apply changes
git add . && git commit -m "message"

# Oops! Pushed wrong code
git revert <commit-hash>             # Safe revert
git push origin main                 # Push revert

# Oops! Need last working version
git checkout main
git reset --hard HEAD~1              # ⚠️ Only if alone!


# ┌─────────────────────────────────────────┐
# │ 2️⃣0️⃣  CHEAT CODES (Productivity)     │
# └─────────────────────────────────────────┘

git add . && git commit -m "WIP" && git push   # One-liner commit & push
git pull --rebase && git push                  # Sync & push
git checkout - && git branch                   # Go to previous branch

# Visualize repository
git log --graph --pretty=oneline --abbrev-commit --all

# See who contributed
git shortlog -sn

# Find when a function was added
git log -S "def clean_data" --source --all

# Undo last pull
git reset --hard HEAD@{1}