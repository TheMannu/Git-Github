### **Setting Up a Git Pre-Commit Hook to Check for Sensitive Data**

#### **1. Create the Pre-Commit Hook File**

1. Navigate to your Git repository's hooks directory:

   ```bash
   cd .git/hooks
   ```

2. Create a file named `pre-commit` if it doesn't already exist:

   ```bash
   touch pre-commit
   ```

#### **2. Edit the `pre-commit` File**

Open the `pre-commit` file in a text editor and add the following script:


```bash
#!/bin/sh

# Define the pattern to search for sensitive information
pattern='password|secret_key|API_KEY'

# Get the list of staged files
files=$(git diff --cached --name-only --diff-filter=ACM)

# Check for sensitive information in the staged files
for file in $files; do
    if grep -qE "$pattern" "$file"; then
        echo "Sensitive data found in $file. Please remove before committing."
        exit 1
    fi
done
```
