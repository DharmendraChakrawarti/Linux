
# 🐧 CHAPTER 15 — ARCHIVES & COMPRESSION

### (tar, zip, unzip, gzip)

This chapter teaches how to **compress, archive, and extract files** (very important for backups).

---

# 1. What is Archive & Compression?

* **Archive** → Combine many files into one
* **Compression** → Reduce file size

---

### Example:

Many files → `backup.tar.gz`

---

# 2. tar — Archive Files

---

### Create archive:

```bash
tar -cvf backup.tar folder
```

Meaning:

* c → create
* v → show progress
* f → file

---

### Extract archive:

```bash
tar -xvf backup.tar
```

Meaning:

* x → extract

---

# 3. tar + gzip — Compressed Archive

---

### Create compressed archive:

```bash
tar -czvf backup.tar.gz folder
```

---

### Extract:

```bash
tar -xzvf backup.tar.gz
```

---

# 4. zip — Create Zip File

```bash
zip files.zip a.txt b.txt
```

---

# 5. unzip — Extract Zip

```bash
unzip files.zip
```

---

# 6. Practical Lab 🧠

```bash
mkdir backup
touch backup/a.txt backup/b.txt backup/c.txt
tar -czvf mybackup.tar.gz backup
rm -r backup
tar -xzvf mybackup.tar.gz
```

---

# 7. Mini Challenge 💡

1. Create folder `data`
2. Add 3 files
3. Create tar.gz backup
4. Delete folder
5. Restore backup

---

# 8. Important Tips ⚡

* tar.gz = most common backup format
* Always test backup restore

---
