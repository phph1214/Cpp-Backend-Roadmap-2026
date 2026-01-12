# Git Command Cheatsheet for C++ Devs


# 1. Daily Workflow
```bash
# Check status (Always do this first!)
git status

# Add changes to staging area
git add .           # Add all files
git add main.cpp    # Add specific file (Recommended)

# Commit changes (Create a snapshot)
# Format: [type]: description
# Types: feat(new feature), fix(bug fix), docs(documentation), refactor(cleanup)
git commit -m "feat: implement basic server loop"

# Upload to GitHub
git push origin main
```

# 2. Undo & Reset
```bash
# 1. Undo local changes (Before 'git add')
git restore main.cpp      # Discard changes in working directory

# 2. Unstage files (After 'git add', before 'git commit')
git restore --staged main.cpp

# 3. Reset to previous version (After 'git commit')
# --soft: Keep your code changes in working directory (Safe)
git reset --soft HEAD~1
# --hard: DESTROY changes and revert to previous commit (Dangerous!)
git reset --hard HEAD~1
```


# 3. Configuration
```bash
# Check remote URL
git remote -v

# Change remote URL (e.g., from HTTPS to SSH)
git remote set-url origin git@github.com:User/Repo.git
```

# 4. Branching
```bash
git checkout -b dev   # Create and switch to 'dev' branch
git checkout main     # Switch back to 'main'
git merge dev         # Merge 'dev' into current branch
```