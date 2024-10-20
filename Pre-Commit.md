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