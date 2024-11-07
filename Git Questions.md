### **Basic Git Questions**
---
1. **What is Git?**
   - Git is a distributed version control system (DVCS) used to track changes in source code during software development. It allows multiple developers to work on a project concurrently.

2. **What are the differences between Git and GitHub?**
   - Git is a tool for managing code versions locally, while GitHub is a web-based hosting service for Git repositories, enabling collaboration, remote hosting, and additional features like issue tracking.

3. **How do you install Git on your system?**
   - Use the following package managers based on your OS:
     - **Ubuntu/Debian:** `sudo apt install git`
     - **CentOS/Fedora:** `sudo yum install git`
     - **macOS:** `brew install git`
     - Alternatively, download it from [git-scm.com](https://git-scm.com).

4. **How do you initialize a new Git repository?**
   - Run `git init` in your project directory to create a new empty Git repository.

5. **What is a Git repository?**
   - A Git repository is a directory that stores the project's history and tracks all changes made to files.

6. **How do you clone a repository?**
   - Run `git clone <repository-url>` to copy a repository from a remote server to your local machine.

7. **What is a branch in Git?**
   - A branch is a movable pointer to a specific commit, allowing independent development paths within the repository.

8. **How do you create a new branch?**
   - Use `git branch <branch-name>` to create a branch, or `git checkout -b <branch-name>` to create and switch to the branch.

9. **How do you switch between branches?**
   - Use `git checkout <branch-name>` to switch to the desired branch.

10. **What is the difference between `git merge` and `git rebase`?**
    - `git merge` combines branches by creating a new commit, while `git rebase` moves or integrates commits from one branch onto another without creating additional commits.

11. **How do you delete a branch?**
    - Use `git branch -d <branch-name>` to delete a branch locally, or `git branch -D <branch-name>` to forcefully delete it.

12. **What is a commit in Git?**
    - A commit is a snapshot of changes made in the repository at a specific point in time.

13. **How do you make a commit?**
    - Stage changes and use `git commit -m "commit message"` to save them in the repository.

14. **What is a staging area or index in Git?**
    - The staging area is a buffer zone where changes are prepared before committing them to the repository.

15. **How do you stage files for a commit?**
    - Use `git add <file-or-directory>` to move changes from the working directory to the staging area.

16. **What is the purpose of `git add`?**
    - It adds changes to the staging area, preparing them for the next commit.

17. **How do you view the commit history?**
    - Use `git log` to view the list of past commits, with details like author, commit message, and timestamp.

18. **What is the difference between `git pull` and `git fetch`?**
    - `git pull` fetches changes and merges them, while `git fetch` only downloads the changes without merging.

19. **How do you undo a commit?**
    - Use `git revert <commit>` to create a new commit that undoes the previous one, or `git reset <commit>` to roll back to a specific commit.

20. **What is a merge conflict and how do you resolve it?**
    - A merge conflict occurs when changes in different branches overlap. To resolve, manually edit the conflicting files, stage them, and commit the changes.

---
### **Intermediate Git Questions**
---
21. **What is `git stash` and how is it used?**
    - `git stash` temporarily saves changes that are not ready to be committed. Use `git stash` to store them and `git stash apply` or `git stash pop` to retrieve them.

22. **How do you apply a stashed change?**
    - Use `git stash apply` to reapply the stash without deleting it, or `git stash pop` to apply and remove the stash.

23. **What is `git cherry-pick` and when would you use it?**
    - `git cherry-pick` applies a specific commit from another branch to your current branch. It is used when you want to include individual changes from other branches.

24. **How do you configure a Git repository to ignore certain files?**
    - Create a `.gitignore` file and specify file patterns or directories to exclude from version control.

25. **What is `git tag` and how do you create a tag?**
    - A Git tag marks a specific point in the commit history. Create a tag using `git tag <tag-name>`.

26. **How do you view all tags in a repository?**
    - Use `git tag` to list all tags in the repository.

27. **What is `git blame` and how is it useful?**
    - `git blame` shows which author made changes to each line of a file, useful for tracking down the origin of code or changes.

28. **What is the purpose of `.gitignore`?**
    - It is used to define files or directories that Git should not track or include in version control.

29. **How do you remove a file from the staging area?**
    - Use `git reset <file>` to unstage a file, keeping it in the working directory.

30. **What is `git bisect` and how is it used?**
    - `git bisect` performs a binary search through commit history to find the commit that introduced a bug. Run `git bisect start` to begin.

31. **How do you rebase a branch?**
    - Use `git rebase <base-branch>` to apply your current branch's changes onto another branch.

32. **What is the difference between `git reset` and `git revert`?**
    - `git reset` moves the branch pointer and modifies the working directory, while `git revert` creates a new commit that undoes previous changes.

33. **How do you amend the most recent commit?**
    - Use `git commit --amend` to modify the previous commit, either by changing the commit message or adding new changes.

34. **How do you set up a remote repository?**
    - Use `git remote add <name> <url>` to add a remote repository for collaboration.

35. **What is `git remote` and how do you use it?**
    - `git remote` manages the set of remote repositories associated with your project. Use `git remote add`, `git remote remove`, etc., to manage them.

36. **How do you remove a remote repository?**
    - Use `git remote remove <name>` to delete a remote repository configuration.

37. **What is `git log` and how can you customize its output?**
    - `git log` shows the commit history, and you can customize the output using options like `--oneline`, `--graph`, and `--decorate` for a cleaner, visual history.
