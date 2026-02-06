

# 🐧 CHAPTER 19 — LOG FILES & TROUBLESHOOTING (Beginner Friendly)

Logs are **the MOST IMPORTANT thing for Linux Admin & DevOps engineers**.

If something breaks → **FIRST CHECK LOGS**.

---

# 1. What are Log Files?

Log files are **text files that store system activity, errors, warnings, and service events**.

They help in:

* Debugging problems
* Monitoring system health
* Security auditing
* Finding crash reasons

---

# 2. Log File Location in Linux

All major logs are inside:

```bash
/var/log
```

Check:

```bash
ls /var/log
```

---

# 3. Important Linux Log Files (Must Know)

| File              | Purpose                |
| ----------------- | ---------------------- |
| /var/log/syslog   | Main system logs       |
| /var/log/auth.log | Login & authentication |
| /var/log/kern.log | Kernel logs            |
| /var/log/dpkg.log | Package install logs   |
| /var/log/boot.log | Boot logs              |
| /var/log/messages | System messages (RHEL) |

---

# 4. View Log Files Safely

### Use `less`

```bash
less /var/log/syslog
```

Keys:

* Scroll → Arrow keys
* Search → `/error`
* Quit → `q`

---

### Real-time Log Monitoring (VERY IMPORTANT)

```bash
tail -f /var/log/syslog
```

Meaning:

* Shows logs **live**

Stop → `Ctrl + C`

---

# 5. journalctl (Systemd Logs)

Modern Linux uses **systemd → journal logs**

View all logs:

```bash
journalctl
```

---

### View latest logs

```bash
journalctl -xe
```

---

### Logs for specific service

```bash
journalctl -u ssh
```

---

# 6. Log Filtering using grep

Find errors:

```bash
grep -i error /var/log/syslog
```

---

Find failed login:

```bash
grep "Failed password" /var/log/auth.log
```

---

# 7. Log Rotation (Important Concept)

Linux automatically **rotates logs** using:

```
logrotate
```

Meaning:

* Old logs compressed
* New logs created
* Prevents disk full

Check:

```bash
ls /var/log/*.gz
```

---

# 8. Real Troubleshooting Examples

---

### SSH Login Failure Debug

```bash
sudo tail -f /var/log/auth.log
```

Try login → check error message.

---

### Service Crash Debug

```bash
journalctl -u nginx
```

---

# 🧪 PRACTICE TASKS — LOGS

Run:

```bash
ls /var/log
less /var/log/syslog
tail -f /var/log/syslog
```

---

# 🧠 Admin Level Practice

1️⃣ Monitor live ssh logs
2️⃣ Find failed login attempts
3️⃣ Track service crash

---
