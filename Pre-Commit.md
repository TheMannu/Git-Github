### **Instructions for Setting Up and Using `flake8`**

Installing and running `flake8` for linting Python files staged for commit, including setting it up as a Git pre-commit hook

#### **1. Install `flake8`**

First, ensure you have Python and pip installed on your system:

```bash
sudo apt update
sudo apt install python3 python3-pip
```

Then, install `flake8` using pip. You can choose to install it globally or within a virtual environment:

- **Global Installation:**

   ```bash
   pip3 install flake8
   ```

- **Virtual Environment (Recommended):**

   ```bash
   python3 -m venv venv
   source venv/bin/activate
   pip install flake8
   ```

Verify the installation:

```bash
flake8 --version
```


#### **2. Check Staged Python Files with `flake8`**

Use the following command to lint only the staged Python files (`*.py` files) before committing:

```bash
files=$(git diff --cached --name-only --diff-filter=ACM | grep '\.py$')
flake8 $files
```

#### **3. Automate Linting with a Git Pre-Commit Hook**

To automatically run `flake8` on staged files before each commit, set up a Git pre-commit hook:

1. **Create the Pre-Commit Hook File:**

   ```bash
   touch .git/hooks/pre-commit
   ```

2. **Edit the `pre-commit` File:**

   Add the following script to the file:

   ```bash
   #!/bin/sh

   files=$(git diff --cached --name-only --diff-filter=ACM | grep '\.py$')

   if [ -n "$files" ]; then
       echo "Running flake8 on staged Python files..."
       flake8 $files

       if [ $? -ne 0 ]; then
           echo "flake8 failed. Commit aborted."
           exit 1
       fi
   fi
   ```
