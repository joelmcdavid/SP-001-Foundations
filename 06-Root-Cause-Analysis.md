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
