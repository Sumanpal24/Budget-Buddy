# Budget Buddy — Expense Tracker

A Flask-based expense tracker web app.

## Project Structure

```
expense-tracker/
├── app.py                  # Flask app entrypoint and routes
├── database/
│   ├── __init__.py
│   └── db.py                # get_db(), init_db(), seed_db()
├── static/
│   ├── css/style.css
│   └── js/main.js
├── templates/
│   ├── base.html
│   ├── landing.html
│   ├── login.html
│   └── register.html
├── requirements.txt
└── venv/                    # local virtual environment (not committed)
```

## Setup

### 1. Create a virtual environment

```cmd
python -m venv venv
```

### 2. Activate the virtual environment

**cmd.exe:**
```cmd
venv\Scripts\activate.bat
```

**PowerShell:**
```powershell
.\venv\Scripts\Activate.ps1
```
If PowerShell blocks the script with an execution-policy error, run once in that same window:
```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
```

**Git Bash:**
```bash
source venv/Scripts/activate
```

Once activated, your prompt will show `(venv)` at the start.

### 3. Install dependencies

```cmd
pip install -r requirements.txt
```

Verify what's installed:
```cmd
pip list
```

### 4. Run the app

```cmd
python app.py
```

The app runs at `http://127.0.0.1:5001`.

## Git Setup (how this repo was initialized and pushed)

These are the exact steps used to turn this local folder into a Git repo and push it to GitHub.

```bash
# 1. Initialize a new git repository in this folder
git init

# 2. Stage all files
git add .

# 3. Commit the staged files
git commit -m "Initial commit"

# 4. Rename the default branch to main
git branch -M main

# 5. Link the local repo to the GitHub remote
git remote add origin https://github.com/Sumanpal24/Budget-Buddy.git

# 6. Push local main branch to GitHub and set upstream tracking
git push -u origin main
```

Notes:
- `.gitignore` excludes `venv/`, `expense_tracker.db`, `__pycache__/`, `.env`, and other local-only files, so they never get committed.
- If `git push` fails with a `403 Permission denied` error, it usually means Git has cached credentials for the wrong GitHub account. Fix it via Windows **Credential Manager** (search for the GitHub entry and remove/update it), then run `git push` again — it will prompt you to sign in with the correct account.
- After the initial push, future updates only need:
  ```bash
  git add .
  git commit -m "your message"
  git push
  ```
