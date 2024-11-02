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
