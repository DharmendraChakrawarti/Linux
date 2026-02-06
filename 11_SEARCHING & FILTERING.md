

# 🐧 CHAPTER 11 — SEARCHING & FILTERING

### (grep, find, pipe `|`, wc, sort)

This chapter teaches how to **search text, find files, and filter output** — very important for Linux admins.

---

# 1. grep — Search Text Inside Files

### Meaning:

`grep` = **Global Regular Expression Print**

Simple meaning → **Search word inside file**

---

### Example:

```bash
grep root /etc/passwd
```

Finds all lines containing **root**

---

### Case-insensitive search:

```bash
grep -i linux file.txt
```

---

### Search in multiple files:

```bash
grep linux *.txt
```

---

# 2. find — Find Files & Folders

### Meaning:

Search files anywhere in system.

---

### Find file by name:

```bash
find / -name file.txt
```

---

### Find all .txt files:

```bash
find /home -name "*.txt"
```

---

# 3. Pipe `|` — Send Output to Another Command

### Meaning:

Take output of one command → give it as input to another.

---

### Example:

```bash
ps aux | grep root
```

Means:

* Show all processes
* Filter only root processes

---

# 4. wc — Count Words, Lines, Characters

### Meaning:

`wc` = **Word Count**

---

### Count lines:

```bash
wc -l file.txt
```

---

### Count words:

```bash
wc -w file.txt
```

---

### Count characters:

```bash
wc -c file.txt
```

---

# 5. sort — Sort Output

### Example:

```bash
sort file.txt
```

---

### Reverse sort:

```bash
sort -r file.txt
```

---

# 6. Combined Commands (Real Linux Power)

```bash
ps aux | grep root | wc -l
```

Meaning:
Count how many root processes running.

---

# 7. Practical Lab 🧠

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

Then:

```bash
cat names.txt
sort names.txt
wc -l names.txt
grep ram names.txt
```

---

# 8. Mini Challenge 💡

1. Find all `.conf` files in `/etc`
2. Search `root` in `/etc/passwd`
3. Count number of users

---

# 9. Important Tips ⚡

* grep + pipe = very powerful
* find helps in large systems

---
