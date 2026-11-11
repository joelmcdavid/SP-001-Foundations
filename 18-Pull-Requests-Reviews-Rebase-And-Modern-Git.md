# 📚 18 - Pull Requests, Reviews, Rebase & Modern Git

## 🎯 Learning Objectives

By the end of this lesson, you will understand:

- Pull Requests (PRs)
- Code Reviews
- Approvals
- Modern Git commands
- `git switch`
- `git switch -c`
- Local vs Remote Branches
- Tracking Branches
- Git Stash
- Git Rebase
- Interactive Rebase
- Professional Git Workflows

---

# 🧠 Why This Lesson Matters

Learning Git commands is not enough.

Professional teams care about:

- Collaboration
- Testing
- Reviews
- Approvals
- Clean commit history
- Safe deployments

This lesson teaches how work moves safely from a developer's laptop into production.

---

# 🔄 Modern Git Philosophy

Historically Git used:

`git checkout`

for many different tasks:

- Switching branches
- Creating branches
- Restoring files
- Viewing old commits

This made Git confusing.

Modern Git separates responsibilities:

- `git switch` → Branch management
- `git restore` → File recovery

This makes workflows safer and easier to understand.

---

# 🌳 git switch

Used to move between existing branches.

Example:

`git switch main`

Purpose:

- Move between branches
- Update working files
- Continue working elsewhere

### 🚂 Train Analogy

Think of branches as railway tracks.

`git switch`

moves your train onto a different track.

---

# 🌳 git switch -c

Creates and switches to a new branch.

Example:

`git switch -c feature-login`

This:

- Creates a branch
- Immediately switches to the branch

Equivalent old syntax:

`git checkout -b feature-login`

### 🚂 Train Analogy

Build a new railway track and move onto it immediately.

---

# 🔙 Return To Previous Branch

Command:

`git switch -`

Purpose:

Return to the branch you were working on before.

Useful when jumping between:

- Main
- Development
- Feature branches

---

# ⚖️ git switch vs git checkout

## git switch

Use for:

- Branch management
- Branch creation

Examples:

`git switch main`

`git switch -c feature-api`

Benefits:

✅ Cleaner

✅ Easier

✅ Safer

✅ Recommended

---

## git checkout

Can perform:

- Branch switching
- Branch creation
- File restoration
- Commit inspection

Examples:

`git checkout main`

`git checkout -b dev`

`git checkout a3f9c2d`

Benefits:

✅ More powerful

Disadvantages:

⚠️ Easier to misuse

⚠️ Easier to enter Detached HEAD accidentally

⚠️ Easier to accidentally restore files

---

# 💡 Solutionist Rule

Use:

`git switch`

for branches.

Use:

`git restore`

for files.

Use:

`git checkout`

when intentionally viewing historical commits.

---

# 🌍 Local vs Remote Branches

Branches can exist locally or remotely.

## Local Branches

Stored on your machine.

Examples:

- main
- dev
- feature-login

---

## Remote Branches

Stored on GitHub.

Examples:

- origin/main
- origin/dev
- origin/feature-login

---

# 📥 Download Branch Information

Fetch all remote branch information:

`git fetch --all`

Purpose:

- Download branch information
- Download tags
- Refresh remote references

Important:

✅ Downloads information

❌ Does not merge anything

### Mental Model

"Show me every branch available on GitHub."

---

# 🌳 View Branches

Show local branches:

`git branch`

---

Show local + remote branches:

`git branch -a`

Example:

```text
main
dev
remotes/origin/main
remotes/origin/dev
```

---

# 🔍 View Branches With Commit Information

Command:

`git branch -a -v`

Shows:

- Branches
- Last commit hash
- Last commit message

Example:

```text
main      Added Login Feature
dev       Fixed API Bug
origin/main
origin/dev
```

---

# 🧠 Visual Mental Model

`-a`

↓

Show all branches

---

`-v`

↓

Show latest activity on every branch

---

# 🔗 View Tracking Relationships

Command:

`git branch -vv`

Example:

```text
dev [origin/dev]

main [origin/main]
```

Meaning:

Local branches are linked to remote branches.

---

# 🌍 Bring Remote Branches To Your Laptop

## Step 1

Fetch updates.

`git fetch --all`

---

## Step 2

View remote branches.

`git branch -a`

---

## Step 3

Create local tracking branch.

`git switch -c dev origin/dev`

This creates:

Local Branch:

`dev`

Tracking:

`origin/dev`

---

## Step 4

Verify linkage.

`git branch -vv`

---

# 📋 Pull Requests (PR)

A Pull Request is:

> A request to merge one branch into another.

Usually:

Feature Branch

↓

Development

↓

Main

---

# 🎯 Why Pull Requests Exist

Pull Requests provide:

✅ Reviews

✅ Testing

✅ Collaboration

✅ Discussion

✅ Approvals

✅ Safer releases

Without Pull Requests:

Developer

↓

Main

↓

Production

❌ Dangerous

With Pull Requests:

Developer

↓

Feature Branch

↓

Review

↓

Approval

↓

Main

↓

Production

✅ Safe

---

# 🚀 Pull Request Workflow

Feature Branch

↓

Develop Feature

↓

Commit

↓

Push

↓

Create Pull Request

↓

Review

↓

Approval

↓

Merge

↓

Deploy

---

# 👀 Code Reviews

Before merging, another engineer reviews the code.

Reviewers look for:

- Security problems
- Performance issues
- Bug risks
- Coding standards
- Logic errors

Outcomes:

✅ Approved

💬 Comments Added

❌ Changes Requested

---

# 📦 git stash

Used when work is unfinished.

Scenario:

You are building a feature.

Suddenly:

> Production issue needs fixing.

Save current work:

`git stash`

Think:

📦 Put unfinished work into temporary storage.

---

# 📋 View Stashes

`git stash list`

Example:

```text
stash@{0}
stash@{1}
stash@{2}
```

---

# 🔄 Restore Stashed Work

Command:

`git stash pop`

Purpose:

- Restore work
- Remove stash entry

---

# 🔄 Restore Without Removing

Command:

`git stash apply`

Purpose:

- Restore work
- Keep stash

Useful for testing.

---

# 🔄 What Is Rebase?

Rebase allows you to:

> Replay your commits on top of another branch.

Most common example:

`git rebase main`

Purpose:

Keep history clean.

---

# 🔀 Merge vs Rebase

## Merge

History:

Main

↓

Feature

↓

Merge Commit

Creates extra merge commits.

---

## Rebase

History:

Main

↓

Commit A

↓

Commit B

↓

Commit C

Creates a cleaner timeline.

---

# ✅ Why Teams Use Rebase

Benefits:

- Cleaner history
- Easier debugging
- Cleaner git log
- Better Pull Requests
- Less merge noise

---

# 🧹 Interactive Rebase

Command:

`git rebase -i HEAD~3`

Meaning:

Edit the last 3 commits.

---

# Interactive Rebase Allows

✅ Squash commits

✅ Edit commit messages

✅ Remove commits

✅ Reorder commits

---

# Example

Before:

```text
Fixed typo

Fixed typo again

Actually fixed typo
```

After:

```text
Improved Login Validation
```

Much cleaner history.

---

# ⚠️ Rebase Warning

Rebase rewrites commit history.

Avoid rebasing:

❌ Main Branch

❌ Shared Team Branches

❌ Active Collaboration Branches

Safe Uses:

✅ Personal Feature Branches

✅ Pull Request Clean-up

✅ Branch Maintenance

---

# 🏢 Professional Workflow

Start Day

↓

`git switch main`

↓

`git pull`

↓

Create Feature Branch

↓

`git switch -c feature-login`

↓

Develop Feature

↓

`git add .`

↓

`git commit`

↓

Need Emergency Fix?

↓

`git stash`

↓

Create Bug Fix Branch

↓

Fix Problem

↓

Commit

↓

Return To Feature

↓

`git stash pop`

↓

Continue Development

↓

`git rebase main`

↓

Push Branch

↓

Create Pull Request

↓

Review

↓

Approval

↓

Merge

↓

Deploy

---

# ⭐ Git Master Workflow

Pull

↓

Branch

↓

Work

↓

Commit

↓

Push

↓

Pull Request

↓

Review

↓

Approval

↓

Merge

↓

Deploy

---

# 💡 Solutionist Wisdom

A beginner thinks:

> My work is finished when I commit.

A developer thinks:

> My work is finished when I push.

A professional thinks:

> My work is finished when the Pull Request is approved.

A Solutionist thinks:

> My work is finished when the change has been reviewed, tested, merged, deployed, documented, and is safely delivering value to the business.

Git is not simply version control.

Git is a collaboration system that allows hundreds of engineers to safely build, review, improve, and deploy software without breaking the Golden Branch.
