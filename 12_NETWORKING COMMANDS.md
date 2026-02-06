

# 🐧 CHAPTER 12 — NETWORKING COMMANDS

### (ip a, ip r, ping, curl, wget)

This chapter teaches how to **check network connectivity, IP address, and download data**.

---

# 1. ip a — Check IP Address

### Meaning:

Shows **your system’s IP address and network interfaces**

```bash
ip a
```

---

### Example Output:

```
inet 192.168.1.10
```

This is your **system IP address**.

---

# 2. ip r — Check Routing Table

### Meaning:

Shows **how your system reaches internet**

```bash
ip r
```

---

# 3. ping — Check Internet Connectivity

### Meaning:

Checks if another system is **reachable**

```bash
ping google.com
```

Stop → `Ctrl + C`

---

### Example:

```bash
ping 8.8.8.8
```

---

# 4. curl — Get Web Data

### Meaning:

Download or view data from a URL

```bash
curl https://example.com
```

---

# 5. wget — Download Files

### Meaning:

Download file from internet

```bash
wget https://example.com/index.html
```

---

# 6. Practical Lab 🧠

```bash
ip a
ip r
ping google.com
curl https://example.com
```

---

# 7. Mini Challenge 💡

1. Find your IP address
2. Check if internet is working
3. Download a webpage using wget

---

# 8. Important Tips ⚡

* ping tests connectivity
* curl useful for APIs
* wget best for file downloads

---
