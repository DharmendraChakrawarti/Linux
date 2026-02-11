

# 🐧 CHAPTER 11 — SEARCHING & FILTERING (MASTER GUIDE)

> Tools covered:
> **grep | find | pipe (|) | wc | sort**

These are **core Linux commands** used **daily by System Admins, DevOps Engineers, Cloud Engineers, and SREs**.

---

# 🔹 Why This Chapter Is EXTREMELY Important?

In real servers, you will:

* Search **error logs**
* Find **config files**
* Filter **process lists**
* Count **users, requests, errors**
* Sort **logs, reports, outputs**

👉 These commands = **Linux Superpower**

---

# 1️⃣ grep — Search Text Inside Files

### Meaning:

`grep` = **Global Regular Expression Print**

Simple meaning:

> 🔍 **Search a word / pattern inside text or files**

---

## 🔹 Basic Syntax:

```bash
grep "word" filename
```

---

## 🔹 Example 1:

```bash
grep root /etc/passwd
```

Meaning:

* Search **root** inside `/etc/passwd`
* Show matching lines only

Output:

```
root:x:0:0:root:/root:/bin/bash
```

---

## 🔹 Example 2 — Case Insensitive Search

```bash
grep -i linux file.txt
```

Finds:

```
Linux
LINUX
linux
```

---

## 🔹 Example 3 — Search in Multiple Files

```bash
grep error *.log
```

Meaning:

Search **error** in all `.log` files.

---

## 🔹 Example 4 — Recursive Search (VERY IMPORTANT 🔥)

```bash
grep -r "password" /etc/
```

Searches **password inside all files of /etc**

👉 Used in **security audits**

---

## 🔹 Example 5 — Show Line Numbers

```bash
grep -n root /etc/passwd
```

Output:

```
1:root:x:0:0:root:/root:/bin/bash
```

---

## 🔹 Example 6 — Count Matches

```bash
grep -c root /etc/passwd
```

Output:

```
1
```

---

## 🔹 Real Admin Use Case:

```bash
grep -i error /var/log/syslog
```

Find system errors 🔥

---

# 2️⃣ find — Find Files & Directories

### Meaning:

> 🔎 Search **files & folders anywhere in system**

---

## 🔹 Basic Syntax:

```bash
find path condition
```

---

## 🔹 Example 1 — Find file by name:

```bash
find / -name file.txt
```

Search **entire system** for file.txt

⚠️ Slow (entire disk scan)

---

## 🔹 Example 2 — Find inside home only:

```bash
find /home -name file.txt
```

---

## 🔹 Example 3 — Find all `.txt` files:

```bash
find /home -name "*.txt"
```

---

## 🔹 Example 4 — Find directories only:

```bash
find /etc -type d
```

---

## 🔹 Example 5 — Find files only:

```bash
find /etc -type f
```

---

## 🔹 Example 6 — Find by size (🔥 ADMIN LEVEL)

```bash
find / -size +100M
```

Find files **larger than 100MB**

---

## 🔹 Example 7 — Find & Delete (DANGEROUS ⚠️)

```bash
find /tmp -name "*.log" -delete
```

Deletes all `.log` files from `/tmp`

---

# 3️⃣ Pipe `|` — Command Chaining (LINUX MAGIC 🔥)

### Meaning:

> Take **output of first command → send as input to second**

---

## 🔹 Example 1:

```bash
ps aux | grep root
```

Meaning:

* `ps aux` → show all processes
* `grep root` → filter only root processes

---

## 🔹 Example 2:

```bash
ls -l | wc -l
```

Count number of files in directory.

---

## 🔹 Example 3:

```bash
history | grep docker
```

Show only docker-related commands you ran.

---

# 4️⃣ wc — Count Lines, Words, Characters

### Meaning:

`wc` = **Word Count**

---

## 🔹 Example 1 — Count lines:

```bash
wc -l file.txt
```

---

## 🔹 Example 2 — Count words:

```bash
wc -w file.txt
```

---

## 🔹 Example 3 — Count characters:

```bash
wc -c file.txt
```

---

## 🔹 Real Admin Example:

```bash
grep root /etc/passwd | wc -l
```

Count number of root users.

---

# 5️⃣ sort — Sort Output Alphabetically / Numerically

---

## 🔹 Example 1:

```bash
sort names.txt
```

---

## 🔹 Example 2 — Reverse:

```bash
sort -r names.txt
```

---

## 🔹 Example 3 — Numeric sort:

```bash
sort -n numbers.txt
```

---

## 🔹 Example 4 — Unique values:

```bash
sort names.txt | uniq
```

---

# 6️⃣ Combined Commands — Real Linux Power 💪

```bash
ps aux | grep root | wc -l
```

Meaning:

1. Show all processes
2. Filter root processes
3. Count them

---

## 🔹 Another Example:

```bash
find /var/log -name "*.log" | wc -l
```

Count total log files.

---

# 7️⃣ Practical Lab (DO THIS 💻)

---

### Step 1:

```bash
nano names.txt
```

Write:

```
ram
shyam
amit
vijay
```

Save → CTRL+O → Enter → CTRL+X

---

### Step 2 — Display:

```bash
cat names.txt
```

---

### Step 3 — Sort:

```bash
sort names.txt
```

---

### Step 4 — Count lines:

```bash
wc -l names.txt
```

---

### Step 5 — Search:

```bash
grep ram names.txt
```

---

# 8️⃣ Mini Challenge — SOLUTIONS ✅

---

### 1️⃣ Find all `.conf` files in `/etc`

```bash
find /etc -name "*.conf"
```

---

### 2️⃣ Search root in passwd

```bash
grep root /etc/passwd
```

---

### 3️⃣ Count number of users

```bash
wc -l /etc/passwd
```

---

# 9️⃣ Pro Linux Tricks 🔥

---

### 🔹 Top 10 largest files:

```bash
find / -type f -exec du -h {} + | sort -rh | head -10
```

---

### 🔹 Most used commands:

```bash
history | awk '{print $2}' | sort | uniq -c | sort -nr | head
```

---

# 🔟 Interview Questions (VERY IMPORTANT ❗)

---

### Q1: Difference between `grep` and `find`?

| grep                    | find                        |
| ----------------------- | --------------------------- |
| Search **inside files** | Search **files themselves** |

---

### Q2: What does pipe `|` do?

👉 Passes output of one command to another.

---

### Q3: How to count lines containing error in log?

```bash
grep -i error app.log | wc -l
```

---
