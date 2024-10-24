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
