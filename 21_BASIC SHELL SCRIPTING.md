

# 🐧 CHAPTER 21 — BASIC SHELL SCRIPTING (BEGINNER FRIENDLY)

This is **EXTREMELY IMPORTANT** for:

* Linux Admin
* DevOps Engineer
* Automation
* Cloud

If you learn this → you move from **user → engineer** 💻🔥

---

# 1. What is Shell Scripting?

Shell scripting means:

> Writing **Linux commands inside a file** to automate tasks.

Example:
Instead of running 10 commands daily → write **1 script** and run once.

---

# 2. What is a Shell Script File?

Shell script file ends with:

```
.sh
```

Example:

```
backup.sh
deploy.sh
cleanup.sh
```

---

# 3. Create Your First Script

```bash
nano first.sh
```

Add:

```bash
#!/bin/bash
echo "Hello Linux"
echo "Welcome to Shell Scripting"
```

Save → Exit

---

# 4. Make Script Executable

```bash
chmod +x first.sh
```

Run:

```bash
./first.sh
```

---

# 5. Variables in Shell Script

Variables store values.

---

### Example:

```bash
#!/bin/bash
name="Dharmendra"
echo "My name is $name"
```

---

# 6. User Input

```bash
#!/bin/bash
echo "Enter your name:"
read name
echo "Welcome $name"
```

---

# 7. If Condition (Decision Making)

```bash
#!/bin/bash
echo "Enter your age:"
read age

if [ $age -ge 18 ]
then
  echo "You are eligible"
else
  echo "You are NOT eligible"
fi
```

---

# 8. For Loop

```bash
#!/bin/bash
for i in 1 2 3 4 5
do
  echo "Number $i"
done
```

---

# 9. While Loop

```bash
#!/bin/bash
count=1
while [ $count -le 5 ]
do
  echo "Count = $count"
  ((count++))
done
```

---

# 10. Real Admin Script Example 🔥

### Disk Usage Alert Script

```bash
#!/bin/bash
df -h | grep /dev/root > disk.txt
cat disk.txt
```

---

# 🧪 PRACTICE TASKS — SHELL SCRIPTING

1️⃣ Create script to print your name
2️⃣ Create input script
3️⃣ Create loop script
4️⃣ Create disk monitoring script

---
