# 📚 SP-014: GitHub & Remote Repositories

## 🎯 Learning Objectives

Understand:

- GitHub
- Local vs Remote Repositories
- Clone
- Push
- Pull
- Authentication
- PATs

---

# 🏠 Local vs Remote

## Local Repository

Lives on your computer.

Contains:

- Files
- Commits
- Branches
- History

Only you can see it.

---

## Remote Repository

Lives on GitHub.

Contains:

- Shared code
- Pull requests
- Reviews
- CI/CD

Everyone can collaborate on it.

---

# 💰 Wallet vs Bank Analogy

Local Repository

💷 Wallet

Remote Repository

🏦 Bank Account

Actions:

Deposit → git push

Withdraw → git pull

Check Activity → git fetch

History → git log

---

# 🚀 GitHub Workflow

Local Repository

↓

git push

↓

GitHub Repository

↓

Team Visibility

↓

Review

↓

Deployment

---

# 📥 Cloning A Repository

HTTPS

`git clone <repository-url>`

SSH

`git clone git@github.com:user/repository.git`

---

# 🔐 Personal Access Tokens (PATs)

PATs replace passwords.

Used for:

- git push
- git pull
- git clone

Never store PATs in repositories.

---

# 🧠 Solutionist Wisdom

Git stores your work.

GitHub shares your work.

Together they create a single source of truth.
