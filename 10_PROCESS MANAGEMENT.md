

# 🐧 CHAPTER 10 — PROCESS MANAGEMENT

*(ps, top, kill, jobs, bg, fg)*

---

# 🔹 What is a Process?

A **process** is simply **a running program**.

When you run any command or open any application → **a process is created**.

### Examples:

| Action              | Process        |
| ------------------- | -------------- |
| Open Chrome         | chrome process |
| Run `ls`            | ls process     |
| Start Apache server | apache process |
| Run `sleep 100`     | sleep process  |

💡 **Simple definition:**

> Program + Running state = **Process**

---

# 🔹 Why Process Management is Important?

In **real servers**, many programs run at the same time.

You must know how to:

✅ View running processes
✅ Monitor CPU & RAM usage
✅ Kill stuck programs
✅ Control background & foreground jobs

This is **critical for system admins + DevOps + Cloud engineers**

---

# 🔹 2. `ps` — Show Running Processes

### Meaning:

`ps` = **Process Status**

```bash
ps
```

Shows only **processes of your current terminal session**

Example output:

```
PID  TTY   TIME  CMD
1234 pts/0 00:00 bash
2345 pts/0 00:00 ps
```

### Important Columns:

| Column | Meaning      |
| ------ | ------------ |
| PID    | Process ID   |
| TTY    | Terminal     |
| TIME   | CPU time     |
| CMD    | Command name |

---

## 🔹 Show ALL system processes

```bash
ps aux
```

This shows **every running process on the system**.

### Meaning of flags:

| Option | Meaning              |
| ------ | -------------------- |
| a      | all users            |
| u      | user info            |
| x      | background processes |

---

### Sample Output:

```
USER   PID  %CPU  %MEM  COMMAND
root   1    0.0   0.1   systemd
root   1123 0.2   1.0   sshd
user   2345 1.2   3.4   chrome
```

---

### Real Admin Usage:

Find a running process:

```bash
ps aux | grep nginx
```

---

# 🔹 3. `top` — Live Process Monitor

```bash
top
```

This shows **real-time system usage**

---

### Displays:

* CPU usage %
* Memory usage %
* Load average
* Running processes
* Process IDs

---

### Sample Info You See:

| Metric  | Meaning      |
| ------- | ------------ |
| %CPU    | CPU usage    |
| %MEM    | RAM usage    |
| PID     | Process ID   |
| COMMAND | Program name |

---

### Useful Keys inside `top`:

| Key | Action          |
| --- | --------------- |
| q   | Quit            |
| k   | Kill process    |
| r   | Change priority |
| M   | Sort by memory  |
| P   | Sort by CPU     |

---

### Real Admin Example:

Check which process is **eating CPU**:

```bash
top
```

---

# 🔹 4. `kill` — Stop a Process

Every process has **PID (Process ID)**.

To stop a process:

```bash
kill PID
```

---

### Example:

```bash
kill 2345
```

---

## 🔹 Force Kill (Hard Kill)

```bash
kill -9 PID
```

⚠ This **forces immediate termination**

Use ONLY when normal kill doesn’t work.

---

### Real World Example:

```bash
ps aux | grep chrome
kill 4567
```

---

### Kill by process name:

```bash
pkill firefox
```

or

```bash
killall firefox
```

---

# 🔹 5. jobs — Show Background Jobs

Shows **processes running in background from your terminal**

```bash
jobs
```

---

### Example:

```bash
sleep 200 &
jobs
```

Output:

```
[1]+ Running sleep 200 &
```

---

# 🔹 6. bg — Resume in Background

If a process is **stopped**, resume it in background.

```bash
bg
```

or

```bash
bg %1
```

---

# 🔹 7. fg — Bring to Foreground

Bring a background process to terminal:

```bash
fg
```

or

```bash
fg %1
```

---

# 🔹 8. Run Command in Background

Add **&** at end:

```bash
sleep 300 &
```

This runs command in background.

---

# 🔹 9. Practical LAB 🧠 (Must Practice)

### Step 1 — Start process

```bash
sleep 200 &
```

---

### Step 2 — Check jobs

```bash
jobs
```

---

### Step 3 — Bring to foreground

```bash
fg
```

---

### Step 4 — Stop it

Press:

```bash
Ctrl + C
```

---

# 🔹 10. Mini Challenge 💡 (Your Practice)

Try this:

```bash
sleep 500 &
jobs
fg
Ctrl + C
```

---

# 🔹 11. Very Important Admin Tips ⚠

### 🚨 Never Kill These (System Critical):

| Process        | Why                     |
| -------------- | ----------------------- |
| systemd        | System controller       |
| init           | Parent of all processes |
| sshd           | SSH connection          |
| kernel threads | System crash risk       |

---

### Safe Practice:

✔ Always verify process
✔ Use `ps aux | grep name`
✔ Use normal kill first
✔ Use kill -9 only if required

---

# 🔹 BONUS: Advanced Useful Commands

### Kill process using PORT:

```bash
sudo lsof -i :8080
kill PID
```

---

### Interactive Process Manager (Best Tool):

```bash
htop
```

(Install using: `sudo apt install htop`)

---

# 🔥 Interview Questions (Very Important)

### Q1: Difference between ps and top?

| ps              | top               |
| --------------- | ----------------- |
| Static snapshot | Live monitoring   |
| One-time output | Continuous update |

---

### Q2: Difference between kill and kill -9?

| kill           | kill -9    |
| -------------- | ---------- |
| Graceful stop  | Force stop |
| Allows cleanup | No cleanup |

---

### Q3: What is PID?

> PID = Process ID = Unique number for each running process

---

# 🎯 You have now MASTERED:

✔ Linux Process management
✔ ps
✔ top
✔ kill
✔ jobs
✔ bg
✔ fg

---
