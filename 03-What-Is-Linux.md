# 🐧 What Is Linux?

> [!IMPORTANT]
> Linux is the most common operating system used in cloud and DevOps environments.

---

## 🎯 Learning Objectives

- What Linux is
- Why Linux is popular
- Linux vs Windows
- Why DevOps engineers use Linux

---

# 🖥️ What Is An Operating System?

An Operating System (OS) manages:

- Hardware
- Memory
- Storage
- Applications

Examples:

- Windows
- Linux
- macOS

---

# 🏆 Why Linux Is Popular

✅ Open Source

✅ Free

✅ Flexible

✅ High Performance

✅ Community Support

✅ Cloud Friendly

---

# 🍔 Restaurant Analogy

## Windows

Like renting a fully furnished restaurant.

Everything is ready.

Less flexibility.

---

## Linux

Like renting an empty restaurant building.

You customise everything.

More work.

More flexibility.

---

# 🚀 Why DevOps Engineers Use Linux

Most cloud infrastructure runs Linux.

Examples:

- EC2
- Containers
- Kubernetes
- Web Servers
- Databases

---

# 💡 Solutionist Wisdom

The best engineers understand systems, not operating systems.

Linux is simply one of the most powerful tools available.








# 🐧 What Is Linux?

## 🖥️ Terminal vs Linux

Many beginners believe the terminal and Linux are the same thing.

They are not.

A terminal is simply a window used to send commands.

Examples:

- PowerShell
- Git Bash
- MobaXterm
- Windows Terminal

Linux is the operating system that processes those commands.

## 🎨 Visual

```text
PowerShell
    │
    ▼
 Windows

Git Bash
    │
    ▼
 Windows + Linux-like tools

Ubuntu EC2
    │
    ▼
 Real Linux
```

---

## 🌎 Environment Awareness

### 🟨 Linux-Like Environments

```text
Git Bash
MobaXterm Local
PowerShell
```

✅ Some Linux commands

❌ Not Linux

❌ No Linux kernel

❌ No Linux services

---

### 🟩 Real Linux Environments

```text
Ubuntu VM
Amazon Linux EC2
Debian VM
Rocky Linux
WSL
```

✅ Real Linux kernel

✅ Linux services

✅ Linux logs

✅ Linux networking

✅ Linux processes

---

## 🤔 Why Some Commands Didn't Work

These worked locally:

```bash
pwd
ls
cd
mkdir
touch
cat
grep
find
```

Because Git Bash includes Linux-style tools.

These typically require real Linux:

```bash
systemctl
journalctl
top
free
ps
df
du
ss
netstat
dmesg
```

They rely on:

- Linux kernel
- Linux memory
- Linux services
- Linux logs
- Linux process management

---

## 🧠 Environment Checks

Before troubleshooting:

```bash
uname -a
cat /etc/os-release
which command-name
```

Ask:

```text
What machine am I on?
What OS am I running?
Is the package installed?
Does this command need real Linux?
```

---

## 💡 Solutionist Wisdom

```text
Terminal ≠ Linux

Git Bash ≠ Linux

PowerShell ≠ Linux

MobaXterm ≠ Linux

Ubuntu VM = Linux

Amazon Linux EC2 = Linux
```

Instead of asking:

"Why doesn't this command work?"

Ask:

"What environment am I standing in?"
