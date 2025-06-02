## 🦭 **Shell Scripting???**

- Bash, Zsh etc..
## 🐚 **What is Bash?**

- A **shell language** used to interact with Unix/Linux systems.
- Supports **simple command execution**, **scripting**, and **automation**.

### 🔹 Why Bash?

- Most **commonly used** shell in Linux systems.
- **Pre-installed** on most Unix-like OS (Linux, macOS).
- **Lightweight** and **fast**: ideal for system-level scripting.

### 🔻 Drawbacks of Bash

- **Limited features** compared to modern languages.
- **No Object-Oriented Programming (OOP)** support.
- Syntax and debugging can be **less intuitive** than Python.

> 📌 In short:  
> Bash is a **lightweight**, **universally supported**, and **non-exclusive** scripting language: great for quick system tasks.

---

## ✍️ Let's Write Some Bash!

### ✅ Shebang (`#!`)

Placed at the **top of the script** to tell the kernel what interpreter to use:

```bash
#!/bin/bash
```

Without this, running `./file.sh` won't work unless you explicitly use `bash file.sh`.

---

### 🧠 **Variables and I/O**

```bash
#!/bin/bash

# Variable declaration
VarOne="My name is Lav !!"
VarTwo="I'm Hacker."

# Output using echo
echo "$VarOne and $VarTwo"

# Input from user
echo "Who are you?"
read about_user

# Display input
echo "You said: $about_user"
```

#### Key Points:

- Variables don't need a `$` when being defined.
- Use `$VarName` to **access** the variable.
- `echo` prints to the terminal.
- `read` captures user input into a variable.

---

## 📦 **Positional Arguments**

When a script is executed with arguments:

```bash
bash script.sh arg1 arg2
```

These arguments are accessed using **positional parameters**:

```bash
#!/bin/bash

echo "Hey $1 $2, you ran the file: $0"
```

- `$0` → Script name (`script.sh`)
- `$1`, `$2` → First and second argumen

#### Example:

If run as:

```bash
./greet.sh Tony Stark
```

The output will be:

```
Hey Tony Stark, you ran the file: ./greet.sh
```

---

## ✅ Summary

- Bash is ideal for **quick system tasks** and **scripting automation**.
- Learn it for **DevOps, scripting**, and **Linux mastery**.
- Limited in structure but powerful in **command chaining**, **process control**, and **scripting glue code**.

