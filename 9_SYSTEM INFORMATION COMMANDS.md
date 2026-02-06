

# 🐧 CHAPTER 9 — SYSTEM INFORMATION COMMANDS

### (uname, df, free, uptime, top, htop, lsblk)

This chapter teaches how to **check system health, hardware info, and performance**.

---

# 1. uname — System Information

### Meaning:

Shows **Linux kernel & system info**

```bash
uname -a
```

### Example Output:

```
Linux cloudshell 5.15.0 x86_64 GNU/Linux
```

Meaning:

* OS name
* Kernel version
* Architecture

---

# 2. df — Disk Space Usage

### Meaning:

Shows **disk usage**

```bash
df -h
```

`-h` → Human readable

---

### Example:

```
Filesystem   Size  Used  Avail
/dev/sda1     20G   5G    15G
```

Meaning:

* Total disk → 20GB
* Used → 5GB
* Free → 15GB

---

# 3. free — RAM Usage

### Meaning:

Shows **memory usage**

```bash
free -h
```

---

### Example:

```
total   used   free
2Gi     500M   1.5Gi
```

---

# 4. uptime — System Running Time

```bash
uptime
```

Shows:

* How long system is ON
* Load average

---

# 5. top — Live Process Monitor

```bash
top
```

Shows:

* CPU usage
* RAM usage
* Running processes

Exit → `q`

---

# 6. htop — Better top (Optional)

Install:

```bash
sudo apt install htop
```

Run:

```bash
htop
```

Exit → `q`

---

# 7. lsblk — Disk Structure

```bash
lsblk
```

Shows:

* Disk partitions
* Storage devices

---

# 8. Practical Lab 🧠

Run one by one:

```bash
uname -a
df -h
free -h
uptime
top
```

---

# 9. Mini Challenge 💡

1. Check disk usage
2. Check RAM usage
3. Find uptime
4. Run top and observe CPU

---

# 10. Important Admin Tips ⚠

* Monitor disk space regularly
* Low disk = server crash risk
* High CPU = performance issue

---
