
# 🐧 CHAPTER 20 — CRON JOBS & TASK SCHEDULING (Beginner Friendly)

Cron jobs are used to **automate tasks** in Linux.

Examples:

* Daily backup
* Log cleanup
* System updates
* Server monitoring
* Automation scripts

---

# 1. What is Cron?

**Cron** is a Linux service that **runs commands automatically at scheduled times**.

Think like:

> Alarm clock for Linux commands ⏰

---

# 2. What is Crontab?

`crontab` = **cron table**
Where scheduled jobs are stored.

Check your cron jobs:

```bash
crontab -l
```

Edit cron jobs:

```bash
crontab -e
```

---

# 3. Cron Job Time Format (VERY IMPORTANT)

```
*  *  *  *  *
|  |  |  |  |
|  |  |  |  +---- Day of week (0 - 7) [Sunday = 0 or 7]
|  |  |  +------- Month (1 - 12)
|  |  +---------- Day of month (1 - 31)
|  +------------- Hour (0 - 23)
+---------------- Minute (0 - 59)
```

---

# 4. Simple Cron Job Examples

---

### Run every minute

```bash
* * * * * echo "Hello Linux" >> /tmp/test.txt
```

---

### Run daily at 2 AM

```bash
0 2 * * * /home/user/backup.sh
```

---

### Run every Sunday at 5 PM

```bash
0 17 * * 0 /home/user/cleanup.sh
```

---

# 5. Create Your First Cron Job (Hands-on)

Open editor:

```bash
crontab -e
```

Add:

```bash
* * * * * date >> /tmp/time.txt
```

Save and exit.

Wait 2 minutes.

Check:

```bash
cat /tmp/time.txt
```

---

# 6. Special Time Shortcuts

| Shortcut | Meaning        |
| -------- | -------------- |
| @reboot  | Run at startup |
| @daily   | Once daily     |
| @hourly  | Every hour     |
| @weekly  | Once weekly    |

---

### Example:

```bash
@reboot echo "System Started" >> /tmp/boot.log
```

---

# 7. System Wide Cron Jobs

Location:

```bash
/etc/crontab
/etc/cron.hourly/
/etc/cron.daily/
/etc/cron.weekly/
/etc/cron.monthly/
```

---

# 8. Real DevOps Cron Use Cases 🔥

* Nightly backup
* Disk cleanup
* Auto SSL renewal
* Log rotation
* Health monitoring

---

# 🧪 PRACTICE TASKS — CRON

1️⃣ Create cron → write time every minute
2️⃣ Schedule reboot message
3️⃣ Create daily cron job

---

# 🧠 Admin Level Practice

1️⃣ Schedule disk cleanup
2️⃣ Schedule backup script
3️⃣ Monitor cron logs

Check cron logs:

```bash
grep CRON /var/log/syslog
```

---
