
# 🐧 CHAPTER 24 — SUDO & PRIVILEGE MANAGEMENT (Beginner Friendly)

This chapter teaches **how Linux controls admin (root) access securely**.

Very important for:

* Linux Admin
* DevOps
* Cloud Security
* Production Servers

---

# 1. What is sudo?

`sudo` = **Super User DO**

It allows **normal users to run admin commands safely**.

---

### Example:

```bash
sudo apt update
```

Means:

> Run command as administrator (root)

---

# 2. What is root User?

`root` is **the main administrator account in Linux**.

* Full control
* Can delete anything
* Can break system

That’s why **normal users use sudo instead of logging in as root**.

---

# 3. Switch to Root User

```bash
sudo su -
```

Exit root:

```bash
exit
```

---

# 4. Check Who Has sudo Access

```bash
getent group sudo
```

---

# 5. Add User to sudo Group

```bash
sudo usermod -aG sudo username
```

Example:

```bash
sudo usermod -aG sudo devuser
```

Logout → Login again → sudo works.

---

# 6. sudoers File (VERY IMPORTANT ⚠)

This file controls **who can run what using sudo**.

File:

```bash
/etc/sudoers
```

⚠ NEVER edit directly.

Use:

```bash
sudo visudo
```

---

# 7. Give Full Sudo Access to User

Inside visudo:

```
devuser ALL=(ALL:ALL) ALL
```

---

# 8. Give Limited Sudo Access (Very Important for Security)

Allow user to restart nginx only:

```
devuser ALL=(ALL) /bin/systemctl restart nginx
```

---

# 9. Check sudo Logs

```bash
sudo grep sudo /var/log/auth.log
```

---

# 10. Disable Root SSH Login (SECURITY BEST PRACTICE 🔐)

Edit:

```bash
sudo nano /etc/ssh/sshd_config
```

Change:

```
PermitRootLogin no
```

Restart ssh:

```bash
sudo systemctl restart ssh
```

---

# 🧪 PRACTICE TASKS — SUDO

1️⃣ Create new user
2️⃣ Give sudo access
3️⃣ Test sudo command
4️⃣ Limit sudo permission

---

# 🧠 Admin Level Practice

1️⃣ Create devops user
2️⃣ Give limited sudo
3️⃣ Harden sudo rules

---
