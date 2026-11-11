# 📚 SP-017: Pull Requests, Reviews, Rebase & Modern Git

## 🎯 Learning Objectives

Understand:

- Pull Requests
- Reviews
- Rebase
- git switch
- Remote branches
- Stash
- Feature workflows

---

# 🔄 Modern Git

Use:

`git switch`

For branch management.

Use:

`git restore`

For file recovery.

---

# 🌳 Branch Management

Switch branch:

`git switch main`

Create and switch:

`git switch -c feature-login`

Return to previous branch:

`git switch -`

---

# 🌍 Local + Remote Branches

Show all branches:

`git branch -a`

Show branches with commit information:

`git branch -a -v`

Show tracking information:

`git branch -vv`

---

# 📥 Bring Remote Branch Locally

Fetch updates:

`git fetch --all`

Create local tracking branch:

`git switch -c dev origin/dev`

Verify:

`git branch -vv`

---

# 📋 Pull Request Workflow

Feature Branch

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

# 👀 Why Pull Requests Exist

They provide:

✅ Reviews

✅ Testing

✅ Approval

✅ Quality Control

✅ Safer Releases

---

# 🔄 Rebase

Update branch with latest Main.

`git rebase main`

Think:

"Replay my commits on top of Main."

---

# 🧹 Interactive Rebase

`git rebase -i HEAD~3`

Allows:

- Squash commits
- Edit messages
- Remove commits
- Reorder commits

---

# 📦 Stash Workflow

Work In Progress

↓

git stash

↓

Switch Tasks

↓

Return

↓

git stash pop

↓

Continue Work

---

# 🏢 Professional Workflow

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

# 🧠 Solutionist Wisdom

A beginner finishes when they commit.

A developer finishes when they push.

A professional finishes when the Pull Request is approved.

A Solutionist finishes when the change safely reaches production and delivers value.
