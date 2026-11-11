# 📚 SP-015: Git Collaboration, Synchronisation & Recovery

## 🎯 Learning Objectives

Understand:

- Fetch
- Pull
- Diff
- Restore
- Revert
- Reset
- Stash
- Recovery workflows

---

# 🔄 Synchronisation Workflow

Fetch

↓

Diff

↓

Pull

---

## Fetch

`git fetch`

Downloads updates.

Does NOT apply updates.

Think:

"Show me what's new."

---

## Diff

`git diff origin/main`

Shows differences.

🟢 Added

🔴 Removed

Think:

"Explain what changed."

---

## Pull

`git pull`

Downloads and applies.

Think:

"Update my copy."

---

# 🩹 Recovery Ladder

restore

↓

revert

↓

reset

↓

push -f

---

## git restore

Undo file changes.

Safest option.

---

## git revert

Undo commit safely.

Creates a new commit.

Safe for teams.

---

## git reset

Move branch backwards.

Can rewrite history.

---

## git push -f

Force GitHub history to match yours.

Dangerous.

Use carefully.

---

# 📦 Stash Workflow

Working

↓

git stash

↓

Emergency Task

↓

Fix Issue

↓

Return

↓

git stash pop

↓

Continue Work

---

# 🧠 Solutionist Wisdom

Professionals don't avoid mistakes.

Professionals build systems that make recovery safe.
