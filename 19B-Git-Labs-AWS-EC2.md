# 🧪 19B - Git Labs On AWS EC2

# 🎯 Mission

This lab series teaches Git in a realistic DevOps environment.

Instead of running Git locally on Windows, you will:

- Launch an EC2 instance
- Connect using SSH
- Work as ec2-user
- Clone repositories
- Create branches
- Resolve conflicts
- Create pull requests
- Use stash
- Use rebase

This simulates real DevOps workflows.

---

# 🏗️ Lab Environment

Laptop

↓

SSH

↓

AWS EC2

↓

Git Repository

↓

GitHub

---

# ✅ Lab 01 - Connect To EC2

## Objective

Successfully connect from your PC to an AWS EC2 instance.

---

## Challenge

Connect to EC2 using your key pair.

Verify connection.

Display current user.

Display current directory.

---

## Hint

Think:

- ssh
- whoami
- pwd

---

## Solution

```bash
ssh -i key.pem ec2-user@PUBLIC-IP

whoami

pwd
```

Expected output:

```text
ec2-user
/home/ec2-user
```

---

## What You Learned

- SSH
- Linux login
- EC2 access

---

# ✅ Lab 02 - Prepare Workspace

## Objective

Create a Git workspace.

---

## Challenge

Create:

```text
~/git-labs
```

Move into it.

Create:

```text
lab01
```

---

## Solution

```bash
mkdir ~/git-labs

cd ~/git-labs

mkdir lab01

cd lab01
```

---

## Verify

```bash
pwd
```

Expected:

```text
/home/ec2-user/git-labs/lab01
```

---

# ✅ Lab 03 - Initialise Git Repository

## Objective

Start a Git repository from scratch.

---

## Challenge

Initialise Git.

Create:

```text
app.txt
```

Add text.

Commit changes.

---

## Solution

```bash
git init

echo "Version 1" > app.txt

git add .

git commit -m "Initial Commit"
```

---

## Verify

```bash
git log
```

---

## What You Learned

- git init
- git add
- git commit
- git log

---

# ✅ Lab 04 - Configure Git Identity

## Objective

Configure your Git user.

---

## Challenge

Check configuration.

Add username.

Add email.

Verify settings.

---

## Solution

```bash
git config --global user.name "Joel"

git config --global user.email "your@email.com"

git config --global --list
```

---

## Verify

Look for:

```text
user.name
user.email
```

---

# ✅ Lab 05 - Clone A GitHub Repository

## Objective

Clone a repository onto EC2.

---

## Challenge

Clone your SP-001 repository.

---

## Hint

Use:

```bash
git clone
```

---

## Solution

```bash
git clone https://github.com/YOUR-USERNAME/SP-001-Foundations.git
```

---

## Verify

```bash
ls
```

Repository should appear.

---

# ✅ Lab 06 - Local vs Remote

## Objective

Understand repository relationships.

---

## Challenge

Display configured remotes.

---

## Solution

```bash
git remote -v
```

Expected:

```text
origin (fetch)

origin (push)
```

---

## What You Learned

Local Repository

↓

Remote Repository

↓

GitHub

---

# ✅ Lab 07 - Create Feature Branch

## Objective

Work safely outside Main.

---

## Challenge

Create:

```text
feature-login
```

Switch to it.

---

## Solution

```bash
git switch -c feature-login
```

---

## Verify

```bash
git branch
```

Expected:

```text
* feature-login
```

---

# ✅ Lab 08 - Create And Commit Work

## Objective

Create meaningful commits.

---

## Challenge

Create:

```text
login.txt
```

Add content.

Commit.

---

## Solution

```bash
echo "Login Feature" > login.txt

git add .

git commit -m "Added login feature"
```

---

## Verify

```bash
git log
```

---

# ✅ Lab 09 - Push To GitHub

## Objective

Upload work.

---

## Challenge

Push branch to GitHub.

---

## Solution

```bash
git push -u origin feature-login
```

---

## Expected Result

GitHub now contains:

```text
feature-login
```

---

# ✅ Lab 10 - Simulate A Merge Conflict

## Objective

Experience a real conflict.

---

## Challenge

Edit same file in:

- main
- feature-login

Then merge.

---

## Solution

Switch main:

```bash
git switch main
```

Edit:

```bash
nano app.txt
```

Commit.

Switch:

```bash
git switch feature-login
```

Edit same line.

Commit.

Merge:

```bash
git merge main
```

---

## Expected Conflict

```text
<<<<<<< HEAD

=======

>>>>>>>
```

---

# ✅ Lab 11 - Resolve Conflict

## Objective

Fix a conflict manually.

---

## Solution

Open file:

```bash
nano app.txt
```

Remove:

```text
<<<<<<<
=======
>>>>>>>
```

Choose correct content.

Save file.

Then:

```bash
git add app.txt

git commit
```

---

## Result

Conflict resolved.

---

# ✅ Lab 12 - git show Investigation

## Objective

Investigate commit history.

---

## Challenge

Inspect an old commit.

---

## Solution

```bash
git log
```

Copy a commit ID.

Then:

```bash
git show COMMIT-ID
```

---

## Observe

- Author
- Date
- Message
- Diff

---

# ✅ Lab 13 - Stash Workflow

## Objective

Handle interruptions.

---

## Challenge

Create unfinished work.

Store it.

Restore it later.

---

## Solution

```bash
git stash

git stash list

git stash pop
```

---

## Mental Model

Work Bench

↓

Stash

↓

Emergency Task

↓

Return

↓

Continue Work

---

# ✅ Lab 14 - Rebase Workflow

## Objective

Create clean history.

---

## Challenge

Create multiple commits.

Rebase onto Main.

---

## Solution

```bash
git rebase main
```

---

## Bonus

```bash
git rebase -i HEAD~3
```

Try:

- squash
- reword
- reorder

---

# ✅ Lab 15 - Full DevOps Workflow

## Objective

Perform entire Git lifecycle.

---

## Workflow

SSH To EC2

↓

Clone Repository

↓

Pull Latest Main

↓

Create Feature Branch

↓

Make Changes

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

Delete Branch

---

# 🏆 Final Challenge

Without notes:

1. Launch EC2
2. SSH
3. Clone Repository
4. Create Branch
5. Commit Work
6. Push Branch
7. Create PR
8. Merge PR
9. Create Conflict
10. Resolve Conflict
11. Stash Work
12. Restore Work
13. Rebase Branch

If you can do all 13 steps without checking notes, you've moved beyond "learning Git" and into "using Git professionally."

---

# 💡 Solutionist Wisdom

A beginner learns Git commands.

A developer learns Git workflows.

A DevOps engineer learns Git in Linux.

A Solutionist learns that Git, Linux, AWS and GitHub are not separate skills.

They are one connected system that moves ideas from a laptop into production safely.
