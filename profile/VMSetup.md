# Getting Started: Your Virtual Machine

**Introduction to AI | Lane Tech College Prep**

---

## Overview

For this course you will do all of your coding inside a virtual machine (VM) hosted by Itopia. Think of it as a computer inside your Chromebook. It has everything you need pre-installed — Visual Studio Code, a terminal, and access to GitHub. All other websites are restricted inside the VM, but you can still open other tabs on your Chromebook normally.

---

## Step 1 — Log Into Your VM

1. Open a new tab on your Chromebook and go to [labs.itopia.com](https://labs.itopia.com)
2. Click **Sign in with Google** and use your CPS Google account
3. You will see your VM instance — it should already be started
4. Click on the instance to connect
5. Your VM desktop will load in the browser

> **If your instance is not started**, let Mr. Berg know. Do not try to start it yourself.

---

## Step 2 — Log Into GitHub in Chrome

Before opening VS Code, log into GitHub in your Chromebook's browser first. This makes the VS Code login process much smoother.

1. Open a new tab on your Chromebook (outside the VM)
2. Go to [github.com](https://github.com)
3. Sign in with your GitHub account
4. Keep this tab open

---

## Step 3 — Open VS Code in Your VM

1. Inside your VM, find the **VS Code** icon on the desktop or taskbar and open it
2. Once VS Code is open, sign in with your GitHub account:
   - Click the **Accounts** icon in the bottom left corner of VS Code
   - Click **Sign in with GitHub**
   - Follow the prompts — since you are already logged into GitHub in your browser, this should complete quickly
3. You are now connected and ready to work

---

## Step 4 — Clone Your First Repository

Once you are logged in, you will clone the class assignments repository so it lives inside your VM.

1. Open a terminal in VS Code:
   - Click **Terminal** in the top menu
   - Click **New Terminal**
2. In the terminal, run:
```bash
git clone https://github.com/LT-IntroToAI-SY2627/assignments.git
```
3. Navigate into the repo folder:
```bash
cd assignments
```
4. You are now inside the class repo and ready to start GH-1

---

## What You Have Access To Inside the VM

| Available | Not Available |
|---|---|
| Visual Studio Code | Most websites |
| GitHub | — |
| Google Classroom | — |
| Terminal | — |

> **Need to visit another site?** Switch to a regular tab on your Chromebook outside the VM.

---

## Every Day Workflow

When you sit down in class, here is what to do:

1. Go to [labs.itopia.com](https://labs.itopia.com) and connect to your instance
2. Open VS Code
3. Open a terminal and navigate to your repo
4. Fetch all branches so Git knows about any new assignments:
```bash
git fetch origin
```
5. Pull the latest changes before you start working:
```bash
git pull origin <branch-name>
```

---

*Questions? Ask Mr. Berg or check the [GitHub Workflow Guide](https://github.com/LT-IntroToAI-SY2627/.github/blob/main/profile/GITHUB_WORKFLOW.md).*
