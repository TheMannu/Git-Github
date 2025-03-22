### Practical Example

1. **Configure your user information:**

   ```bash
   git config --global user.name "Admin"
   git config --global user.email snsb.mahi@gmail.com
   ```

   **To check The ORIGIN connection**
   ```bash
   git remote -v
   ```

   **To change the DEFAULT Coonection name From ORIGIN to Something Else**
   ```bash
   git remote rename origin newName
   ```

2. **Create a new repository and push changes:**

   ```bash
   echo "cloudweb for my first application" >> README.md
   git init
   git status
   git add README.md # to move the changes in file to staging area
   git commit -m "first commit" # to move the from staging area to.git directory

   git branch -M main
   git remote add origin https://github.com/vikas4cloud/cloudweb.git
   git push -u origin main
   ```

3. **Next time:**

   ```bash
   git add *
   git commit -m "2nd commit"
   git push
   ```
4. **Git log & Git Show**

   ```bash
   git log # to show History Of Commits in details
   ```

   ```bash
   git log --oneline # to show History Of Commits in One Line
   ```

   ```bash
   git log --graph --oneline # to show History Of Commits on different brances in graphical manner
   ```

   ```bash
   git show <commit id> # to show details of specific Commits ID 
   ```

5. **Create branch, checkout and create PULL REQUEST**

6. **PULL and PUSH**

   - git pull <Connection Name> <Branch Name>

   ```bash
   git pull origin main
   ```

   - git pull <Connection Name> <Branch Name>

   ```bash
   git push origin main
   ```

7. **To add a remote connection**

```bash
git remote add <Connection Name> <Github URL>
```