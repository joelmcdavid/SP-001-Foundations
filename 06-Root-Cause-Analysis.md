# 🔍 Root Cause Analysis

---

# 🚨 Scenario

A website goes down.

Bad engineers say:

```text
Restart Everything
```

Good engineers ask:

- Is DNS working?
- Is networking working?
- Is the server healthy?
- Is the application healthy?
- Is the database healthy?

---

# ✅ Solutionist Approach

1. Observe
2. Investigate
3. Gather Evidence
4. Identify Cause
5. Fix Problem
6. Prevent Recurrence

---

# 💡 Golden Rule

Never assume.

Always verify.

## Why Should You Care?

Many people fix symptoms.

Engineers solve underlying causes.

---

## Simple Explanation

Root Cause Analysis (RCA) identifies the true reason a problem occurred.

---

## Real World Analogy

Imagine a leaking ceiling.

Bad Fix:

```text
Paint Over Leak
```

Good Fix:

```text
Find Source
Repair Roof
Stop Future Leaks
```

---

## The Five Whys

Example:

Website Down

Why?

Server Crashed.

Why?

Disk Full.

Why?

Logs Filled Disk.

Why?

Log Rotation Missing.

Why?

Nobody Configured It.

Root Cause Found.

---

## Production Example

```text
Problem
   ↓
Evidence
   ↓
Investigation
   ↓
Root Cause
   ↓
Permanent Fix
```

---

## Key Takeaways

✅ Symptoms are not causes.

✅ Evidence drives investigation.

✅ Root causes prevent recurrence.

✅ RCA improves long-term reliability.

---

## 🧠 Solutionist Thinking

Never stop at the first answer.

Keep asking:

Why?

Why?

Why?

Until the true cause is revealed.


# 🔎 Root Cause Analysis

## 🚨 SSH Timeout Investigation

Problem:

```text
SSH Timed Out
```

Most beginners think:

```text
SSH is broken.
```

Not necessarily.

A timeout is a symptom.

---

## ✅ Root Cause Checklist

```text
No Public IP

Wrong Security Group

Missing Internet Gateway

Wrong Route Table

Bad Subnet

Wrong Key Pair

SSH Service Not Running

Incorrect IP Address
```

---

## ⚡ Real Example #1

Instance launched without a Public IP.

Instance received:

```text
172.31.x.x
```

Private IP only.

Result:

```text
SSH Timeout
```

Root Cause:

```text
No Public IP
```

---

## ⚡ Real Example #2

VPC networking issue.

Missing subnet or incorrect routing.

Result:

```text
SSH Timeout
```

Root Cause:

```text
Network Configuration
```

---

## 🎯 Lesson Learned

The same symptom can be caused by many different problems.

```text
SSH Timeout ≠ SSH Problem
```

It may actually be:

```text
Network Problem

Security Group Problem

Routing Problem

Public IP Problem
```

---

## 🧠 Solutionist Wisdom

Never troubleshoot the symptom.

Trace the path.

```text
Laptop
 ↓
Internet
 ↓
Public IP
 ↓
Internet Gateway
 ↓
Route Table
 ↓
Subnet
 ↓
Security Group
 ↓
EC2
 ↓
SSH Service
```

Find the broken layer.
