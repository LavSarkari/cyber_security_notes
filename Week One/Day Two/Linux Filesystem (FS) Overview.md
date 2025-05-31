In Linux, **everything is treated as a file**: which includes hardware (like RAM, keyboard), sockets, and even processes.

- The filesystem starts at the **root directory**: `/`
- Key system directories:
    
    - `/home` — user-specific data and files
    - `/etc` — configuration files and system-wide settings
    - `/var` — variable data like logs, spool files, cache, etc.
    - `/bin` — essential user binaries (e.g., `ls`, `cp`, `mv`, etc.)

*and many more: check them with `ls /`*.

---

# **Permissions Model in Linux**

Each file and directory has **three permission types**:

- `r` — Read (view contents)
- `w` — Write (modify contents)
- `x` — Execute (run as a program or traverse directory)

And **three user classes**:

- **Owner** — user who owns the file
- **Group** — users in the same group
- **Others** — everyone else

Permissions are shown as 10-character strings:

```
-rwxr-xr--  → [file type][owner][group][others]
```
- `-`: is a file
- `d`: is a dir
### Common Commands:

- `chmod` — change permissions  
    e.g., `chmod 755 file`
- `chown` — change ownership  
    e.g., `chown user:group file`

---

# **`chmod` Permission Table**

Linux permissions can be represented using **numeric (octal)** or **symbolic** modes.

## 🔢 Numeric (Octal) Representation

Each permissio(read, write, execute) is assigned a value:

| Permission  | Value |
| ----------- | ----- |
| `r` (read)  | 4     |
| `w` (write) | 2     |
| `x` (exec)  | 1     |

To get the permission for each class (owner, group, others), **add the values**.

|Permission Set|Octal|Meaning|
|---|---|---|
|`---`|`0`|No permissions|
|`--x`|`1`|Execute only|
|`-w-`|`2`|Write only|
|`-wx`|`3`|Write + Execute|
|`r--`|`4`|Read only|
|`r-x`|`5`|Read + Execute|
|`rw-`|`6`|Read + Write|
|`rwx`|`7`|Full permissions|

### Common Examples:

|Command|Meaning|
|---|---|
|`chmod 755 file`|Owner: all, Group: read+exec, Others: read+exec|
|`chmod 644 file`|Owner: read+write, Group/Others: read-only|
|`chmod 700 file`|Only owner has full permissions|

## 🧬 Symbolic Representation

Syntax: `chmod [type][who][operator][permissions] file`

- **Who**: `u` (user), `g` (group), `o` (others), `a` (all)
- **Operator**: `+` (add), `-` (remove), `=` (set exact)
- **Permissions**: `r`, `w`, `x`

### Examples:

|Command|Meaning|
|---|---|
|`chmod u+x file`|Add execute to user|
|`chmod g-w file`|Remove write from group|
|`chmod o=r file`|Set others to read-only|
|`chmod a+x script`|Give execute to everyone|

---

# **Processes in Linux**

A **process** is any running program. Each has a **PID** (Process ID).

### Types:

- **Foreground** — runs interactively in terminal
- **Background** — runs silently using `&` (e.g., `python script.py &`)

### Key Commands:

- `ps` — list running processes
- `kill PID` — terminate a process by PID
- `htop` — interactive, ncurses-based process viewer (like GUI task manager) -> `apt install htop -y`
