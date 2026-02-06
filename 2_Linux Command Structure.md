

# **2. Linux Command Structure**

Every Linux command generally follows this structure:

```
command [options] [arguments]
```

### **Example:**

```
ls -l /home/user
```

### **Breakdown:**

| Part         | Meaning                      |
| ------------ | ---------------------------- |
| `ls`         | Command (list files)         |
| `-l`         | Option (long listing format) |
| `/home/user` | Argument (path/location)     |

---

# **Basic Parts Explained**

## **1. Command**

The actual instruction to Linux.

Examples:

```
ls      → list files
pwd     → show current directory
date    → show current date & time
whoami  → show current user
```

---

## **2. Options (Flags)**

They modify how the command behaves.

They usually start with `-` or `--`

Examples:

```
ls -a      → show hidden files
ls -lh     → human readable size
rm -rf     → force delete recursively
```

---

## **3. Arguments**

They tell the command *on what* to act.

Examples:

```
ls /etc
cat file.txt
rm test.txt
```

---

# **Some Real Examples**

```
mkdir myfolder
```

➡ Create a folder named `myfolder`

```
rm -rf myfolder
```

➡ Delete folder forcefully

```
cp file1.txt file2.txt
```

➡ Copy file1 → file2

```
mv old.txt new.txt
```

➡ Rename file

---

# **Command Chaining**

Run multiple commands in one line:

### **Using `;`**

```
mkdir test; cd test; touch a.txt
```

### **Using `&&` (Next runs only if previous succeeds)**

```
mkdir test && cd test
```

---

# **Getting Help in Linux**

```
man ls
ls --help
```

---

# **Mini Practice for You 💻**

Try these:

```
pwd
ls
mkdir demo
cd demo
touch file1.txt
ls -l
```

---
