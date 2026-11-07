# 🌐 What Is Networking?

## Why Should You Care?

Without networking modern technology would not exist.

Networking allows systems to communicate.

---

## Simple Explanation

Networking is the way devices exchange data.

Examples:

- Computers
- Servers
- Phones
- Routers



## 🎯 Learning Objectives

- Understand how computers communicate
- Understand IP addresses
- Understand DNS
- Understand connectivity

---

# 📞 IP Address

An IP Address is like a phone number for a computer.

Example:

```text
54.123.45.67
```

Computers use IP addresses to communicate.

---

# 🗺️ DNS

DNS translates names into IP addresses.

Example:

```text
google.com
      ↓
IP Address
```

Without DNS we would need to remember IP addresses.

---

# 🍔 Restaurant Analogy

A DNS server is like a receptionist.

The receptionist knows where everything is and directs customers correctly.

---

# 💡 Solutionist Wisdom

Most network issues involve:

- DNS
- Connectivity
- Routing

Always verify before making assumptions.

---

## Real World Analogy

Think of networking like roads.

```text
Roads
      ↓
Vehicles Travel

Network
      ↓
Data Travels
```

No roads means no deliveries.

No network means no communication.

---

## Production Example

```text
Laptop
   ↓
Router
   ↓
Internet
   ↓
AWS Server
   ↓
Website
```

Every request follows a path.

---

## Key Takeaways

✅ Networks connect devices.

✅ Data travels through networks.

✅ Most outages involve networking somewhere.

✅ Networking is a core engineering skill.

---

## 🧠 Solutionist Thinking

Ask yourself:

- How does data travel?
- What happens if DNS fails?
- What happens if routing fails?




# 🌐 What Is Networking?

## 🚪 Ports Explained

Think of a server as a building.

```text
IP Address = Building

Port = Door
```

Examples:

```text
22    SSH

80    HTTP

443   HTTPS

8080  Development Web Apps

3306  MySQL

6379  Redis
```

### Visual

```text
Server

 ├── Door 22   → SSH
 ├── Door 80   → HTTP
 ├── Door 443  → HTTPS
 └── Door 3306 → MySQL
```

---

## 🏓 Ping

Used to answer:

```text
Can I reach the server?
```

Example:

```bash
ping google.com
```

Stop:

```text
CTRL + C
```

Think:

```text
"Hello, can you hear me?"
```

---

## 📖 DNS

DNS is the internet's phonebook.

Instead of remembering:

```text
142.250.x.x
```

you remember:

```text
google.com
```

DNS performs the translation.

### Quick Lookup

```bash
host google.com
```

### Deep Investigation

```bash
dig google.com
```

### Memory Hack

```text
host = Quick Answer

dig = Full Investigation
```

---

## 🚪 Telnet

Tests whether a port is reachable.

Example:

```bash
telnet SERVER_IP 22
```

Question:

```text
Can I reach SSH?
```

Results:

```text
Connects = Port Open

Fails = Port Closed
        Firewall
        Security Group
        Service Down
```

---

## 📡 Netstat and SS

Used to see:

- Open ports
- Listening services
- Active connections

Legacy:

```bash
netstat -tunlp
```

Modern:

```bash
ss -tunlp
```

Think:

```text
Which doors are currently open?
```
