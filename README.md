# Case-Study-Wilderness-Weathering-System

This is for learning git contribution

# Guideline for work flow

# Wilderness Weathering System

## Git Team Workflow

This document explains how every team member should use Git when contributing to the Wilderness Weathering System project.

---

## 1. Clone the Repository

First, clone the repository to your computer.

```bash
git clone https://github.com/Nak-Danin/Case-Study-Wilderness-Weathering-System.git
```

Enter the project folder:

```bash
cd Wilderness-Weathering-System
```

---

## 2. Check the Current Branch

Before starting any work:

```bash
git branch
```

You should normally see:

```text
* main
```

---

## 3. Get the Latest Changes

Always make sure you have the latest version before creating your branch:

```bash
git pull origin main
```

---

## 4. Create Your Own Branch

**Do not work directly on `main`.**

Create a branch for your task:

```bash
git switch -c feature/your-task
```

For example:

```bash
git switch -c feature/urd
```

Or:

```bash
git switch -c feature/use-case-diagram
```

### Branch Naming

Use this format:

```text
feature/task-name
```

Examples:

```text
feature/urd
feature/srs
feature/functional-requirements
feature/use-case-diagram
feature/activity-diagram
feature/class-diagram
```

---

## 5. Work on Your Assigned Task

Edit or create the files related to your assigned task.

For example:

```text
docs/
└── SRS/
    └── functional-requirements.md
```

Write your content using Markdown.

---

## 6. Check Your Changes

Before committing, check which files you changed:

```bash
git status
```

You can also see the changes:

```bash
git diff
```

---

## 7. Add Your Changes

Add your files:

```bash
git add .
```

Or add a specific file:

```bash
git add docs/SRS/functional-requirements.md
```

---

## 8. Commit Your Changes

Create a commit with a clear message:

```bash
git commit -m "Add functional requirements"
```

### Good Commit Messages

```text
Add URD introduction
Add system objectives
Add functional requirements
Add use case diagram
Update system scope
Fix SRS requirements
```

Avoid unclear messages such as:

```text
update
changes
stuff
final
asdf
```

---

## 9. Push Your Branch

Push your branch to GitHub:

```bash
git push -u origin feature/your-task
```

For example:

```bash
git push -u origin feature/urd
```

After the first push, you can usually use:

```bash
git push
```

---

## 10. Create a Pull Request

After pushing your branch:

1. Open the GitHub repository.
2. Go to **Pull Requests**.
3. Click **New Pull Request**.
4. Select your branch.
5. Set the destination branch to `main`.
6. Add a short description of your changes.
7. Create the Pull Request.
8. Ask another team member to review it.

Do **not** merge your own Pull Request unless the team has agreed that this is allowed.

---

# Updating Your Branch

While you are working, another team member may merge changes into `main`.

Before continuing your work, update your local repository:

```bash
git switch main
git pull origin main
```

Then return to your branch:

```bash
git switch feature/your-task
```

Update your branch with the latest `main`:

```bash
git merge main
```

If there are no conflicts, continue working.

---

# If You Have Merge Conflicts

Git may report a conflict if two people changed the same part of a file.

For example:

```text
CONFLICT (content): Merge conflict in functional-requirements.md
```

Open the file and look for:

```text
<<<<<<< HEAD
Your changes
=======
Changes from main
>>>>>>> main
```

Decide which content should remain, then remove the conflict markers:

```text
<<<<<<<
=======
>>>>>>>
```

After fixing the conflict:

```bash
git add .
git commit -m "Resolve merge conflict"
git push
```

---

# Important Team Rules

### 1. Never work directly on `main`

Always create your own branch:

```bash
git switch -c feature/your-task
```

### 2. Pull before starting new work

```bash
git switch main
git pull origin main
```

### 3. Use clear commit messages

Good:

```bash
git commit -m "Add system objectives"
```

Bad:

```bash
git commit -m "update"
```

### 4. Do not overwrite another member's work

Before editing a file, check whether someone else is currently working on it.

### 5. Keep commits focused

A commit should represent one logical piece of work.

Good:

```text
Add system objectives
```

Then another commit:

```text
Add system scope
```

Instead of putting everything into one huge commit:

```text
Finish entire project
```

---

# Recommended Workflow

Every time you start working:

```bash
git switch main
git pull origin main
git switch -c feature/your-task
```

Work on your task.

Then:

```bash
git status
git add .
git commit -m "Describe your changes"
git push -u origin feature/your-task
```

Then create a **Pull Request** on GitHub.

---

# Example

Suppose you are responsible for the URD.

Start:

```bash
git switch main
git pull origin main
git switch -c feature/urd
```

Create/edit:

```text
docs/URD/introduction.md
docs/URD/objectives.md
docs/URD/scope.md
```

Then:

```bash
git add .
git commit -m "Add URD introduction objectives and scope"
git push -u origin feature/urd
```

Finally, create a Pull Request:

```text
feature/urd → main
```

After the team reviews it, merge it into `main`.

---

# Quick Reference

```bash
# Get latest project
git switch main
git pull origin main

# Create your branch
git switch -c feature/your-task

# Check changes
git status
git diff

# Save your work
git add .
git commit -m "Describe your changes"

# Upload your branch
git push -u origin feature/your-task

# After your Pull Request is merged,
# update your local main branch
git switch main
git pull origin main
```

## Golden Rule

**Pull → Branch → Work → Commit → Push → Pull Request → Review → Merge**
