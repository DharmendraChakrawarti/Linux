
# 🐧 CHAPTER 16 — ENVIRONMENT VARIABLES

### (PATH, export, env, printenv)

This chapter is **VERY IMPORTANT** for:

* Linux
* DevOps
* Docker
* CI/CD
* Shell scripting
* AWS servers

---

# 1. What are Environment Variables?

They are **system values** used by Linux and applications.

---

### Example:

```bash
USER=dharmendra
HOME=/home/dharmendra
PATH=/usr/bin:/bin:/usr/local/bin
```

---

# 2. View Environment Variables

```bash
env
```

or

```bash
printenv
```

---

# 3. Check Specific Variable

```bash
echo $USER
echo $HOME
echo $PATH
```

---

# 4. What is PATH? (VERY IMPORTANT)

PATH tells Linux **where to find commands**

---

### Check:

```bash
echo $PATH
```

---

### Example:

If PATH not set → commands won’t run

---

# 5. Create Your Own Variable

```bash
MYNAME=Dharmendra
echo $MYNAME
```

---

# 6. Export Variable (Make it Global)

```bash
export MYCITY=Bangalore
```

---

# 7. Permanent Variables

Open profile file:

```bash
nano ~/.bashrc
```

Add:

```bash
export JAVA_HOME=/usr/lib/jvm/java-17
```

Apply:

```bash
source ~/.bashrc
```

---

# 8. Practical Lab 🧠

```bash
MYAPP=DevOps
echo $MYAPP
export MYAPP
bash
echo $MYAPP
```

---

# 9. Mini Challenge 💡

1. Create variable `PROJECT=Terraform`
2. Make it permanent
3. Open new terminal → check it

---
