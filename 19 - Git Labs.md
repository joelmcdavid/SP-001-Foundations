# 🧪 19 - Git Labs

## 🎯 Purpose

Reading creates understanding.

Labs create skill.

Complete each lab without looking at the answer first.

If stuck, use the hints.

Only use the solution after attempting the challenge.

---

# 🧪 Lab 01 - Git Basics

## Challenge

Create a repository called:

`git-lab-01`

Create:

`app.txt`

Add:

`Version 1`

Create a commit.

Update the file.

Add:

`Version 2`

Create another commit.

View the history.

---

## Hint

Think about:

- Repository creation
- Staging
- Committing
- Viewing history

---

## Solution

```bash
mkdir git-lab-01

cd git-lab-01

git init

echo "Version 1" > app.txt

git add .

git commit -m "Initial commit"

echo "Version 2" >> app.txt

git add .

git commit -m "Updated app"

git log
```

---

## What You Learned

- git init
- git add
- git commit
- git log

---

## Troubleshooting

Nothing to commit?

Run:

```bash
git status
```

Check whether file changes were staged.

---

# 🧪 Lab 02 - Local vs Remote Repository

## Challenge

Create a GitHub repository.

Connect your local repository.

Push your commits.

Modify the file.

Push again.

---

## Hint

You need:

- Remote
- Push
- Commit

---

## Solution

```bash
git remote add origin <repository-url>

git push -u origin main

echo "Version 3" >> app.txt

git add .

git commit -m "Version 3"

git push
```

---

## What You Learned

Local Repository

↓

Push

↓

GitHub Repository

---

## Troubleshooting

Authentication issue?

Check:

```bash
git remote -v
```

and verify PAT or SSH configuration.

---

# 🧪 Lab 03 - Recovery Commands

## Challenge

Modify:

`app.txt`

Undo the changes.

Create a bad commit.

Undo the commit safely.

Move the repository back one commit.

---

## Solution 1 - Restore File

```bash
git restore app.txt
```

---

## Solution 2 - Revert Commit

```bash
git revert HEAD
```

---

## Solution 3 - Reset History

```bash
git reset --hard HEAD~1
```

---

## What You Learned

| Problem | Command |
|----------|----------|
| Bad file change | git restore |
| Bad commit | git revert |
| Move backwards | git reset |

---

# 🧪 Lab 04 - Branching

## Challenge

Create:

`feature-login`

Add:

`login.txt`

Commit the file.

Switch back to Main.

Return to the feature branch.

---

## Solution

```bash
git switch -c feature-login

touch login.txt

git add .

git commit -m "Added login file"

git switch main

git switch feature-login
```

---

## What You Learned

Main

↓

Feature Branch

↓

Commit

↓

Switch Back

---

# 🧪 Lab 05 - Merging

## Challenge

Create a branch.

Make changes.

Merge them into Main.

---

## Solution

```bash
git switch -c feature-login

touch login.txt

git add .

git commit -m "Added login feature"

git switch main

git merge feature-login
```

---

## What You Learned

Git combines two development timelines.

---

# 🧪 Lab 06 - Merge Conflict Lab

## Challenge

Force Git to create a conflict.

Main:

```text
Server=Production
```

Feature:

```text
Server=Production-01
```

Merge them.

Resolve conflict.

---

## Expected Conflict

```text
<<<<<<< HEAD

Server=Production

=======

Server=Production-01

>>>>>>> feature-login
```

---

## Resolution

Choose the correct value:

```text
Server=Production-01
```

Remove all conflict markers.

Save file.

---

## Complete Merge

```bash
git add app.txt

git commit
```

---

## What You Learned

- Why conflicts happen
- How conflicts are fixed

---

# 🧪 Lab 07 - Pull Requests

## Challenge

Create a feature.

Push branch.

Create Pull Request.

Merge Pull Request.

Delete branch.

---

## Solution

```bash
git switch -c feature-profile

touch profile.txt

git add .

git commit -m "Added profile feature"

git push -u origin feature-profile
```

Then:

1. Open GitHub
2. Create Pull Request
3. Review
4. Merge
5. Delete Branch

---

## What You Learned

Feature Branch

↓

Push

↓

Pull Request

↓

Review

↓

Merge

---

# 🧪 Lab 08 - Git Stash

## Challenge

Start editing a file.

Don't commit.

Switch tasks.

Save work temporarily.

Return later.

Continue working.

---

## Solution

```bash
git stash

git switch main

git switch feature-login

git stash pop
```

---

## Bonus

View stashes:

```bash
git stash list
```

---

## What You Learned

Stash allows unfinished work to be temporarily stored.

---

# 🧪 Lab 09 - Rebase

## Challenge

Create three commits.

Update Main.

Rebase feature branch onto Main.

---

## Solution

```bash
git switch feature-login

git rebase main
```

---

## Bonus

Interactive Rebase:

```bash
git rebase -i HEAD~3
```

Try:

- Squash
- Reorder
- Rename commits

---

## What You Learned

Merge combines histories.

Rebase rewrites history into a cleaner timeline.

---

# 🧪 Lab 10 - Real DevOps Workflow

## Challenge

Simulate an actual team workflow.

---

## Solution

```bash
git switch main

git pull

git switch -c feature-login

git add .

git commit -m "Added login feature"

git push -u origin feature-login
```

Then:

1. Create Pull Request
2. Request Review
3. Merge
4. Delete Branch

---

## What You Learned

Professional Workflow

Pull

↓

Branch

↓

Develop

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

# 🏆 Final Git Mastery Questions

Without notes, answer:

1. Difference between fetch and pull?
2. Difference between merge and rebase?
3. When do you use stash?
4. Why use feature branches?
5. What causes merge conflicts?
6. Why are Pull Requests important?
7. When should revert be used?
8. When should reset be used?
9. What is a tracking branch?
10. What is the Golden Branch?

---

# 💡 Solutionist Wisdom

Knowledge is knowing the command.

Understanding is knowing when to use the command.

Wisdom is knowing when not to use the command.

The goal is not command memorisation.

The goal is workflow mastery.
