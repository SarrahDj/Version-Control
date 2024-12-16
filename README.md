# Git Cheat Sheet

Type: TP

## Basic Configuration

```bash
# Set up global user information
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

# Check current configuration
git config --list

```

## Repository Creation & Initialization

```bash
# Create a new repository
git init

# Clone an existing repository
git clone <https://github.com/username/repository.git>

# Clone a specific branch
git clone -b branch-name <https://github.com/username/repository.git>

```

## Branching

```bash
# List branches
git branch

# Create a new branch
git branch new-branch-name

# Switch to a branch
git checkout branch-name

# Create and switch to a new branch
git checkout -b new-branch-name

# Delete a branch
git branch -d branch-name

# Delete a branch forcefully
git branch -D branch-name

# Rename a branch
git branch -m old-branch-name new-branch-name

```

## Adding & Committing

```bash
# Add specific file
git add filename

# Add all changed files
git add .

# Commit with message
git commit -m "Commit message"

# Commit all changed tracked files
git commit -am "Commit message"

# Amend the last commit (modify most recent commit)
git commit --amend

```

## Checking Status & History

```bash
# Check status of working directory
git status

# Show differences
git diff

# Show commit history
git log

# Show compact log with one line per commit
git log --oneline

# Show last n commits
git log -n 3

```

## Undoing Changes

```bash
# Unstage a file
git reset HEAD filename

# Discard changes in working directory
git checkout -- filename

# Revert a commit (creates a new commit that undoes changes)
git revert commit-hash

# Reset to a previous commit (use with caution)
git reset --hard commit-hash

```

## Remote Repositories

```bash
# Add a remote repository
git remote add origin <https://github.com/username/repository.git>

# List remote repositories
git remote -v

# Push to remote repository
git push origin branch-name

# Pull from remote repository
git pull origin branch-name

# Fetch changes without merging
git fetch origin

```

## Merging & Rebasing

```bash
# Merge a branch into current branch
git merge branch-name

# Rebase current branch onto another branch
git rebase branch-name

# Interactive rebase (edit, squash, reorder commits)
git rebase -i HEAD~n  # n = number of commits

```

## Stashing

```bash
# Stash current changes
git stash

# List stashes
git stash list

# Apply most recent stash
git stash apply

# Apply specific stash
git stash apply stash@{n}

# Pop (apply and remove) most recent stash
git stash pop

```

## Advanced Operations

```bash
# Create a tag
git tag v1.0

# Create an annotated tag
git tag -a v1.0 -m "Version 1.0"

# Push tags to remote
git push --tags

# Create a patch
git format-patch HEAD~n

# Apply a patch
git apply patch-file

```

## Workflows & Best Practices

1. Always pull before you push to avoid conflicts
2. Use feature branches for development
3. Write clear, descriptive commit messages
4. Use `.gitignore` to exclude unnecessary files
5. Regularly backup your repositories

## Troubleshooting

```bash
# If you're stuck, use help
git help <command>

# Verbose output for debugging
git <command> -v

```

**Pro Tips:**

- Use `git gui` for a graphical interface
- Learn keyboard shortcuts in `gitk`
- Consider using Git GUI tools like SourceTree or GitHub Desktop
- Always review changes before committing
