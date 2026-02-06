

# 🐧 CHAPTER 14 — SERVICES & systemctl

### (start, stop, restart, status, enable, disable)

This chapter teaches how to **control system services (servers)** in Linux.

---

# 1. What is a Service?

A **service** is a program that **runs continuously in background**.

Examples:

* Web server (nginx, apache)
* Database (mysql)
* SSH server

---

# 2. What is systemctl?

`systemctl` is used to **control services**.

---

# 3. Check Service Status

```bash
sudo systemctl status nginx
```

---

# 4. Start a Service

```bash
sudo systemctl start nginx
```

---

# 5. Stop a Service

```bash
sudo systemctl stop nginx
```

---

# 6. Restart a Service

```bash
sudo systemctl restart nginx
```

---

# 7. Enable Service at Boot

```bash
sudo systemctl enable nginx
```

---

# 8. Disable Service at Boot

```bash
sudo systemctl disable nginx
```

---

# 9. List All Services

```bash
systemctl list-units --type=service
```

---

# 10. Practical Lab 🧠

```bash
sudo apt install nginx
sudo systemctl start nginx
sudo systemctl status nginx
```

Open browser → your IP → see nginx page.

---

# 11. Mini Challenge 💡

1. Install nginx
2. Start nginx
3. Enable nginx
4. Stop nginx

---

# 12. Important Admin Tips ⚠

* Always check status after start
* Enable only required services

---
