
# 🐧 CHAPTER 10 — PROCESS MANAGEMENT

### (ps, top, kill, jobs, bg, fg)

This chapter teaches how to **see, control, and stop running programs (processes)**.

---

# 1. What is a Process?

A **process** = A **running program**

Examples:

* Chrome running
* Terminal command running
* Server service running

---

# 2. ps — Show Running Processes

### Meaning:

`ps` = **Process Status**

```bash
ps
```

Shows processes of **current terminal**

---

### Show all system processes:

```bash
ps aux
```

---

### Explanation:

* a → all users
* u → user info
* x → background processes

---

# 3. top — Live Process Monitor

```bash
top
```

Shows:

* CPU usage
* RAM usage
* Process list

Exit → `q`

---

# 4. kill — Stop Process

### Stop process using PID

```bash
kill PID
```

---

### Force stop:

```bash
kill -9 PID
```

---

### Example:

```bash
ps aux | grep firefox
kill 1234
```

---

# 5. jobs — Show Background Jobs

```bash
jobs
```

---

# 6. bg — Resume Process in Background

```bash
bg
```

---

# 7. fg — Bring Process to Foreground

```bash
fg
```

---

# 8. Run Command in Background

Add `&`

```bash
sleep 300 &
```

---

# 9. Practical Lab 🧠

```bash
sleep 200 &
jobs
fg
Ctrl + C
```

---

# 10. Mini Challenge 💡

1. Run sleep 500 in background
2. Check jobs
3. Bring to foreground
4. Stop it

---

# 11. Important Admin Tips ⚠

* Use kill carefully
* Never kill system critical processes
* Always check process before killing

---

---
