### 🔹 **Task 1: Create a File and a Folder**

> 🔸 Practice using `mkdir` and `touch`

```bash
mkdir myfolder
cd myfolder
touch file1.txt
```

✅ **Check**:

```bash
ls -l
```

📝 _Q: What do you see after `ls -l`? Which part shows the file's name?_

---

### 🔹 **Task 2: View and Understand Permissions**

> 🔸 List the permission bits of the file you just created

```bash
ls -l file1.txt
```

📝 _Q: What are the letters on the left? What do `r`, `w`, and `x` stand for?_

---

### 🔹 **Task 3: Change File Permissions**

> 🔸 Give yourself execute permission for the file

```bash
chmod +x file1.txt
ls -l
```

📝 _Q: What changed in the permission string? What does `+x` mean?_

---

### 🔹 **Task 4: Remove Write Permission from Others**

> 🔸 Limit file editing to only yourself

```bash
chmod o-w file1.txt
ls -l
```

📝 _Q: What part of the permissions string changed? Who is “others”?_

---

### 🔹 **Task 5: Change File Ownership (View Only)**

> 🔸 Show who owns the file (don’t change it, just observe)

```bash
ls -l
```

📝 _Q: Who is the owner? Who is the group?_

---

### 🔹 **Task 6: View All Files with Details**

> 🔸 Explore listing everything including hidden files

```bash
ls -la
```

📝 _Q: What does the dot (`.`) file represent? What is `..`?_
