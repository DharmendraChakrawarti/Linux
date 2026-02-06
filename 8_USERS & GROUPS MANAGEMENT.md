
# 🐧 CHAPTER 8 — USERS & GROUPS MANAGEMENT

### (useradd, userdel, groupadd, usermod, passwd)

This chapter teaches how to **manage users and groups in Linux** — a **very important admin skill**.

---

# 1. What is a User in Linux?

A **user** is a person who uses the system.

Examples:

* You
* Other employees
* System services

---

# 2. Types of Users

| User Type   | Meaning            |
| ----------- | ------------------ |
| Root        | Admin (full power) |
| Normal user | Limited access     |
| System user | For services       |

---

# 3. What is Root User?

Root is the **administrator**.

Root can:

* Delete anything
* Install anything
* Change system settings

⚠ Very dangerous if used wrongly.

---

# 4. What is a Group?

A **group** is a collection of users.

Used for:

* File permissions
* Access control

---

### Example:

Group → devops
Users → ram, shyam, tom

---

# 5. useradd — Create User

```bash
sudo useradd testuser
```

Set password:

```bash
sudo passwd testuser
```

---

# 6. userdel — Delete User

```bash
sudo userdel testuser
```

Delete user + home folder:

```bash
sudo userdel -r testuser
```

---

# 7. groupadd — Create Group

```bash
sudo groupadd devops
```

---

# 8. usermod — Add User to Group

```bash
sudo usermod -aG devops testuser
```

---

# 9. Check User & Group Info

---

### List users:

```bash
cat /etc/passwd
```

---

### List groups:

```bash
cat /etc/group
```

---

### Check user groups:

```bash
groups testuser
```

---

# 10. Switch User (Login as Another User)

```bash
su - testuser
```

Exit:

```bash
exit
```

---

# 11. Practical Lab 🧠

```bash
sudo groupadd developers
sudo useradd dev1
sudo passwd dev1
sudo usermod -aG developers dev1
groups dev1
```

---

# 12. Mini Challenge 💡

1. Create 3 users:

```
user1 user2 user3
```

2. Create group:

```
linuxgrp
```

3. Add all users to linuxgrp

---

# 13. Important Admin Tips ⚠

* Never share root password
* Always use sudo
* Follow least privilege

---
---
