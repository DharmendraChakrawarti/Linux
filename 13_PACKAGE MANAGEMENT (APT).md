

# 🐧 CHAPTER 13 — PACKAGE MANAGEMENT (APT)

### (apt update, install, remove, upgrade)

This chapter teaches how to **install, update, and remove software in Linux**.

---

# 1. What is a Package Manager?

A **package manager** helps you:

* Install software
* Update software
* Remove software

Just like:

* Play Store (Android)
* Microsoft Store (Windows)

In Ubuntu → **APT**

---

# 2. apt update — Update Software List

### Meaning:

Updates list of available software packages.

```bash
sudo apt update
```

---

# 3. apt upgrade — Update Installed Software

### Meaning:

Upgrades all installed software.

```bash
sudo apt upgrade
```

---

# 4. apt install — Install Software

### Example: Install nginx web server

```bash
sudo apt install nginx
```

---

### Install multiple packages:

```bash
sudo apt install git curl vim
```

---

# 5. apt remove — Remove Software

```bash
sudo apt remove nginx
```

---

# 6. apt purge — Remove + Delete Config Files

```bash
sudo apt purge nginx
```

---

# 7. Check Installed Package

```bash
dpkg -l | grep nginx
```

---

# 8. Practical Lab 🧠

```bash
sudo apt update
sudo apt install tree
tree
```

---

# 9. Mini Challenge 💡

1. Install `htop`
2. Run `htop`
3. Remove `htop`

---

# 10. Important Tips ⚡

* Always run `apt update` before install
* Use sudo

---
