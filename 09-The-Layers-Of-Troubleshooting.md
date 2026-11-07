# 🏗️ The Layers Of Troubleshooting

When a service fails, investigate in layers.

---

Layer 1

```text
DNS
```

Layer 2

```text
Network
```

Layer 3

```text
Server
```

Layer 4

```text
Application
```

Layer 5

```text
Database
```

---

# 💡 Solutionist Wisdom

Follow a method.

Do not guess.

## Why Should You Care?

Most troubleshooting failures happen because engineers investigate the wrong thing first.

Problems exist in layers.

Understanding those layers saves time.

---

## Simple Explanation

Systems are built in levels.

Each level depends on the one beneath it.

When something fails, start at the bottom.

---

## Layer 1 - Physical

```text
Power
Hardware
Cable
Device
```

---

## Layer 2 - Network

```text
IP Address
DNS
Routing
Firewall
```

---

## Layer 3 - Operating System

```text
Linux
Windows
Permissions
Services
Processes
```

---

## Layer 4 - Application

```text
Nginx
Apache
Docker
NodeJS
Python
Database
```

---

## Layer 5 - Business

```text
Customer Impact
Revenue Impact
Service Impact
```

---

## Production Example

Website not loading.

Wrong approach:

```text
Check Application First
```

Better approach:

```text
Power
   ↓
Network
   ↓
Operating System
   ↓
Application
   ↓
Business Impact
```

---

## Key Takeaways

✅ Problems exist in layers.

✅ Lower layers affect higher layers.

✅ Never skip troubleshooting levels.

✅ Follow a consistent process.

---

## 🧠 Solutionist Thinking

Before investigating ask:

"What layer am I currently working in?"

Always work methodically.



# 🛠️ The Layers Of Troubleshooting

## 🧠 Memory Investigation

### free

Purpose:

```text
Check RAM usage.
```

Command:

```bash
free -h
```

Think:

```text
How much desk space is left?
```

---

## 💾 Disk Investigation

### df

Purpose:

```text
Check free disk space.
```

Command:

```bash
df -h
```

Think:

```text
How full is the warehouse?
```

---

### du

Purpose:

```text
Find what is consuming space.
```

Examples:

```bash
du -sh /var/log

du -h --max-depth=1
```

Think:

```text
Which boxes are taking warehouse space?
```

---

## ⚙️ Process Investigation

### top

Linux Task Manager.

```bash
top
```

Useful Keys:

```text
P = CPU Sort

M = Memory Sort

q = Exit
```

Think:

```text
Live CCTV for the server.
```

---

### ps

Process snapshot.

```bash
ps aux

ps -ef
```

Find process:

```bash
ps -ef | grep nginx
```

Think:

```text
Photograph of running processes.
```

---

## 🔪 Process Termination

Normal stop:

```bash
kill PID
```

Force stop:

```bash
kill -9 PID
```

Kill by name:

```bash
pkill nginx

killall nginx
```

Think:

```text
Linux End Task
```

---

## 📜 Linux Logs

Linux's black box recorder:

```text
/var/log
```

Important logs:

```text
/var/log/syslog

/var/log/auth.log

/var/log/cloud-init.log

/var/log/messages
```

---

### View Logs

```bash
cat file
less file
tail -f file
```

---

### Search Logs

```bash
grep error file

grep denied file

grep -Ei "error|fail|denied" file
```

Example:

```bash
sudo cat /var/log/cloud-init.log | grep error
```

Meaning:

```text
Show startup errors.
```

---

## 🔐 SSH

Remote login.

```bash
ssh -i key.pem ec2-user@IP
```

Visual:

```text
Laptop
   │
   ▼
SSH Tunnel
   │
   ▼
EC2 Server
```

Think:

```text
Remote Control
```

---

## 📦 SCP

Secure file transfer.

Upload:

```bash
scp file.txt ec2-user@server:/home/ec2-user
```

Download:

```bash
scp ec2-user@server:file.txt .
```

Think:

```text
Secure Drag & Drop
```

---

## 🚀 Solutionist Troubleshooting Flow

```text
Server Slow?

→ top
→ free -h

Disk Full?

→ df -h
→ du -sh

Service Down?

→ systemctl status
→ ps -ef

Website Not Working?

→ curl
→ ss -tunlp

DNS Issue?

→ host
→ dig

Connectivity Issue?

→ ping
→ telnet

Application Error?

→ grep
→ tail -f
→ journalctl
```

---

## 🧠 Biggest Lesson Learned Today

```text
A valid command can fail if you're standing in the wrong environment.

Always identify:

Machine
OS
Network
Service
Process

BEFORE troubleshooting.
```
