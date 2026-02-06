
# 🐧 CHAPTER 23 — DISK MANAGEMENT & STORAGE (Beginner Friendly)

This chapter teaches how Linux **manages hard disks, partitions, and mounting**.

Very important for:

* Linux Admin
* Cloud Engineer
* DevOps
* Server Management

---

# 1. What is Disk Management?

Disk management means:

* Viewing disks
* Creating partitions
* Formatting disks
* Mounting disks
* Making storage permanent

---

# 2. List All Disks

```bash
lsblk
```

Shows:

* Disks
* Partitions
* Mount points

---

# 3. Check Disk Space

```bash
df -h
```

---

# 4. View Partition Table

```bash
sudo fdisk -l
```

---

# 5. Create Partition (Practice VM Only)

```bash
sudo fdisk /dev/xvdb
```

Commands inside fdisk:

```
n → new partition
p → primary
w → write & save
```

---

# 6. Format Disk (Create Filesystem)

```bash
sudo mkfs.ext4 /dev/xvdb1
```

---

# 7. Create Mount Directory

```bash
sudo mkdir /data
```

---

# 8. Mount Disk

```bash
sudo mount /dev/xvdb1 /data
```

Check:

```bash
df -h
```

---

# 9. Permanent Mount (VERY IMPORTANT)

Edit:

```bash
sudo nano /etc/fstab
```

Add:

```
/dev/xvdb1   /data   ext4   defaults   0   0
```

Test:

```bash
sudo mount -a
```

---

# 10. Unmount Disk

```bash
sudo umount /data
```

---

# 11. Swap Memory (Important)

Check:

```bash
free -h
```

Create swap:

```bash
sudo fallocate -l 1G /swapfile
sudo chmod 600 /swapfile
sudo mkswap /swapfile
sudo swapon /swapfile
```

---

# 🧪 PRACTICE TASKS — DISK

1️⃣ Check disks
2️⃣ Mount USB drive
3️⃣ Create mount directory
4️⃣ Make permanent mount

---

# 🧠 Admin Level Practice

1️⃣ Add new disk
2️⃣ Create partition
3️⃣ Format
4️⃣ Mount permanently

---
