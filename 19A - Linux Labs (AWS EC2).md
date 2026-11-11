# 🧪 19A - Linux Labs (AWS EC2)

# 🎯 Mission

These labs are designed to build real Linux confidence.

You will work as:

`ec2-user`

on an AWS EC2 instance.

The goal is not number memorisation.

The goal is becoming comfortable inside a Linux terminal.

By the end of these labs you should be able to:

✅ Navigate Linux

✅ Work with files

✅ Work with directories

✅ Search for information

✅ Inspect processes

✅ Troubleshoot issues

✅ Manage permissions

✅ Connect using SSH

✅ Think like a junior DevOps engineer

---

# 🏗️ Lab Environment

Laptop

↓

SSH

↓

AWS EC2

↓

Linux Terminal

↓

Problem Solving

---

# ✅ Lab 01 - Connect To EC2

## Objective

Successfully connect to an EC2 instance.

---

## Challenge

Connect to your EC2 instance.

Display:

- Current user
- Current directory
- Server hostname

---

## Hint

Think:

- ssh
- whoami
- pwd
- hostname

---

## Solution

```bash
ssh -i key.pem ec2-user@PUBLIC-IP

whoami

pwd

hostname
```

---

## What You Learned

- SSH
- Linux login
- Server identity

---

# ✅ Lab 02 - Linux Navigation

## Objective

Move around the Linux filesystem.

---

## Challenge

Find:

- Current directory
- Contents of directory
- Home directory

Move into:

```text
Documents
```

Create it if it doesn't exist.

Return home.

---

## Hint

Think:

- pwd
- ls
- cd

---

## Solution

```bash
pwd

ls

mkdir Documents

cd Documents

pwd

cd ~

pwd
```

---

## What You Learned

- pwd
- ls
- cd
- home directory

---

# ✅ Lab 03 - Create Files & Directories

## Objective

Manage files and folders.

---

## Challenge

Create:

```text
projects
```

Inside create:

```text
devops.txt

aws.txt

linux.txt
```

---

## Solution

```bash
mkdir projects

cd projects

touch devops.txt

touch aws.txt

touch linux.txt

ls
```

---

## What You Learned

- mkdir
- touch
- ls

---

# ✅ Lab 04 - Read Files

## Objective

Inspect file contents.

---

## Challenge

Add text to a file.

Display the contents.

---

## Solution

```bash
echo "I love Linux" > linux.txt

cat linux.txt
```

---

## Bonus

```bash
cat -n linux.txt
```

---

## What You Learned

- echo
- cat

---

# ✅ Lab 05 - Copy & Move Files

## Objective

Work with existing files.

---

## Challenge

Create backup copies.

Rename files.

---

## Solution

```bash
cp linux.txt linux-backup.txt

mv linux.txt linux-notes.txt

ls
```

---

## What You Learned

- cp
- mv

---

# ✅ Lab 06 - Delete Files

## Objective

Remove unwanted content.

---

## Challenge

Delete backup file.

Create test folder.

Delete folder.

---

## Solution

```bash
rm linux-backup.txt

mkdir temp

rm -r temp
```

---

## What You Learned

- rm
- rm -r

---

# ✅ Lab 07 - Find Files

## Objective

Locate files anywhere.

---

## Challenge

Find:

```text
linux-notes.txt
```

---

## Hint

Think:

```bash
find
```

---

## Solution

```bash
find ~ -name "linux-notes.txt"
```

---

## What You Learned

- find
- file searching

---

# ✅ Lab 08 - Search Inside Files

## Objective

Search for specific text.

---

## Challenge

Add:

```text
AWS

Linux

Terraform

Docker
```

Search for:

```text
Terraform
```

---

## Solution

```bash
echo "AWS" >> tools.txt

echo "Linux" >> tools.txt

echo "Terraform" >> tools.txt

echo "Docker" >> tools.txt

grep Terraform tools.txt
```

---

## What You Learned

- grep
- searching file contents

---

# ✅ Lab 09 - View Logs

## Objective

Investigate large files.

---

## Challenge

View:

- First lines
- Last lines

---

## Solution

```bash
head tools.txt

tail tools.txt
```

---

## Bonus

```bash
tail -f tools.txt
```

---

## What You Learned

- head
- tail
- log viewing

---

# ✅ Lab 10 - Redirect Output

## Objective

Save output to files.

---

## Challenge

Store command output inside a file.

---

## Solution

```bash
ls > listing.txt

cat listing.txt
```

---

## Append Output

```bash
date >> listing.txt
```

---

## What You Learned

- >
- >>

---

# ✅ Lab 11 - Pipe Commands

## Objective

Chain commands together.

---

## Challenge

Display only matching data.

---

## Solution

```bash
ls | grep txt
```

---

## Bonus

```bash
cat tools.txt | grep Linux
```

---

## What You Learned

- pipe operator |
- command chaining

---

# ✅ Lab 12 - Running Processes

## Objective

Inspect running processes.

---

## Challenge

Display active processes.

---

## Solution

```bash
ps

ps -ef
```

---

## Bonus

```bash
top
```

Exit:

```text
q
```

---

## What You Learned

- ps
- top

---

# ✅ Lab 13 - Kill A Process

## Objective

Stop unwanted processes.

---

## Challenge

Start a long-running process.

Find PID.

Terminate process.

---

## Solution

```bash
sleep 600 &
```

Find process:

```bash
ps -ef | grep sleep
```

Terminate:

```bash
kill PID
```

---

## Verify

```bash
ps -ef | grep sleep
```

---

## What You Learned

- background processes
- PID
- kill

---

# ✅ Lab 14 - Linux Permissions

## Objective

Manage execution rights.

---

## Challenge

Create script.

Make executable.

Run script.

---

## Solution

```bash
touch script.sh

chmod +x script.sh

./script.sh
```

---

## View Permissions

```bash
ls -l
```

---

## What You Learned

- chmod
- file permissions

---

# ✅ Lab 15 - Networking & DNS

## Objective

Investigate DNS.

---

## Challenge

Lookup GitHub.

---

## Solution

```bash
host github.com
```

---

## Bonus

```bash
dig github.com
```

---

## What You Learned

- host
- dig
- DNS

---

# ✅ Lab 16 - Download Files

## Objective

Retrieve data from internet.

---

## Challenge

Download a web page.

---

## Solution

```bash
curl https://github.com
```

---

## Bonus

```bash
wget https://github.com
```

---

## What You Learned

- curl
- wget

---

# ✅ Lab 17 - SCP Transfer

## Objective

Move files between systems.

---

## Challenge

Copy file between laptop and EC2.

---

## Solution

Upload:

```bash
scp -i key.pem myfile.txt ec2-user@PUBLIC-IP:/home/ec2-user
```

Download:

```bash
scp -i key.pem ec2-user@PUBLIC-IP:/home/ec2-user/myfile.txt .
```

---

## What You Learned

- SCP
- File transfer

---

# ✅ Lab 18 - Linux Troubleshooting Challenge

## Scenario

Developer says:

> "The file exists somewhere but I don't know where."

---

## Solution

```bash
find / -name filename 2>/dev/null
```

---

# ✅ Lab 19 - Process Troubleshooting Challenge

## Scenario

Developer says:

> "The application is stuck."

---

## Solution Workflow

View processes:

```bash
ps -ef
```

Find application:

```bash
ps -ef | grep app
```

Terminate:

```bash
kill PID
```

---

# ✅ Lab 20 - EC2 Survivor Challenge

## Objective

Combine everything learned.

---

## Challenge

1. SSH into EC2
2. Create workspace
3. Create files
4. Search files
5. View contents
6. Copy files
7. Move files
8. Delete files
9. Investigate processes
10. Inspect DNS
11. Download webpage
12. Change permissions

Complete without notes.

---

# 🏆 Final Linux Mastery Questions

Without notes answer:

1. Difference between absolute and relative paths?
2. What does pwd show?
3. What does ls -l show?
4. What does grep do?
5. Difference between > and >> ?
6. What does ps -ef show?
7. What is a PID?
8. What does chmod do?
9. What does host do?
10. What problem does SCP solve?

---

# 💡 Solutionist Wisdom

A beginner learns commands.

A Linux user learns workflows.

A DevOps engineer learns troubleshooting.

A Solutionist learns that Linux is not an operating system.

Linux is an environment for solving problems.

The command is rarely the goal.

The solution is.
