# **Introduction to CLI and Terminal**

---

## **1. What is CLI?**

**CLI** stands for **Command Line Interface**.

* It is a **text-based interface** where you type **commands** to communicate with the computer.
* Unlike GUI (Graphical User Interface) where you click icons and menus, CLI relies entirely on **text commands**.
* CLI interprets your commands and gives **textual output**.

**Example of CLI:**

```
C:\Users\Soumya> dir
```

This lists files and folders in the current directory.

**Advantages of CLI:**

1. Faster and more powerful for advanced tasks.
2. Can automate repetitive tasks using scripts.
3. Requires less system resources than GUI.

**Disadvantages of CLI:**

1. Requires learning commands and syntax.
2. No visual interface, so it can be harder for beginners.

---

## **2. What is a Terminal?**

A **Terminal** is an **application/program** that provides access to a CLI.

* Think of it as a **window where you type commands**.
* Terminals allow you to communicate with the system using a shell (like **bash** on Linux/macOS or **cmd/powershell** on Windows).

**Popular terminals:**

* **Windows:** Command Prompt (CMD), PowerShell, Windows Terminal
* **Linux:** GNOME Terminal, Konsole, xterm
* **macOS:** Terminal app

**Example:**
Opening the terminal on Linux and typing:

```bash
ls -l
```

will list all files and folders in long format.

---

## **3. Shell vs Terminal vs CLI**

| Term         | Meaning                                                   | Example                           |
| ------------ | --------------------------------------------------------- | --------------------------------- |
| **CLI**      | Command Line Interface – the text-based system itself     | `ls`, `dir`                       |
| **Terminal** | Application/program that lets you type commands           | GNOME Terminal, CMD, Terminal app |
| **Shell**    | Program that interprets commands you type in the terminal | bash, zsh, PowerShell             |

**Analogy:**

* CLI = The language you speak
* Shell = The interpreter that understands the language
* Terminal = The “window” where you speak

---

## **4. Why Use CLI/Terminal?**

1. **Efficiency:** Do tasks faster than GUI for advanced operations.
2. **Automation:** Run scripts to automate repetitive tasks.
3. **Remote Access:** Connect to servers via SSH and manage systems remotely.
4. **Powerful Tools:** Use advanced tools like `grep`, `awk`, `sed`, `git`, `docker`.

---


# **Linux Commands: (Basic → Advanced)**

---

## **1. Navigation & Directory Commands**

| Command | Syntax                | Example           | Use / Notes                                                       |
| ------- | --------------------- | ----------------- | ----------------------------------------------------------------- |
| `pwd`   | `pwd`                 | `pwd`             | Shows current directory path.                                     |
| `ls`    | `ls [options] [path]` | `ls -l /home`     | Lists files/folders. `-l` for long format, `-a` for hidden files. |
| `cd`    | `cd [directory]`      | `cd /home/user`   | Change directory. `cd ..` goes up.                                |
| `mkdir` | `mkdir foldername`    | `mkdir Test`      | Create a new directory.                                           |
| `rmdir` | `rmdir foldername`    | `rmdir Test`      | Remove empty directory.                                           |
| `tree`  | `tree [path]`         | `tree /home/user` | Shows directory structure in tree format.                         |

---

## **2. File Handling Commands**

| Command         | Syntax                | Example                         | Use / Notes                                           |
| --------------- | --------------------- | ------------------------------- | ----------------------------------------------------- |
| `touch`         | `touch filename`      | `touch file.txt`                | Create empty file or update timestamp.                |
| `cat`           | `cat filename`        | `cat file.txt`                  | View file contents.                                   |
| `more` / `less` | `more filename`       | `less file.txt`                 | View file content page by page.                       |
| `cp`            | `cp source dest`      | `cp file.txt /home/user/Backup` | Copy files or directories (`-r` for recursive).       |
| `mv`            | `mv source dest`      | `mv file.txt /home/user/Backup` | Move or rename files/directories.                     |
| `rm`            | `rm filename`         | `rm file.txt`                   | Delete file. Add `-r` for directories, `-f` to force. |
| `head`          | `head -n 10 filename` | `head -n 10 file.txt`           | Show first 10 lines of file.                          |
| `tail`          | `tail -n 10 filename` | `tail -n 10 file.txt`           | Show last 10 lines. `-f` to follow live logs.         |

---

## **3. Searching & Text Processing**

| Command  | Syntax                      | Example                              | Use / Notes                               |
| -------- | --------------------------- | ------------------------------------ | ----------------------------------------- |
| `grep`   | `grep "text" filename`      | `grep "error" log.txt`               | Search text inside files.                 |
| `find`   | `find path -name filename`  | `find /home -name file.txt`          | Search for files in directories.          |
| `locate` | `locate filename`           | `locate file.txt`                    | Quickly find files (requires `updatedb`). |
| `wc`     | `wc -l filename`            | `wc -l file.txt`                     | Count lines, words, characters.           |
| `cut`    | `cut -d"," -f1 file.csv`    | Extract specific columns.            |                                           |
| `sort`   | `sort filename`             | `sort file.txt`                      | Sort lines alphabetically/numerically.    |
| `uniq`   | `uniq filename`             | `uniq file.txt`                      | Remove duplicate consecutive lines.       |
| `awk`    | `awk '{print $1}' file.txt` | Advanced text processing.            |                                           |
| `sed`    | `sed 's/old/new/' file.txt` | Stream editor, modify text in files. |                                           |

---

## **4. File Permissions & Ownership**

| Command | Syntax                  | Example                    | Use / Notes                     |
| ------- | ----------------------- | -------------------------- | ------------------------------- |
| `chmod` | `chmod 755 file`        | `chmod 755 script.sh`      | Change file permissions.        |
| `chown` | `chown user:group file` | `chown root:root file.txt` | Change file owner/group.        |
| `ls -l` | `ls -l`                 | `ls -l file.txt`           | View permissions and ownership. |

---

## **5. System Information & Management**

| Command    | Syntax          | Example             | Use / Notes                                  |                         |
| ---------- | --------------- | ------------------- | -------------------------------------------- | ----------------------- |
| `uname`    | `uname -a`      | `uname -a`          | Show system/kernel info.                     |                         |
| `df`       | `df -h`         | `df -h`             | Show disk space usage (`-h` human-readable). |                         |
| `du`       | `du -sh folder` | `du -sh /home/user` | Show folder size.                            |                         |
| `top`      | `top`           | `top`               | Show running processes in real time.         |                         |
| `ps`       | `ps aux`        | `ps aux             | grep processname`                            | Show current processes. |
| `free`     | `free -h`       | `free -h`           | Show memory usage.                           |                         |
| `uptime`   | `uptime`        | `uptime`            | Show system running time.                    |                         |
| `who`      | `who`           | `who`               | List logged-in users.                        |                         |
| `hostname` | `hostname`      | `hostname`          | Show system name.                            |                         |

---

## **6. Networking Commands**

| Command      | Syntax                     | Example                            | Use / Notes                      |
| ------------ | -------------------------- | ---------------------------------- | -------------------------------- |
| `ping`       | `ping IP/host`             | `ping google.com`                  | Check connectivity.              |
| `ifconfig`   | `ifconfig`                 | `ifconfig`                         | Show network interfaces.         |
| `ip`         | `ip addr`                  | `ip addr`                          | Modern replacement for ifconfig. |
| `netstat`    | `netstat -tuln`            | `netstat -tuln`                    | Show listening ports.            |
| `traceroute` | `traceroute host`          | `traceroute google.com`            | Trace network path.              |
| `scp`        | `scp file user@host:/path` | Secure copy file to remote server. |                                  |
| `ssh`        | `ssh user@host`            | `ssh root@192.168.1.10`            | Secure shell to remote server.   |
| `wget`       | `wget URL`                 | Download files from internet.      |                                  |
| `curl`       | `curl URL`                 | Fetch data from web.               |                                  |

---

## **7. Package Management (Linux Distros)**

| Command   | Syntax                         | Example                         | Use / Notes |
| --------- | ------------------------------ | ------------------------------- | ----------- |
| `apt-get` | `sudo apt-get install package` | Ubuntu/Debian install software. |             |
| `yum`     | `sudo yum install package`     | RHEL/CentOS install software.   |             |
| `dpkg`    | `dpkg -i package.deb`          | Install .deb package.           |             |
| `rpm`     | `rpm -i package.rpm`           | Install .rpm package.           |             |

---

## **8. Archiving & Compression**

| Command  | Syntax                        | Example               | Use / Notes |
| -------- | ----------------------------- | --------------------- | ----------- |
| `tar`    | `tar -cvf archive.tar folder` | Create archive.       |             |
| `tar`    | `tar -xvf archive.tar`        | Extract archive.      |             |
| `gzip`   | `gzip file`                   | Compress file to .gz. |             |
| `gunzip` | `gunzip file.gz`              | Extract .gz file.     |             |
| `zip`    | `zip archive.zip file1 file2` | Create zip file.      |             |
| `unzip`  | `unzip archive.zip`           | Extract zip file.     |             |

---

## **9. Process Management**

| Command     | Syntax                | Example                             | Use / Notes                 |
| ----------- | --------------------- | ----------------------------------- | --------------------------- |
| `kill`      | `kill PID`            | `kill 1234`                         | Kill process by PID.        |
| `killall`   | `killall processname` | `killall firefox`                   | Kill all processes by name. |
| `jobs`      | `jobs`                | Show background jobs.               |                             |
| `fg` / `bg` | `fg %1`               | Bring background job to foreground. |                             |

---

## **10. Scripting & Automation**

| Command    | Syntax               | Example                    | Use / Notes |
| ---------- | -------------------- | -------------------------- | ----------- |
| `echo`     | `echo "Hello"`       | Print text to console.     |             |
| `export`   | `export VAR=value`   | Set environment variables. |             |
| `crontab`  | `crontab -e`         | Schedule recurring tasks.  |             |
| `bash`     | `bash script.sh`     | Run bash scripts.          |             |
| `chmod +x` | `chmod +x script.sh` | Make script executable.    |             |

---

## **11. Disk & Storage Management**

| Command  | Syntax              | Example                         | Use / Notes |
| -------- | ------------------- | ------------------------------- | ----------- |
| `mount`  | `mount device path` | Mount device to directory.      |             |
| `umount` | `umount path`       | Unmount device.                 |             |
| `lsblk`  | `lsblk`             | List block devices (disks).     |             |
| `fdisk`  | `sudo fdisk -l`     | List partitions / manage disks. |             |

---

## **12. Miscellaneous Useful Commands**

| Command    | Syntax              | Example                            | Use / Notes                     |
| ---------- | ------------------- | ---------------------------------- | ------------------------------- |
| `date`     | `date`              | Show current date & time.          |                                 |
| `cal`      | `cal`               | Show calendar.                     |                                 |
| `history`  | `history`           | Show previously executed commands. |                                 |
| `alias`    | `alias ll='ls -la'` | Create command shortcut.           |                                 |
| `uname -r` | `uname -r`          | Show kernel version.               |                                 |
| `uptime`   | `uptime`            | Show system uptime.                |                                 |
| `man`      | `man command`       | `man ls`                           | Show manual/help for a command. |

---

✅ **Tips for Linux Mastery**

1. Combine commands using `|` (pipe) to chain outputs.
   Example: `ps aux | grep firefox`
2. Redirect output using `>` (overwrite) or `>>` (append).
   Example: `ls > file.txt`
3. Use `Ctrl+C` to stop a running command.
4. `sudo` allows running commands as root/admin.

---

