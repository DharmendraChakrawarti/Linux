
---

# 🐧 CHAPTER 7 — FILE PERMISSIONS & OWNERSHIP

### *(chmod, chown, chgrp, umask)*

This chapter is **VERY IMPORTANT** for:

* Security 🔐
* Servers 🌐
* System Administration ⚙

---

# 1️⃣ Why Permissions Are Important?

Permissions decide:

* Who can **read** a file
* Who can **edit** a file
* Who can **run** a file

Without permissions → Linux would be **insecure** ❌

---

# 2️⃣ Permission Types (Very Simple)

| Symbol | Meaning | For Files | For Directories |
| ------ | ------- | --------- | --------------- |
| r      | Read    | View file | List files      |
| w      | Write   | Edit file | Create / delete |
| x      | Execute | Run file  | Enter directory |

---

# 3️⃣ Permission Structure Explained

### Check permissions:

```bash
ls -l
```

### Example Output:

```
-rwxr-xr--
```

### Breakdown:

```
-   rwx   r-x   r--
|   user  group others
```

| Part   | Meaning       |
| ------ | ------------- |
| user   | Owner         |
| group  | Group members |
| others | Everyone else |

---

# 4️⃣ Symbolic Permission Method (Without Numbers)

### Symbols:

```
u → user
g → group
o → others
a → all

+ → add
- → remove
= → set exact
```

---

## ➕ Add Permission

```bash
chmod u+r file.txt     # Add read to owner
chmod g+w file.txt     # Add write to group
chmod o+x script.sh   # Add execute to others
chmod a+r file.txt    # Add read to all
```

---

## ➖ Remove Permission

```bash
chmod u-w file.txt
chmod g-x script.sh
chmod o-r file.txt
chmod a-w file.txt
```

---

## 🎯 Set Exact Permission

```bash
chmod u=rw file.txt
chmod u=rwx file.txt
chmod a=r file.txt
```

---

## 🔄 Multiple Changes

```bash
chmod u+rwx,g+rx,o+r file.txt
```

---

# 5️⃣ Numeric Permission System (Very Important)

| Permission | Value |
| ---------- | ----- |
| r          | 4     |
| w          | 2     |
| x          | 1     |

### Combined Values:

| Permission | Number |
| ---------- | ------ |
| rwx        | 7      |
| rw-        | 6      |
| r-x        | 5      |
| r--        | 4      |

---

### Example:

```bash
chmod 755 file.sh
```

Meaning:

```
Owner  → rwx
Group  → r-x
Others → r-x
```

---

# 6️⃣ chmod — Change Permissions

```bash
chmod +x script.sh
chmod -w file.txt
chmod 644 file.txt
```

---

# 7️⃣ chown — Change Ownership

### Check owner:

```bash
ls -l
```

### Change owner:

```bash
sudo chown user file.txt
```

### Change owner + group:

```bash
sudo chown user:group file.txt
```

---

# 8️⃣ chgrp — Change Group Ownership

### Syntax:

```bash
chgrp group_name file_or_folder
```

### Example:

```bash
chgrp dev file.txt
```

### Recursive:

```bash
chgrp -R dev folder/
```

---

# 9️⃣ umask — Default Permission

### Show umask:

```bash
umask
```

Example Output:

```
0022
```

Meaning:

| Type      | Permission |
| --------- | ---------- |
| Directory | 755        |
| File      | 644        |

---

# 🔟 Practical Hands-on Lab 🧠

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

# 🧪 Mini Challenge 💡

1. Create `script.sh`
2. Give execute permission
3. Remove write permission
4. Check permissions

---

# ⚠️ Important Tips

* ❌ Never use **777** on production servers
* ✅ Always follow **Least Privilege Principle**
* 🔐 Give only **required permissions**

---

