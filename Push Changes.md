### Fixing Issues When Pushing Changes

1. **Fetch the latest changes from the remote:**

   ```bash
   git fetch origin
   ```

2. **Rebase or merge the changes:**

- To **rebase** (apply your changes on top of the remote branch):

  ```bash
  git pull --rebase origin main
  ```

- Alternatively, to **merge** the remote changes into your branch:

  ```bash
  git pull origin main
  ```

  You will need to resolve any merge conflicts manually if they arise.

3. **Push your changes after resolving conflicts (if any):**

  ```bash
  git push origin main
  ```

4. **Set default pull behavior:**

- For rebase:
  ```bash
  git config pull.rebase true
  ```

- For merge:
  ```bash
  git config pull.rebase false
  ```