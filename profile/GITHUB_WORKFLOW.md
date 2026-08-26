# GitHub Workflow Guide
**Introduction to AI | Lane Tech College Prep | [School Year]**

---

## 1. How Our Code is Organized

All class code lives inside a GitHub organization called `LT-IntroToAI-SY2627`. Inside it are two repositories — one for individual assignments and one for the shared class project.

```
LT-IntroToAI-SY2627/                        ← GitHub Organization
│
├── assignments/                          ← Repo 1: mini assignments
│   ├── gh1/                              ← instructor creates with starter files
│   │   ├── gh1-alexj/                     ← your branch + your personal file
│   │   └── gh1-mariac/
│   ├── gh2/
│   └── gh3/ ...
│
└── [class-project-repo]/                     ← Repo 2: shared class project
    ├── main                              ← protected, instructor merges only
    └── dev                              ← integration branch, students PR here
        ├── unit3-club-class-alexj/        ← your feature branch
        └── unit5-gemini-handler-mariac/
```

> **Key Rule:**
> - Mini assignments → `assignments` repo, branch off the assignment branch (`gh1`, `gh2`, etc.)
> - Class project → `[class-project-repo]` repo, branch off `dev`

---

## 2. Key Concepts

| Term | What It Means |
|---|---|
| `repository` | A folder on GitHub that stores your project and its full history |
| `branch` | Your own copy of the code where you can make changes safely |
| `commit` | A saved snapshot of your changes with a short description |
| `push` | Send your local commits up to GitHub |
| `pull` | Download the latest changes from GitHub |
| `pull request` | A request to merge your branch into another — how you submit work |
| `merge` | Combining one branch into another — your instructor does this after reviewing |
| `main` | The protected main branch — only the instructor merges here |
| `dev` | The integration branch for the class project — you PR your features here |
| `origin` | The name Git uses to refer to the remote copy of the repo on GitHub |

---

## 3. Daily VM Workflow

You will do all your coding inside a virtual machine (VM). Here is what to do every time you sit down in class:

1. Log in to your VM with your school credentials
2. Open a terminal
3. Navigate to your repo folder:
```bash
cd LT-IntroToAI-SY2627/assignments
# or for the class project:
cd LT-IntroToAI-SY2627/[class-project-repo]
```
4. Check your branch and pull the latest:
```bash
git status
git pull origin <branch-name>
```
5. Open VS Code and do your work
6. Commit and push when done — see sections 4 and 5 below

> **Always pull before you start.** Pulling first makes sure you have the latest version of the code. Skipping this step is the most common cause of merge conflicts.

---

## 4. Mini Assignment Workflow

Each assignment has its own branch that your instructor creates with starter files. You branch off it, create your personal file, and submit a pull request when done.

### Naming Conventions

| Thing | Convention |
|---|---|
| Your branch | `gh#-firstnamelastinitial` — example: `gh1-alexj` |
| Your file | `greetings_alexj.py` — match your first name and last initial consistently all year |
| Commit message | Short, present tense: `Add greet_user function` not `I did the thing` |

### Step-by-Step

**Step 1 — Switch to the assignment branch and pull the latest:**
```bash
git checkout gh1
git pull origin gh1
```

**Step 2 — Create your personal branch:**
```bash
git checkout -b gh1-alexj
```

**Step 3 — Create your personal file — never edit a classmate's file:**
```bash
touch greetings/greetings_alexj.py
```

**Step 4 — Write your code in VS Code. Save often.**

**Step 5 — Stage, commit, and push:**
```bash
git add .
git commit -m "Add greet_user function"
git push origin gh1-alexj
```

**Step 6 — Open a Pull Request on GitHub:**
- Go to the `assignments` repo on github.com
- Click **Compare & pull request**
- Set the base branch to `gh1` — **not main**
- Add a short description and submit

---

## 5. Class Project Workflow

The class project uses a two-branch protection system. You never push directly to `main` or `dev` — always work on a feature branch and PR into `dev`.

### Naming Conventions

| Thing | Convention |
|---|---|
| Your branch | `unit#-feature-firstnamelastinitial` — example: `unit3-club-class-alexj` |
| PR target | Always `dev` — never `main` |
| Commit message | Describe the feature: `Add Club class with get_info method` |

### Step-by-Step

**Step 1 — Switch to dev and pull the latest:**
```bash
git checkout dev
git pull origin dev
```

**Step 2 — Create your feature branch:**
```bash
git checkout -b unit3-club-class-alexj
```

**Step 3 — Do your work. Commit often with clear messages.**

**Step 4 — Push your feature branch:**
```bash
git push origin unit3-club-class-alexj
```

**Step 5 — Open a Pull Request on GitHub:**
- Go to the `[class-project-repo]` repo
- Click **Compare & pull request**
- Set the base branch to `dev` — **not main**
- Request a peer review from a classmate
- Submit and wait for instructor merge

> **Merge Conflicts:** Later in the year, multiple students may edit the same file. Git will flag this as a merge conflict. Do not panic — your instructor will walk you through resolving it. It is a normal part of collaborative development.

---

## 6. Common Problems & Fixes

| Problem | Why It Happens | Fix |
|---|---|---|
| On the wrong branch | Forgot to checkout before starting | `git stash` → `git checkout <correct-branch>` → `git stash pop` |
| Forgot to pull first | Local copy is behind GitHub | `git pull origin <branch-name>` before making changes |
| Pushed to wrong branch | PR is targeting the wrong base | Close the PR, open a new one with the correct base branch |
| Nothing to commit | No files were staged | Run `git add .` before `git commit` |
| Rejected push | Local branch is behind the remote | `git pull origin <branch-name>` first, then push again |
| Merge conflict | Two people edited the same lines | Open the file, look for `<<<<<<` markers, resolve manually, then add and commit |
| Can't find repo folder | Wrong directory in terminal | Run `ls` to see what's here, then `cd` to navigate |
| PR won't merge | Conflicts or failing checks | Ask your instructor — do not force merge |

---

## 7. Command Quick Reference

| Command | What It Does |
|---|---|
| `git status` | Shows current branch and any uncommitted changes |
| `git checkout branch-name` | Switch to an existing branch |
| `git checkout -b new-branch` | Create and switch to a new branch |
| `git pull origin branch-name` | Download the latest changes from GitHub |
| `git add .` | Stage all changed files for commit |
| `git commit -m "message"` | Save a snapshot with a description |
| `git push origin branch-name` | Upload your commits to GitHub |
| `git log --oneline` | See a short history of commits on the current branch |
| `git stash` | Temporarily save uncommitted changes |
| `git stash pop` | Restore the most recently stashed changes |
| `ls` | List files and folders in your current directory |
| `cd folder-name` | Navigate into a folder |
| `cd ..` | Go up one level in the directory |

---

## 8. Good Habits

- **Pull before you start** — always get the latest code first
- **Commit often** — small, frequent commits are better than one giant one at the end
- **Write clear commit messages** — future you will thank present you
- **Never push directly to `main` or `dev`**
- **One file per student** on mini assignments — never edit a classmate's file
- **PR into the right base branch** — `gh#` for assignments, `dev` for the project
- **Ask for help early** — Git errors are fixable, but easier when caught right away
- **Your commit history is visible** — contribute honestly and consistently

---

*Questions? Check the `contributing.md` file in the class repo, or ask Mr. Berg.*