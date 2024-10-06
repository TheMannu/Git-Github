### Practical Example

1. **Configure your user information:**

   ```bash
   git config --global user.name "Admin"
   git config --global user.email snsb.mahi@gmail.com
   ```

2. **Create a new repository and push changes:**

   ```bash
   echo "# cloudweb for my first application" >> README.md
   git init
   git status
   git add README.md
   git commit -m "first commit"
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
