# 📚 SP-016: Git Branching, Merging & Team Collaboration

## 🎯 Learning Objectives

Understand:

- Main branch
- Development branch
- Feature branches
- Hotfixes
- Merge workflows
- Merge conflicts
- Team collaboration

---

# 🌳 Branch Types

## Main

🏆 Golden Branch

Production ready.

---

## Development

🔨 Working branch.

Used for active development.

---

## Feature Branch

🚀 New functionality.

Examples:

- feature-login
- feature-api

---

## Hotfix Branch

🚨 Production fixes.

Examples:

- hotfix-authentication
- hotfix-security

---

# 🏗️ Team Workflow

Main

↓

Development

↓

Feature Branch

↓

Commit

↓

Push

↓

Pull Request

↓

Review

↓

Merge

↓

Main

---

# 🔀 Merge

Combines branches together.

Example:

`git merge feature-login`

---

# ⚡ Fast Forward Merge

Main contains no extra commits.

Git simply moves forward.

Simple.

Clean.

---

# ⚠️ Merge Conflict

Occurs when two developers modify the same lines.

Git asks:

"Which version should I keep?"

---

# ✅ Conflict Resolution

Open file

↓

Review both versions

↓

Choose correct version

↓

Remove markers

↓

git add

↓

git commit

Conflict resolved.

---

# 🧼 Daily Git Hygiene

Every Morning:

Switch To Main

↓

Pull Latest Changes

↓

Switch To Development

↓

Merge Main

↓

Start Work

Repeat throughout day.

---

# 🧠 Solutionist Wisdom

Most merge conflicts are not technical problems.

They are communication problems arriving in technical form.
