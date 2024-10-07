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