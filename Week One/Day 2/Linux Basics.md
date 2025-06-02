In Linux, **everything is treated as a file**: yes, _everything_:

- Files and folders
- Hardware (RAM, CPU, USB, keyboard, etc.)
- System devices (network interfaces, storage)
- Commands and executables
- Running processes
- Even virtual constructs like `/proc` and `/sys`

This abstraction is what makes Linux **powerful and consistent**.

---

# **Orientation: Who, Where, What, How**

Let’s explore Linux like a terminal detective:

---

## 🧍‍♂️ **Who are you?**

```bash
whoami
```

Shows your current **logged-in username**.

---

## 📍 **Where are you?**

```bash
pwd
```

Prints the **current working directory** (like your GPS in the shell).

---

## 📂 **What do you have here?**

```bash
ls
```

Lists files and directories in your current location.  
Useful flags:

- `ls -l` → detailed list with permissions, owner, size, etc.
- `ls -a` → shows hidden files (those starting with `.`)

---

## 🚪 **How do you move around?**

```bash
cd <directory>
```

Changes your current directory. Examples:

- `cd Documents` → move into Documents
- `cd /etc` → jump to the system’s config directory
- `cd ~` → return to your home directory

---

## ⬅️ **How to go back?**

```bash
cd ..
```

Moves one level **up** the directory tree.

---

## 🌀 **What happens if you keep going back?**

Eventually, you’ll reach:

```bash
/
```

That’s the **root directory**: the origin of all files and folders in the system.  
It contains critical subdirectories like `/home`, `/bin`, `/etc`, `/var`, etc. 
[[Linux Filesystem (FS) Overview]] for more.

---
# 📂**Managing Files & Folders**

To Create a folder/dir:
```shell
mkdir <dirname> #eg. mkdir students
```

To Create a File:
```shell
touch <filename> #eg. touch coders.txt
```

To Remove a File:
```shell
rm <filename> 
```

To Remove a Folder:
```shell
rm -rf <foldername>
```

---
# Writing Contents Inside a File:

```shell
echo "hi my name is lav sarkari" > names.txt 
```

Or We Can Use `nano`:
```shell
nano <filename>
```

then to save a file in `nano`,  press `ctrl + o` hit enter to save the file, then press `ctrl + x` to exit `nano`.

---

# **Bonus: More Navigation & Exploration**

### 📎 **Absolute vs Relative Paths**

- Absolute: Starts from `/` (e.g., `/home/lav/Documents`)
- Relative: Based on where you are now (e.g., `cd ../Downloads`)

---

### 📜 **Show detailed file info**

```bash
stat file.txt
```

Gives timestamps, size, permissions, and inode of a file.

---

### 🧭 **Where is a command located?**

```bash
which ls
```

Shows the **full path** of an executable (e.g., `/bin/ls`).

---

### 📋 **How to view file contents?**

```bash
cat file.txt      # for small files  
less file.txt     # for large files, scrollable  
head file.txt     # view top lines  
tail file.txt     # view bottom lines
```

---

### 🔍 **Searching in files & directories**

```bash
grep "text" file.txt     # search for 'text' inside a file  
find /path -name "*.sh"  # find shell scripts recursively
```

---

### 🗄**Manual Of Tools**

To know more about any tools, we can use `tldr` (third party application),
Or, We should use `man`

- To Use `tldr`:
```shell
apt install tldr -y
tldr <name>
```

- To Use `man`:
```bash
man <name>
```

---
 
### 🐚 **Learn [[Shell Scripting Basics]]**
