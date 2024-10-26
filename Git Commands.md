# Git Commands  
**Version control is a system that records changes to a file or set of files over time so that you can recall specific versions later.**

### Quick Start

```bash
git pull --rebase
git add .
git commit -m "commit message"
git push
```

## Let's Get Started

- `git init`: Initializes a new Git repository locally.

- `git help <command>`: Provides help for a specific Git command.

### Checking Changes

- `git status`: Lists modified files and staged changes.

- `git diff`: Shows file differences not yet staged. Use `git diff --staged` for staged changes.

#### Example:
```bash
git status
git diff --staged
```

### Adding & Removing Files

- `git add <filename>`: Stages the `<filename>` for commit.

- `git add .`: Stages all changes in the directory for commit.

- `git rm --cached <filename>`: Removes `<filename>` from the staging area without deleting it from the working directory.

- `git rm <filename>`: Removes `<filename>` from both the working directory and the staging area.

- `git restore <filename>`: Restores the file to the last committed version, discarding any local changes.

#### Example:
```bash
git add .
git rm --cached unwanted-file.txt
git rm old-file.txt
```

### Committing Changes

- `git commit -m "message"`: Commits staged changes with a message.

- `git commit --amend`: Modify the last commit. *(Avoid if already pushed)*

#### Example:
```bash
git commit -m "Initial commit"
```

### Viewing History

- `git log`: Displays the full commit history.

- `git log --oneline`: Shows commit history in one-line summaries.

- `git log -G "search-string"`: Searches for a specific string in the commit history.

- To exit the `git log`, press `q`.

#### Example:
```bash
git log
git log --oneline
git log -G "fix bug"
```

### Branching

- `git branch`: Lists all branches.

- `git branch <branch-name>`: Creates a new branch without switching to it.

- `git branch master`: Creates a new `master` branch.

- `git switch <branch-name>`: Switches to the specified branch (recommended instead of `git checkout`).

- `git checkout <branch-name>`: Switches to the specified branch.

- `git checkout -b <branch-name>`: Creates a new branch and switches to it.

- `git branch -d <branch-name>`: Deletes the specified branch.

#### Example:
```bash
git branch master
git checkout -b feature/new-feature
git switch master
```

### Working with Remote Repositories

- `git remote -v`: Displays remote repository URLs.

- `git remote add <remote-name> <url>`: Adds a new remote repository.

- `git remote remove <remote>`: Removes the specified remote repository.

- `git remote set-url origin <new-url>`: Changes the remote URL for `origin`.

- `git fetch <remote>`: Fetches changes from a remote without merging.

- `git pull <remote> <branch>`: Fetches and merges changes from the remote branch.

- `git push <remote> <branch>`: Pushes local changes to the remote branch.

#### Example:
```bash
git remote add origin https://github.com/username/repo.git
git remote set-url origin http://token@github.com/username/repo.git
git push origin master
```

### Merging & Rebasing

- `git merge <branch-name>`: Merges `<branch-name>` into the current branch.

- `git rebase <branch-name>`: Re-applies commits from the current branch on top of `<branch-name>`.

- `git pull origin master --rebase`: Fetches and rebases changes from the `master` branch.

#### Example:
```bash
git merge feature/new-feature
git pull origin master --rebase
```

### Handling Conflicts

- `git mergetool`: Opens a merge tool to resolve conflicts.

- `git add <file>`: Marks a conflict as resolved after manual editing.

- `git rebase --continue`: Continues a rebase after resolving conflicts.

- `git rebase --abort`: Cancels an ongoing rebase.


#### Example:
```bash
git rebase --continue
```

### Undoing Changes

- `git restore <filename>`: Restores the file to the last committed version.

- `git reset --hard HEAD`: Discards all local changes.

- `git checkout HEAD <file-name>`: Reverts changes in a specific file to the last commit.

- `git reset <commit>`: Resets to a previous commit, preserving changes as unstaged.

#### Example:
```bash
git reset --hard HEAD
```

### Tags

- `git tag <tag-name>`: Tags the current commit.

- `git push --tags`: Pushes all tags to the remote.

#### Example:
```bash
git tag v1.0.0
```
