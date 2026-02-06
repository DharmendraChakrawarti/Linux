
# 🐧 CHAPTER 22 — SSH & REMOTE SERVER MANAGEMENT (Beginner Friendly)

This chapter is **EXTREMELY IMPORTANT** for:

* Linux Admin
* DevOps Engineer
* Cloud Engineer
* AWS / Azure / GCP

If you know SSH → **you can control any server in the world** 🌍🔥

---

# 1. What is SSH?

**SSH (Secure Shell)** is a secure way to **connect to a remote Linux server**.

Think:

> Remote login to another Linux machine securely 🔐

---

# 2. Why SSH is Important?

* Connect to cloud servers
* Manage production servers
* Secure communication
* Transfer files securely

---

# 3. SSH Basic Syntax

```bash
ssh username@server_ip
```

Example:

```bash
ssh ubuntu@192.168.1.10
```

---

# 4. First Time SSH Connection

When connecting first time:

```
Are you sure you want to continue connecting?
```

Type:

```
yes
```

---

# 5. SSH Using Key Authentication (VERY IMPORTANT 🔥)

This is **industry standard method**.

---

### Step 1: Create SSH Key Pair

```bash
ssh-keygen
```

Press Enter → Enter → Enter

Keys created in:

```
~/.ssh/id_rsa
~/.ssh/id_rsa.pub
```

---

### Step 2: Copy Public Key to Server

```bash
ssh-copy-id user@server_ip
```

---

### Step 3: Login Without Password

```bash
ssh user@server_ip
```

You will login **without password** 🔥

---

# 6. Copy Files Using SCP

---

### Copy local → server

```bash
scp file.txt user@server_ip:/home/user/
```

---

### Copy server → local

```bash
scp user@server_ip:/home/user/file.txt .
```

---

# 7. Sync Files Using rsync (VERY IMPORTANT)

Better than scp.

---

```bash
rsync -avz folder/ user@server_ip:/home/user/folder/
```

---

# 8. SSH Config File (Advanced)

File:

```bash
~/.ssh/config
```

Example:

```bash
Host myserver
  HostName 192.168.1.10
  User ubuntu
  IdentityFile ~/.ssh/id_rsa
```

Now connect:

```bash
ssh myserver
```

---

# 9. Real Cloud Example (AWS EC2)

```bash
ssh -i key.pem ubuntu@ec2-public-ip
```

---

# 🧪 PRACTICE TASKS — SSH

1️⃣ Generate SSH key
2️⃣ Copy key to server
3️⃣ Login without password
4️⃣ Transfer file using scp
5️⃣ Sync folder using rsync

---

# 🧠 Admin Level Practice

1️⃣ Disable password login
2️⃣ Allow only key login
3️⃣ Harden SSH security

---
