# Pushing to GitHub in VS Code

## Step 1: Open the Terminal

In VS Code, open the integrated terminal:
- **Mac:** `Ctrl + `` ` (backtick)
- **Windows:** `Ctrl + `` ` (backtick)
- Or go to **Terminal → New Terminal** from the menu bar

---

## Step 2: Make Sure You're in the Right Folder

Your terminal should already be in your project folder. Double-check with:

```bash
pwd
```

You should see the path to your project. If not, navigate there with `cd`.

---

## Step 3: Check What's Changed

See which files have been modified:

```bash
git status
```

Files in red = not yet staged. Files in green = ready to commit.

---

## Step 4: Stage Your Changes

Add the files you want to include in your commit:

```bash
# Add a specific file
git add filename.py

# Or add everything at once
git add .
```

---

## Step 5: Commit Your Changes

Write a short message describing what you did:

```bash
git commit -m "your message here"
```

> 💡 **Good commit messages** are short and descriptive — e.g., `"add bubble sort function"` or `"fix loop bug in search"`.

---

## Step 6: Push to GitHub

Send your commit up to GitHub:

```bash
git push
```

That's it! You can visit your GitHub repository in a browser to confirm your changes are there.

---

## Troubleshooting

| Problem | Fix |
|---|---|
| `git: command not found` | Git may not be installed — ask Mr. Berg |
| `fatal: not a git repository` | You're not in the right folder — check `pwd` and `cd` to your project |
| `rejected` on push | Run `git pull` first to sync, then try pushing again |
| Asked for username/password | Make sure you're logged into GitHub in VS Code |

---

## Quick Reference Cheat Sheet

```bash
git status          # see what's changed
git add .           # stage everything
git commit -m "msg" # commit with a message
git push            # push to GitHub
```
