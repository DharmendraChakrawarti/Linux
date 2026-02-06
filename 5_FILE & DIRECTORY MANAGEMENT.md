

# 🐧 CHAPTER 5 — FILE & DIRECTORY MANAGEMENT

### (mkdir, touch, cp, mv, rm)

These commands help you **create, copy, move, rename, and delete files & folders**.

---

# 1. mkdir — Create Folder

### Meaning:

`mkdir` = **Make Directory (create folder)**

---

### Create one folder:

```bash
mkdir test
```

---

### Create multiple folders:

```bash
mkdir folder1 folder2 folder3
```

---

### Create nested folders:

```bash
mkdir -p linux/practice/day1
```

Creates:

```
linux → practice → day1
```

---

# 2. touch — Create Empty File

### Meaning:

Creates a **new empty file**

---

### Example:

```bash
touch file1.txt
```

---

### Create multiple files:

```bash
touch a.txt b.txt c.txt
```

---

# 3. cp — Copy Files & Folders

### Meaning:

Make **duplicate copy**

---

### Copy file:

```bash
cp file1.txt file2.txt
```

---

### Copy file to folder:

```bash
cp file1.txt /tmp
```

---

### Copy folder:

```bash
cp -r folder1 folder2
```

(`-r` means recursive → copy all inside)

---

# 4. mv — Move & Rename

### Rename file:

```bash
mv old.txt new.txt
```

---

### Move file:

```bash
mv file.txt /tmp
```

---

### Move folder:

```bash
mv test /home/user/
```

---

# 5. rm — Delete Files & Folders ⚠

### Delete file:

```bash
rm file.txt
```

---

### Delete folder:

```bash
rm -r folder
```

---

### Force delete:

```bash
rm -rf folder
```

⚠ **VERY DANGEROUS — No recovery**

---

# 6. Safe Delete Practice

Always verify before deleting:

```bash
ls
rm file.txt
```

---

# 7. Complete Practice Lab 🧠

Run these commands one by one:

```bash
mkdir linux
cd linux
mkdir day1
cd day1
touch a.txt b.txt c.txt
ls
cp a.txt copy_a.txt
mv b.txt file2.txt
rm c.txt
ls
cd ~
```

---

# 8. Mini Challenge 💡

Create this structure:

```
/home/yourname/practice/linux/day1
```

Inside day1:

* Create 3 files
* Copy 1 file
* Rename 1 file
* Delete 1 file

---

# 9. Important Tips ⚡

* Linux is **case sensitive**
* Always double-check before `rm -rf`
* Use `ls` before delete

---
