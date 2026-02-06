

# 🐧 CHAPTER 17 — PACKAGE MANAGEMENT (Beginner Friendly)

This chapter teaches **how to install, update, remove software in Linux**.

Very important for:

* Linux Admin
* DevOps
* AWS / Azure servers
* Docker images

---

# 1. What is a Package Manager?

A **package manager** is a tool that:

* Installs software
* Updates software
* Removes software
* Handles dependencies automatically

---

### Example:

Instead of downloading Chrome manually → Linux does:

```bash
sudo apt install google-chrome-stable
```

---

# 2. Types of Package Managers

| Linux OS        | Package Manager |
| --------------- | --------------- |
| Ubuntu / Debian | apt             |
| RHEL / CentOS   | yum / dnf       |
| Fedora          | dnf             |
| Universal       | snap            |

---

# 3. apt (Most Important – Ubuntu)

---

## Update Package List (FIRST STEP ALWAYS)

```bash
sudo apt update
```

### Meaning:

* Downloads latest software list from internet
* Does NOT install anything

---

## Upgrade Installed Packages

```bash
sudo apt upgrade
```

### Meaning:

* Updates already installed software

---

# 4. Install Any Software

### Example: Install git

```bash
sudo apt install git
```

---

### Install multiple software:

```bash
sudo apt install git curl wget unzip -y
```

`-y` → auto yes (no confirmation)

---

# 5. Check Installed Version

```bash
git --version
```

---

# 6. Remove Software

```bash
sudo apt remove git
```

---

# 7. Completely Remove (with config files)

```bash
sudo apt purge git
```

---

# 8. Search Any Software

```bash
apt search nginx
```

---

# 9. Clean System (Important)

```bash
sudo apt autoremove
sudo apt autoclean
```

### Meaning:

* Removes unused packages
* Cleans disk space

---

# 10. yum & dnf (RedHat / CentOS)

### Install:

```bash
sudo yum install git -y
```

or

```bash
sudo dnf install git -y
```

---

### Update:

```bash
sudo yum update -y
```

or

```bash
sudo dnf update -y
```

---

# 11. snap (Universal Package Manager)

Install snap app:

```bash
sudo snap install postman
```

---

# 12. Real DevOps Usage Example 🔥

Install all DevOps tools:

```bash
sudo apt update
sudo apt install -y git docker.io docker-compose terraform ansible awscli
```

---

# 🧠 Mini Practice Lab

Run:

```bash
sudo apt update
sudo apt install git -y
git --version
```

---
