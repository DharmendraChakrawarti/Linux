

# 🐧 CHAPTER 4 — BASIC NAVIGATION COMMANDS

### (pwd, ls, cd)

These are the **MOST IMPORTANT beginner commands**.
You will use them **every day** in Linux.

---

# 1. pwd — Where am I?

### Meaning:

`pwd` = **Print Working Directory**

It shows **your current location (folder)**.

---

### Command:

```bash
pwd
```

### Example Output:

```
/home/dharmendra
```

### Meaning:

You are inside:

```
/home/dharmendra
```

---

### Simple Example:

If you are in:

```
C:\Users\Name\Documents
```

Linux equivalent:

```
/home/name/Documents
```

---

# 2. ls — List Files & Folders

### Meaning:

`ls` = **List**

Shows **files & folders inside current directory**.

---

### Basic:

```bash
ls
```

---

### Long format:

```bash
ls -l
```

Shows:

* permissions
* owner
* size
* date

---

### Hidden files:

```bash
ls -a
```

---

### Human readable size:

```bash
ls -lh
```

---

### Example:

```bash
ls /etc
```

Lists everything inside `/etc`

---

# 3. cd — Change Directory

### Meaning:

Move from **one folder to another**.

---

### Basic:

```bash
cd foldername
```

---

### Go inside /etc:

```bash
cd /etc
```

---

### Go back one folder:

```bash
cd ..
```

---

### Go home:

```bash
cd ~
```

or simply:

```bash
cd
```

---

# 4. Special Symbols Explained

| Symbol | Meaning        |
| ------ | -------------- |
| /      | Root           |
| ~      | Home folder    |
| .      | Current folder |
| ..     | Parent folder  |

---

### Example:

```bash
cd ..
```

Move one folder back.

---

# 5. Practical Navigation Examples

### Step 1:

```bash
pwd
```

### Step 2:

```bash
ls
```

### Step 3:

```bash
cd /etc
```

### Step 4:

```bash
pwd
```

### Step 5:

```bash
cd ..
```

### Step 6:

```bash
cd ~
```

---

# 6. Absolute vs Relative Path (Simple)

---

### Absolute Path (Full Address):

```bash
cd /home/dharmendra/Documents
```

Starts from `/`

---

### Relative Path (From current folder):

```bash
cd Documents
```

---

# 7. Real-Life Example

If you are here:

```
/home/user
```

And folder is:

```
/home/user/linux/practice
```

Then:

### Absolute:

```bash
cd /home/user/linux/practice
```

### Relative:

```bash
cd linux/practice
```

---

# 8. Your Practice Tasks 🧠

Try each command slowly:

```bash
pwd
ls
cd /
pwd
ls
cd /home
ls
cd ~
pwd
```

---

# 9. Mini Challenge 💡

1. Go to root folder `/`
2. List all folders
3. Go to `/var`
4. List its contents
5. Return to home

---

# 10. Very Important Tips ⚠

* Linux is **case sensitive**

```
Test  ≠  test
```

* Space matters:

```
my file.txt ❌
"my file.txt" ✅
```

---
