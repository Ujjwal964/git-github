# GIT | GITHUB 🚀

This repository contains my **hands-on practice while learning Git & GitHub**.  
I practiced all commands on my local machine 💻, created a repository, added files, committed them, pushed to GitHub, and this README is also part of the same learning repo 📘.

---

# GIT 🛠️

1. Famous FREE OPEN SOURCE VCS (Version Control System)  
2. Used to keep track of every code version change. We can revert back to a specific version if there's a bug. When a project gets big, it becomes tough to manage code, so companies use VCS. The most commonly used VCS are: Git, Piper, etc.

---

## INSTALLATION ⚙️

To use Git, download the Git version from Chrome → **git scm** website.  

In terminal, search for git or use:

```bash
git -v
```

It will confirm if Git is installed or not.

Set your global username and email:

```bash
git config --global user.name "your name"
git config --global user.email "your email"
```

**Why do this?** Because whenever you make a commit, it shows which person (username & email) made that commit.

Post this, we can start in our project → open in VS Code → go to code directory.

Initialize Git using:

```bash
git init
```

Now Git will create a folder called `.git` and will keep track of the project.

Install **Git Graph extension** in VS Code for better visualization 📊.

---

## ADDING USING GIT ➕

If your file in VS Code shows **'U'**, it means **untracked** (Git is not tracking it).

To make it tracked:

```bash
git add <filepath>
```

Now BOOM 💥 Git will track and show as **'A'**.

Whenever you write something in the file, it will show that line as green.

To check added changes:

```bash
git diff
```

Since projects usually have many files, we use:

```bash
git add .
```

This adds all files of the directory and Git starts tracking all.

To remove a file from tracking:

```bash
git rm <filepath>
```

---

## COMMITS 💾

Git version changes over time.  
Every change in code with time is called a **Commit**.

Whenever we make changes, we commit:

```bash
git commit -m "First Commit"
```

After committing, you can see at what time and which person added which code.

To check commit history:

```bash
git log
git log --oneline
git show <commitID>
git blame <filepath>
```

We always do:

```bash
git add .
git commit -m "message"
```

**Best practice:** Keep commits clean. Don’t commit everything at once. Add one functionality → commit → repeat.

Using:

```bash
git status
```

we can see which files got modified/updated.

---

## HOW TO REVERT BACK? ⏪

What is Linked List → ⭕️ → ⭕️ → ⭕️  
Means one node is connected to another. Current node is HEAD and previous is TAIL.  
Git commit history also works like a Linked List, and HEAD points to the latest commit.

Two ways to revert back:

### HARD Approach ⚠️
```bash
git reset --hard <commitId>
```
Head moves back and later commits get lost.

### SAFE WAY ✅
```bash
git revert <commitId>
```
It reverts only that specific commit and creates a new commit without breaking history.

---

## GIT COLLABORATION 🤝

Two people working on the same project stay in sync using **push & pull**.

Common Git servers:
- GITHUB (free)  
- GITLAB (paid)  
- BITBUCKET (paid)

---

# GITHUB 🌍

GitHub is a **Git Server**: Central server where developers push & pull their code.  
Git is the version control system, and GitHub is the central remote server (Single Source Of Truth).

If we don’t have GitHub, we use:

```bash
git init
```

But if using GitHub, we create a repo there and connect:

```bash
git remote -v
git remote add origin <repo path>
git push -u origin main
```

---

## AUTHENTICATION (SSH) 🔐

We need SSH Keys (public & private).  
Add SSH key in GitHub settings after generating it locally.

Workflow:

```bash
git status
git diff
git add .
git commit -m "message"
git push
```

To revert remote using hard reset:

```bash
git reset --hard <commitId>
git push -f
```

---

# BRANCHING IN GITHUB 🌿

A branch is like a railway track of commits.

Why need branching? To avoid polluting the main branch when multiple people are working.

Commands:

```bash
git branch
git branch <branchname>
git checkout <branchname>
git checkout -b <branchname>
git push -u origin <branchname>
```

---

## MERGING 🔀

### CLI
```bash
git checkout main
git merge origin/<branchname>
git push
```

### GitHub UI
After merging on GitHub:

```bash
git checkout main
git pull
```

---

## BRANCH NAME SHOULD BE? 🏷️

feat, wip, bug, junk  

Examples:
```
feat/add-skip-button
bug/login-not-working
wip/working
junk/test-no-use
```

---

## REBASE 🔁

Rebase keeps full commit history instead of combining.

```bash
git rebase <branchname>
```

Mostly merge is preferred.

---

## STASHING (Temp Commit) 📦

Used when you want to pull but have unfinished work.

```bash
git stash
git pull
git stash apply
```

---

# TOOLS PREFER FOR FUTURE PRACTISE 🧰

1. [GIT CHEATSHEET CHROME (GitHub Education PDF)](https://education.github.com/git-cheat-sheet-education.pdf)
2. GIT VISUALIZER CHROME  
3. VS CODE EXTEN (Git Graph, Git Lens)

---

**END OF MY GIT & GITHUB BEGINNER NOTES ✨**
