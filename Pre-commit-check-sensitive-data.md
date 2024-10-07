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

#### **3. Make the Script Executable**

Make sure the `pre-commit` hook is executable:

```bash
chmod +x pre-commit
```

#### **4. Explanation of the Script**

- **`pattern='password|secret_key|API_KEY'`**: Defines the search pattern for sensitive information. You can add or remove patterns as needed.

- **`files=$(git diff --cached --name-only --diff-filter=ACM)`**: Lists all staged files that have been added (`A`), copied (`C`), or modified (`M`).

- **`grep -qE "$pattern" "$file"`**: Searches for the defined pattern in each staged file. The `-q` option suppresses output, and `-E` enables extended regex patterns.

- **`echo "Sensitive data found in $file. Please remove before committing."`**: Displays a message if sensitive data is found.

- **`exit 1`**: Exits with status code `1` to abort the commit if sensitive data is detected.
