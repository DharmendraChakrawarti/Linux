

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
Got it 👍 You want **Linux permissions WITHOUT numeric method** — only **symbolic method** (u, g, o, a).

---

# 🔐 Linux Permissions – WITHOUT Numeric Method (Beginner Friendly)

We use **symbolic notation**:

```
u → user (owner)
g → group
o → others
a → all (u+g+o)

+ → add permission
- → remove permission
= → set exact permission
```

Permissions:

```
r → read
w → write
x → execute
```

---

# 🔍 Check Permissions

```bash
ls -l
```

Example:

```
-rw-r--r-- 1 root root file.txt
```

---

# ➕ Add Permission

### Add read to owner:

```bash
chmod u+r file.txt
```

### Add write to group:

```bash
chmod g+w file.txt
```

### Add execute to others:

```bash
chmod o+x script.sh
```

### Add read to everyone:

```bash
chmod a+r file.txt
```

---

# ➖ Remove Permission

### Remove write from owner:

```bash
chmod u-w file.txt
```

### Remove execute from group:

```bash
chmod g-x script.sh
```

### Remove read from others:

```bash
chmod o-r file.txt
```

### Remove write from all:

```bash
chmod a-w file.txt
```

---

# 🎯 Set Exact Permission (=)

### Set only read & write for owner:

```bash
chmod u=rw file.txt
```

### Set full permission for owner:

```bash
chmod u=rwx file.txt
```

### Set only read for all:

```bash
chmod a=r file.txt
```

---

# 🔄 Multiple Changes in One Command

```bash
chmod u+rwx,g+rx,o+r file.txt
```

Meaning:

* Owner → rwx
* Group → r-x
* Others → r--

---

# 📂 Directory Permission Example

### Give full access to owner, read+execute to others:

```bash
chmod u=rwx,go=rx mydir
```

---

# 🛡️ Special Permissions (Without Numbers)

### SUID:

```bash
chmod u+s file
```

### SGID:

```bash
chmod g+s folder
```

### Sticky Bit:

```bash
chmod +t /shared
```

---

# 🧠 Real-Life Examples

### Make script executable:

```bash
chmod u+x deploy.sh
```

### Make file read-only:

```bash
chmod a-w report.txt
```

### Secure private file:

```bash
chmod u=rw,go= private.txt
```

---

# ⚡ Quick Practice

```bash
touch demo.txt
chmod u=rw,g=r,o= demo.txt
ls -l demo.txt
```

---

If you want, I can give:

✅ **Practice tasks**
✅ **Interview Q&A**
✅ **Real-world permission scenarios**

Just say 😄

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
