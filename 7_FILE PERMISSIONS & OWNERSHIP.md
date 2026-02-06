

# 🐧 CHAPTER 7 — FILE PERMISSIONS & OWNERSHIP

### (chmod, chown, umask)

This chapter is **VERY IMPORTANT** for:

* Security 🔐
* Servers 🌐
* Admin work ⚙

---

# 1. Why Permissions Are Important?

Permissions decide:

* Who can **read** a file
* Who can **edit** a file
* Who can **run** a file

Without permissions → Linux would be **insecure**.

---

# 2. Permission Types (Very Simple)

| Symbol | Meaning            |
| ------ | ------------------ |
| r      | Read → View file   |
| w      | Write → Edit file  |
| x      | Execute → Run file |

---

# 3. Permission Structure Explained

Check permissions:

```bash
ls -l
```

Example output:

```
-rwxr-xr--
```

Break it:

```
-  rwx   r-x   r--
|  user  group others
```

| Part   | Meaning       |
| ------ | ------------- |
| user   | File owner    |
| group  | Group members |
| others | Everyone else |

---

# 4. Numeric Permission System (Very Important)

| Permission | Number |
| ---------- | ------ |
| r          | 4      |
| w          | 2      |
| x          | 1      |

Add values:

| Permission | Value |
| ---------- | ----- |
| rwx        | 7     |
| rw-        | 6     |
| r-x        | 5     |
| r--        | 4     |

---

### Example:

```bash
chmod 755 file.sh
```

Means:

```
Owner → 7 → rwx
Group → 5 → r-x
Others → 5 → r-x
```

---

# 5. chmod — Change Permission

---

### Give execute permission:

```bash
chmod +x script.sh
```

---

### Remove write permission:

```bash
chmod -w file.txt
```

---

### Numeric method:

```bash
chmod 644 file.txt
```

---

# 6. chown — Change Ownership

Check owner:

```bash
ls -l
```

---

### Change owner:

```bash
sudo chown user file.txt
```

---

### Change owner + group:

```bash
sudo chown user:group file.txt
```

---

# 7. umask — Default Permission

Shows default permission setting.

```bash
umask
```

Common output:

```
0022
```

Means:

* Default folder → 755
* Default file → 644

---

# 8. Practical Hands-on Lab 🧠

```bash
mkdir permtest
cd permtest
touch file.txt
ls -l
chmod 600 file.txt
ls -l
chmod 755 file.txt
ls -l
```

---

# 9. Mini Challenge 💡

1. Create file `script.sh`
2. Give execute permission
3. Remove write permission
4. Check permissions

---

# 10. Important Tips ⚠

* Never give **777** permission on production server
* Always follow **least privilege rule**

---
