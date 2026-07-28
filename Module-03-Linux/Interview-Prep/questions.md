# 🐧 Linux Interview Questions

## 1. What is Linux?

### Answer

Linux is an open-source, Unix-like operating system kernel created by Linus Torvalds in 1991. It is widely used in servers, cloud computing, embedded systems, and DevOps because of its stability, security, and flexibility.

**Examples:**
- Ubuntu
- CentOS
- Red Hat Enterprise Linux (RHEL)
- Debian
- Fedora

---

## 2. Why is Linux preferred in DevOps?

### Answer

Linux is preferred because:

- Open Source
- Stable and reliable
- Secure
- Powerful command-line interface
- Easy automation using Bash scripting
- Supports Docker and Kubernetes
- Most cloud servers run Linux

---

## 3. What is the difference between Linux and Unix?

| Linux | Unix |
|--------|------|
| Open Source | Mostly Proprietary |
| Free | Usually Licensed |
| Community Developed | Developed by Vendors |
| Runs on many platforms | Runs on specific hardware |

---

## 4. What is the Linux Kernel?

### Answer

The kernel is the core component of Linux.

It acts as a bridge between hardware and software by managing:

- CPU
- Memory
- Devices
- Processes
- File System

Without the kernel, the operating system cannot function.

---

## 5. What is Shell?

### Answer

A shell is a command-line interpreter that allows users to interact with the operating system.

Popular shells:

- Bash
- Zsh
- Fish
- Korn Shell

Example:

```bash
ls
pwd
mkdir test
```

---

## 6. What is Bash?

### Answer

Bash (Bourne Again Shell) is the default shell in many Linux distributions.

It is used for:

- Running commands
- Writing shell scripts
- Automation

---

## 7. What is the root user?

### Answer

The root user is the superuser in Linux.

It has permission to perform all administrative tasks such as:

- Installing software
- Creating users
- Deleting files
- Changing permissions

---

## 8. What is sudo?

### Answer

`sudo` allows a normal user to execute commands with administrative (root) privileges without logging in as the root user.

Example:

```bash
sudo apt update
```

---

## 9. What is the difference between Root and Sudo?

| Root | Sudo |
|------|------|
| Permanent administrator account | Temporary elevated privileges |
| Full access at all times | Access only for specific commands |
| Riskier if misused | More secure for daily administration |

---

## 10. What is a Linux Distribution?

### Answer

A Linux distribution (distro) is a complete operating system built around the Linux kernel.

Examples:

- Ubuntu
- Debian
- Fedora
- CentOS
- Rocky Linux
- RHEL

---

## 11. What is the Linux File System?

### Answer

Linux stores everything as files in a hierarchical directory structure starting from the root directory (`/`).

Examples:

- `/home`
- `/etc`
- `/var`
- `/tmp`
- `/usr`

---

## 12. What is the root directory (`/`)?

### Answer

The root directory (`/`) is the top-most directory in Linux.

Every other file and directory exists under it.

Example:

```
/
├── home
├── etc
├── var
├── usr
└── tmp
```

---

## 13. What is the difference between Root (/) and Root User?

| Root (/) | Root User |
|----------|-----------|
| Top-level directory | Administrator account |
| Part of the file system | User with highest privileges |

---

## 14. What is CLI?

### Answer

CLI (Command Line Interface) is a text-based interface used to interact with the operating system by typing commands.

Example:

```bash
ls
pwd
cd
```

---

## 15. What is GUI?

### Answer

GUI (Graphical User Interface) allows users to interact with the operating system using windows, icons, buttons, and menus.

Examples:

- GNOME
- KDE Plasma
- XFCE

# 🐧 Linux Interview Questions (Part 2)

---

## 16. What are file permissions in Linux?

### Answer

File permissions determine who can read, write, or execute a file or directory.

There are three types of users:
- Owner (u)
- Group (g)
- Others (o)

There are three permissions:
- Read (r = 4)
- Write (w = 2)
- Execute (x = 1)

Example:

```bash
-rwxr-xr--
```

Here:
- Owner → rwx
- Group → r-x
- Others → r--

---

## 17. What does `chmod` do?

### Answer

`chmod` changes the permissions of a file or directory.

Example:

```bash
chmod 755 script.sh
```

Permission Breakdown:

```
7 = rwx
5 = r-x
5 = r-x
```

Meaning:
- Owner → Read, Write, Execute
- Group → Read, Execute
- Others → Read, Execute

---

## 18. What is `chown`?

### Answer

`chown` changes the owner of a file or directory.

Example:

```bash
sudo chown kartik file.txt
```

To change both owner and group:

```bash
sudo chown kartik:developers file.txt
```

---

## 19. What is `umask`?

### Answer

`umask` sets the default permissions for newly created files and directories.

Example:

```bash
umask
```

Output:

```
0022
```

Default Permissions:

Files → 666

Directories → 777

After applying umask 022:

Files → 644

Directories → 755

---

## 20. What is the difference between Hard Link and Soft Link?

| Hard Link | Soft Link |
|-----------|-----------|
| Shares same inode | Has different inode |
| Cannot cross file systems | Can cross file systems |
| Cannot link directories | Can link directories |
| Original file can be deleted only if links remain | Breaks if original file is deleted |

Create:

```bash
ln file.txt hardlink
```

```bash
ln -s file.txt softlink
```

---

## 21. What is an inode?

### Answer

An inode is a data structure that stores metadata about a file.

It stores:

- Owner
- Permissions
- File size
- Creation time
- Modification time
- File location

It does **not** store the file name.

View inode number:

```bash
ls -i
```

---

## 22. What is a process?

### Answer

A process is a program that is currently running.

Example:

Running Firefox or executing a Bash script creates one or more processes.

Useful commands:

```bash
ps
```

```bash
top
```

```bash
htop
```

---

## 23. Difference between `kill` and `kill -9`?

### Answer

`kill`

Sends the SIGTERM signal.

Allows the program to close gracefully.

Example:

```bash
kill 1234
```

---

`kill -9`

Sends the SIGKILL signal.

Forcefully terminates the process.

Example:

```bash
kill -9 1234
```

Use `kill -9` only if the process does not stop with a normal `kill`.

---

## 24. What is the difference between `ps` and `top`?

| ps | top |
|----|-----|
| Snapshot of running processes | Real-time monitoring |
| Static output | Continuously updates |
| Good for scripting | Good for monitoring |

---

## 25. What is PID?

### Answer

PID stands for **Process ID**.

Every running process has a unique PID assigned by the operating system.

View:

```bash
ps -ef
```

---

## 26. What is a daemon process?

### Answer

A daemon is a background process that runs without user interaction and provides system or application services.

Examples:
- `sshd`
- `cron`
- `systemd`
- `httpd`

---

## 27. What is the purpose of `/etc/passwd`?

### Answer

The `/etc/passwd` file stores basic user account information.

It contains:
- Username
- UID
- GID
- Home directory
- Login shell

View:

```bash
cat /etc/passwd
```

---

## 28. What is `/etc/shadow`?

### Answer

`/etc/shadow` stores encrypted user passwords and password policies.

Only privileged users (such as `root`) can read this file.

---

## 29. What is the difference between `grep` and `find`?

| grep | find |
|------|------|
| Searches inside file contents | Searches for files and directories |
| Searches text | Searches paths |

Examples:

```bash
grep "error" log.txt
```

```bash
find /home -name "*.txt"
```

---

## 30. What is the difference between absolute path and relative path?

### Absolute Path

Starts from the root directory (`/`).

Example:

```bash
/home/kartik/Documents/file.txt
```

### Relative Path

Starts from the current working directory.

Example:

```bash
Documents/file.txt
```
