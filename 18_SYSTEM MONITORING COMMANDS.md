
# 🐧 CHAPTER 18 — SYSTEM MONITORING COMMANDS (Beginner Friendly)

System monitoring means **checking health, performance, and resource usage of Linux system**.

This is **VERY IMPORTANT** for:

* Linux Admin
* DevOps Engineer
* Cloud Engineer

---

# 1. Why System Monitoring?

To check:

* CPU usage
* RAM usage
* Disk usage
* System load
* Running processes
* System uptime

---

# 2. uptime — System Running Time

```bash
uptime
```

### Output example:

```
10:30:25 up 3 days, 5:20,  2 users,  load average: 0.05, 0.10, 0.15
```

### Meaning:

| Field     | Meaning             |
| --------- | ------------------- |
| up 3 days | system running time |
| 2 users   | logged in users     |
| load avg  | CPU load            |

---

# 3. top — Live Process Monitor

```bash
top
```

### Shows:

* CPU usage
* RAM usage
* Running processes

Press:

* `q` → quit
* `k` → kill process
* `P` → sort by CPU
* `M` → sort by Memory

---

# 4. htop — Advanced Monitor (Better than top)

Install first:

```bash
sudo apt install htop -y
```

Run:

```bash
htop
```

### Features:

* Colorful UI
* Mouse support
* Easy process kill

Exit → `F10`

---

# 5. free — Memory Usage

```bash
free -h
```

### Output:

```
              total   used   free
Mem:           2.0G   900M   1.1G
```

`-h` → human readable

---

# 6. df — Disk Usage (Filesystem)

```bash
df -h
```

### Shows:

* Disk size
* Used space
* Free space

---

# 7. du — Folder Size

```bash
du -sh /var/log
```

### Meaning:

* Shows total folder size

---

# 8. vmstat — System Performance

```bash
vmstat 2 5
```

Meaning:

* Refresh every 2 seconds
* 5 times

---

# 9. iostat — Disk I/O (Advanced)

Install:

```bash
sudo apt install sysstat -y
```

Run:

```bash
iostat
```

---

# 10. watch — Continuous Monitoring

```bash
watch free -h
```

Shows RAM live every 2 sec.

---

# 🧪 PRACTICE TASKS — SYSTEM MONITORING

Try all:

```bash
uptime
top
free -h
df -h
du -sh /var/log
```

---

# 🧠 Admin Level Practice

1️⃣ Find which process uses most CPU
2️⃣ Find biggest folder in `/var`

---
