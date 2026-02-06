
# 🐧 CHAPTER 6 — VIEWING & EDITING FILES

### (cat, less, nano, vim)

This chapter teaches how to **read and edit files in Linux**.

---

# 1. cat — View File Content

### Meaning:

`cat` = **Concatenate**

Used mainly to **display file content**

---

### Example:

```bash
cat file.txt
```

---

### Show multiple files:

```bash
cat a.txt b.txt
```

---

### Create file using cat:

```bash
cat > test.txt
```

Type something → Press **Ctrl + D** to save.

---

# 2. less — Scroll File Content

Used when file is **large**

---

### Example:

```bash
less /etc/passwd
```

### Controls:

| Key   | Action        |
| ----- | ------------- |
| Space | Next page     |
| b     | Previous page |
| q     | Quit          |

---

# 3. nano — Simple Text Editor (Best for Beginners)

---

### Open file:

```bash
nano file.txt
```

---

### Save:

```
Ctrl + O
Enter
```

---

### Exit:

```
Ctrl + X
```

---

### Example:

```bash
nano linux.txt
```

Type:

```
Linux is simple
Linux is powerful
```

Save and exit.

---

# 4. vim — Advanced Editor (Just Basics)

---

### Open file:

```bash
vim file.txt
```

---

### Modes:

| Mode | Meaning             |
| ---- | ------------------- |
| i    | Insert (write mode) |
| ESC  | Command mode        |

---

### Save & Exit:

```
:wq
```

---

### Exit without save:

```
:q!
```

---

# 5. Practical File Editing Lab 🧠

```bash
mkdir filepractice
cd filepractice
touch notes.txt
nano notes.txt
```

Write:

```
I am learning Linux
Linux is interesting
```

Save and exit.

Then:

```bash
cat notes.txt
```

---

# 6. Difference Between cat & less

| cat                  | less               |
| -------------------- | ------------------ |
| Shows entire file    | Scroll view        |
| Good for small files | Good for big files |

---

# 7. Mini Challenge 💡

1. Create file `about.txt`
2. Write 5 lines
3. View using `cat`
4. View using `less`

---

# 8. Important Tips ⚡

* Use **nano** as beginner
* Use **vim** when you become advanced
* Use **less** for large logs

---
