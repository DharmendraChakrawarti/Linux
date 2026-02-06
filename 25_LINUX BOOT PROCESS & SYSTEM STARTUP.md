

# 🐧 CHAPTER 25 — LINUX BOOT PROCESS & SYSTEM STARTUP (Beginner Friendly)

This chapter explains **what happens when you power ON a Linux system**.

This is **important for troubleshooting boot failures & admin-level debugging**.

---

# 1. What is Boot Process?

Boot process =

> Steps Linux follows to **start the operating system**

---

# 2. Linux Boot Process Flow (Simple)

```
Power ON
   ↓
BIOS / UEFI
   ↓
Bootloader (GRUB)
   ↓
Kernel
   ↓
Init System (systemd)
   ↓
Services
   ↓
Login Screen
```

---

# 3. Step-by-Step Explanation

---

## Step 1 — BIOS / UEFI

* Checks hardware
* Loads bootloader

---

## Step 2 — Bootloader (GRUB)

* Select OS
* Loads kernel

File:

```bash
/boot/grub/grub.cfg
```

---

## Step 3 — Kernel

* Core of Linux OS
* Controls CPU, memory, hardware

Check kernel version:

```bash
uname -r
```

---

## Step 4 — systemd (Init System)

* Starts services
* Manages system

Check:

```bash
ps -p 1
```

Output: systemd

---

## Step 5 — Services Start

Examples:

* Network
* SSH
* Docker
* Web servers

---

## Step 6 — Login Prompt

System ready for use 🎉

---

# 4. systemd Targets (Runlevels)

| Old | New               | Meaning  |
| --- | ----------------- | -------- |
| 0   | poweroff.target   | Shutdown |
| 1   | rescue.target     | Rescue   |
| 3   | multi-user.target | CLI mode |
| 5   | graphical.target  | GUI      |
| 6   | reboot.target     | Reboot   |

---

# 5. Check Current Target

```bash
systemctl get-default
```

---

# 6. Change Boot Target

### Switch to CLI mode:

```bash
sudo systemctl set-default multi-user.target
```

---

### Switch to GUI mode:

```bash
sudo systemctl set-default graphical.target
```

---

# 7. View Boot Logs (VERY IMPORTANT)

```bash
journalctl -b
```

---

# 8. Troubleshooting Boot Problems

```bash
systemctl --failed
```

---

# 🧪 PRACTICE TASKS — BOOT PROCESS

1️⃣ Check kernel version
2️⃣ Check systemd
3️⃣ View boot logs
4️⃣ Check failed services

---

# 🧠 Admin Level Practice

1️⃣ Switch default target
2️⃣ Debug boot delay
3️⃣ Find failed startup services

---
