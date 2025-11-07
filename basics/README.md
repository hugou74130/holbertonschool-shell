<p align="center">
  <a href="https://github.com/hugou74130/holbertonschool-shell/tree/main/basics" rel="noopener">
 <img width=400px height=200px src="https://image.noelshack.com/fichiers/2025/45/3/1762375260-gemini-generated-image-602ke1602ke1602k.png" alt="Project logo"></a>
</p>

<h3 align="center">Shell Basics - Fundamentals of Shell Navigation and File Management</h3>

<div align="center">

[![Status](https://img.shields.io/badge/status-active-success.svg)]()
[![GitHub Issues](https://img.shields.io/github/issues/hugou74130/holbertonschool-shell.svg)](https://github.com/hugou74130/holbertonschool-shell/issues)
[![GitHub Pull Requests](https://img.shields.io/github/issues-pr/hugou74130/holbertonschool-shell.svg)](https://github.com/hugou74130/holbertonschool-shell/pulls)

</div>

---

<p align="center"> Master the fundamentals of shell navigation, file management, and basic Linux commands.
    <br>
This project covers essential commands for working with the file system in Unix/Linux environments.
    <br> 
</p>

## 📝 Table of Contents
- [About](#about)
- [Getting Started](#getting_started)
- [Scripts](#scripts)
- [Usage](#usage)
- [Key Commands](#key_commands)
- [Built Using](#built_using)
- [Authors](#authors)
- [Acknowledgments](#acknowledgement)

## 🧐 About <a name = "about"></a>

The Shell Basics module is your introduction to working with the command-line shell (Bash). You will learn the fundamental commands needed to navigate the file system, list files, create and manage directories, and understand how to interact with the shell environment.

These are the essential skills that every developer and system administrator must know. By mastering these basics, you'll be able to work efficiently in any Unix/Linux environment and build more complex shell scripts later.

## 🏁 Getting Started <a name = "getting_started"></a>

### Prerequisites

You will need:

```
- A Unix/Linux terminal (Ubuntu, macOS, WSL on Windows)
- Bash shell
- Basic command line knowledge
```

### Setup

Clone the repository and navigate to the basics folder:

```bash
git clone https://github.com/hugou74130/holbertonschool-shell.git
cd holbertonschool-shell/basics
```

## 📋 Scripts <a name = "scripts"></a>

### 0-current_working_directory
Prints the absolute pathname of the current working directory. Your first introduction to the `pwd` command.

```bash
bash 0-current_working_directory
# Output: /home/user/path/to/current/directory
```

**Commands used:** `pwd`

**What it teaches:** Understanding your location in the file system hierarchy

---

### 1-listit
Lists the contents of the current directory. Introduction to the `ls` command.

```bash
bash 1-listit
# Output: file1.txt  file2.sh  directory1
```

**Commands used:** `ls`

**What it teaches:** Viewing what files and directories exist in the current location

---

### 2-bring_me_home
Changes the current working directory to the user's home directory. Demonstrates the `cd` command with no arguments.

```bash
bash 2-bring_me_home
# Changes to home directory (~)
```

**Commands used:** `cd` or `cd ~`

**What it teaches:** Navigating to your home directory from anywhere

---

### 3-listfiles
Lists all files and directories with their details in long format. Uses `ls -la` to show detailed information.

```bash
bash 3-listfiles
# Output: drwxr-xr-x  owner  group  size  date  filename
```

**Commands used:** `ls -la`

**What it teaches:** Understanding file permissions, ownership, size, and dates

---

### 4-listmorefiles
Lists all files including hidden ones, with additional formatting. Displays hidden files (starting with `.`).

```bash
bash 4-listmorefiles
# Includes files like .bashrc, .bash_profile, .hidden
```

**Commands used:** `ls -lha`

**What it teaches:** Hidden files in Unix/Linux systems and viewing them

---

### 5-listfilesdigitonly
Lists files with detailed information but displays numeric user and group IDs instead of names.

```bash
bash 5-listfilesdigitonly
# Output: -rw-r--r-- 1000 1000 1024 date filename
```

**Commands used:** `ls -ln` or `ls -lna`

**What it teaches:** Understanding numeric UID/GID representations

---

### 6-firstdirectory
Creates a directory named `my_first_directory` in the `/tmp` directory.

```bash
bash 6-firstdirectory
# Creates /tmp/my_first_directory
```

**Commands used:** `mkdir`

**What it teaches:** Creating new directories using `mkdir`

---

### 7-movethatfile
Moves a file named `betty` from `/tmp` to `/tmp/my_first_directory`.

```bash
bash 7-movethatfile
# Moves /tmp/betty to /tmp/my_first_directory/betty
```

**Commands used:** `mv`

**What it teaches:** Moving and renaming files with `mv`

---

### 8-firstdelete
Deletes the file `betty` from `/tmp/my_first_directory`.

```bash
bash 8-firstdelete
# Removes /tmp/my_first_directory/betty
```

**Commands used:** `rm`

**What it teaches:** Deleting files safely and permanently

---

### 9-firstdirdeletion
Removes the entire directory `/tmp/my_first_directory`.

```bash
bash 9-firstdirdeletion
# Deletes /tmp/my_first_directory and its contents
```

**Commands used:** `rm -rf` or `rmdir`

**What it teaches:** Removing directories and their contents

---

### 10-back
Changes the current working directory to the previous directory (the one you were in before the last `cd`).

```bash
bash 10-back
# Changes to the previous directory
```

**Commands used:** `cd -`

**What it teaches:** Navigating between directories efficiently

---

### 11-lists
Lists all files (including hidden) in multiple directories: current, parent directory, and `/boot`.

```bash
bash 11-lists
# Output: Files from current directory, parent directory, and /boot
```

**Commands used:** `ls -la . .. /boot`

**What it teaches:** Listing contents of multiple directories in one command

---

### 12-file_type
Prints the type of a file located at `/tmp/iamafile`. Determines if it's a directory, regular file, or other type.

```bash
bash 12-file_type
# Output: /tmp/iamafile: ASCII text (or other type)
```

**Commands used:** `file`

**What it teaches:** Using the `file` command to determine file types

---

### 13-symbolic_link
Creates a symbolic (soft) link named `__ls__` that points to `/bin/ls`.

```bash
bash 13-symbolic_link
# Creates symbolic link: __ls__ -> /bin/ls
```

**Commands used:** `ln -s`

**What it teaches:** Creating symbolic links and understanding shortcuts to files

---

### 14-copy_html
Copies all HTML files (files ending with `.html`) from the current directory to the parent directory, but only if they don't already exist there.

```bash
bash 14-copy_html
# Copies *.html files to parent directory
```

**Commands used:** `cp` with globbing patterns

**What it teaches:** Copying multiple files matching a pattern

---

### 15-lets_move
Moves all files starting with an uppercase letter from the current directory to `/tmp/u`.

```bash
bash 15-lets_move
# Moves files like: FILENAME, Alpha, Beta to /tmp/u
```

**Commands used:** `mv` with pattern matching

**What it teaches:** Moving files based on naming patterns

---

### 16-clean_emacs
Deletes all files ending with `~` (backup files created by Emacs editor).

```bash
bash 16-clean_emacs
# Removes all *~ files
```

**Commands used:** `rm` with wildcard

**What it teaches:** Cleaning up backup and temporary files

---

### 16-clean_emacs~
This is a backup file (notice the `~` at the end). It's created by text editors like Emacs or Vi.

---

### 17-tree
Lists the directory tree structure, showing all files and subdirectories recursively. Uses `tree` command or `ls` recursively.

```bash
bash 17-tree
# Output: Directory structure with indentation showing hierarchy
```

**Commands used:** `tree` or `ls -R`

**What it teaches:** Viewing the complete directory structure

---

## 🎈 Usage <a name="usage"></a>

### Running Scripts

To execute any script:

```bash
# Method 1: Run with bash
bash script_name

# Method 2: Make executable and run
chmod +x script_name
./script_name

# Method 3: View the script first
cat script_name
# Then run it
bash script_name
```

### Learning Path

It's recommended to follow the scripts in order:

1. Start with `0-current_working_directory` to understand `pwd`
2. Move through navigation (`1-listit`, `2-bring_me_home`, `10-back`)
3. Learn file operations (`3-listfiles` through `5-listfilesdigitonly`)
4. Practice directory creation and manipulation (`6-firstdirectory` through `9-firstdirdeletion`)
5. Master advanced operations (`11-lists` through `17-tree`)

## 🔑 Key Commands <a name = "key_commands"></a>

### Navigation Commands

| Command | Purpose | Example |
|---------|---------|---------|
| `pwd` | Print Working Directory | `pwd` |
| `cd` | Change Directory | `cd /home/user` |
| `cd ~` | Go to Home Directory | `cd ~` |
| `cd -` | Go to Previous Directory | `cd -` |
| `cd ..` | Go to Parent Directory | `cd ..` |

### File Listing Commands

| Command | Purpose | Example |
|---------|---------|---------|
| `ls` | List Files | `ls` |
| `ls -l` | List with Details | `ls -l` |
| `ls -a` | List All (including hidden) | `ls -a` |
| `ls -la` | List All with Details | `ls -la` |
| `ls -lh` | List with Human-Readable Sizes | `ls -lh` |
| `ls -R` | List Recursively | `ls -R` |

### File and Directory Operations

| Command | Purpose | Example |
|---------|---------|---------|
| `mkdir` | Make Directory | `mkdir my_dir` |
| `rmdir` | Remove Empty Directory | `rmdir my_dir` |
| `rm` | Remove Files | `rm file.txt` |
| `rm -r` | Remove Directory Recursively | `rm -r my_dir` |
| `cp` | Copy Files | `cp file1 file2` |
| `mv` | Move/Rename Files | `mv old_name new_name` |
| `touch` | Create Empty File | `touch newfile.txt` |

### File Information Commands

| Command | Purpose | Example |
|---------|---------|---------|
| `file` | Determine File Type | `file document.txt` |
| `ln -s` | Create Symbolic Link | `ln -s /bin/ls my_ls` |
| `tree` | Show Directory Tree | `tree` |

## 🔐 Understanding File Permissions <a name = "permissions"></a>

When you run `ls -l`, you see output like:

```
-rw-r--r-- 1 user group 1024 Dec 15 10:30 file.txt
```

Breaking this down:
- `-rw-r--r--`: Permissions (first char is file type, next 9 are permissions)
- `1`: Number of links
- `user`: File owner
- `group`: Group owner
- `1024`: File size in bytes
- `Dec 15 10:30`: Date and time modified
- `file.txt`: Filename

**Permission breakdown:**
- `r` (read): 4
- `w` (write): 2
- `x` (execute): 1

First 3 characters (after `-`) = owner permissions
Next 3 = group permissions
Last 3 = others permissions

## 💡 Tips and Tricks <a name = "tips"></a>

- Use `Tab` for auto-completion of file and directory names
- Use `Ctrl+C` to stop a running command
- Use `Ctrl+L` to clear the screen
- Use `history` to see previously executed commands
- Use `!number` to repeat a command from history
- Use `*` as wildcard for any characters
- Use `?` as wildcard for a single character

## ⛏️ Built Using <a name = "built_using"></a>

- [Bash Shell](https://www.gnu.org/software/bash/) - Command-line shell
- [Linux](https://www.linux.org/) - Operating system
- [GNU Coreutils](https://www.gnu.org/software/coreutils/) - Core utilities

## ✍️ Authors <a name = "authors"></a>

- [@hugou74130](https://github.com/hugou74130) - Complete work

See also the list of [contributors](https://github.com/hugou74130/holbertonschool-shell/contributors) who participated in this project.

## 📚 Additional Resources <a name = "resources"></a>

- [GNU Bash Manual](https://www.gnu.org/software/bash/manual/)
- [Linux Command Line Basics](https://ubuntu.com/tutorials/command-line-for-beginners)
- [The Linux Command Line](http://linuxcommand.org/)
- [Bash Cheat Sheet](https://devhints.io/bash)

## 🎉 Acknowledgements <a name = "acknowledgement"></a>

- Holberton School for the curriculum and educational projects
- The Linux and Unix communities for creating these powerful tools
- All learners using this resource to improve their shell skills
