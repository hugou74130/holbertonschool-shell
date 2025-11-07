<p align="center">
  <a href="https://github.com/hugou74130/holbertonschool-shell/tree/main/permissions" rel="noopener">
 <img width=400px height=200px src="https://image.noelshack.com/fichiers/2025/45/3/1762375260-gemini-generated-image-602ke1602ke1602k.png" alt="Project logo"></a>
</p>

<h3 align="center">Permissions - File Access Control and Ownership in Unix/Linux</h3>

<div align="center">

[![Status](https://img.shields.io/badge/status-active-success.svg)]()
[![GitHub Issues](https://img.shields.io/github/issues/hugou74130/holbertonschool-shell.svg)](https://github.com/hugou74130/holbertonschool-shell/issues)
[![GitHub Pull Requests](https://img.shields.io/github/issues-pr/hugou74130/holbertonschool-shell.svg)](https://github.com/hugou74130/holbertonschool-shell/pulls)

</div>

---

<p align="center"> Master file permissions, ownership, and access control in Unix/Linux systems.
    <br>
Learn to manage who can read, write, and execute files and directories, and how to change file ownership.
    <br> 
</p>

## 📝 Table of Contents
- [About](#about)
- [Getting Started](#getting_started)
- [Scripts](#scripts)
- [Usage](#usage)
- [Permission Concepts](#permissions_concepts)
- [chmod Guide](#chmod_guide)
- [chown and chgrp Guide](#owner_group_guide)
- [Built Using](#built_using)
- [Authors](#authors)
- [Acknowledgments](#acknowledgement)

## 🧐 About <a name = "about"></a>

The Permissions module teaches one of the most critical aspects of Unix/Linux system administration: file access control. You will learn how to manage file permissions (read, write, execute), change file ownership, and understand the security implications of different permission configurations.

Understanding permissions is essential for system security, preventing unauthorized access, enabling proper file sharing between users, and protecting critical system files. Every Unix/Linux administrator and developer must master these concepts.

## 🏁 Getting Started <a name = "getting_started"></a>

### Prerequisites

You will need:

```
- A Unix/Linux terminal (Ubuntu, macOS, WSL on Windows)
- Bash shell
- Understanding of basic shell commands
- Files to practice with (created during exercises)
```

### Setup

Clone the repository and navigate to the permissions folder:

```bash
git clone https://github.com/hugou74130/holbertonschool-shell.git
cd holbertonschool-shell/permissions
```

### Important Note

Some scripts may require elevated privileges (sudo). Use them carefully and understand the security implications.

## 📋 Scripts <a name = "scripts"></a>

### 0-iam_betty
Switches the current user to the user `betty`. Demonstrates user switching.

```bash
bash 0-iam_betty
# Changes current user to betty (if password is provided)
# su betty
```

**Commands used:** `su` (switch user)

**What it teaches:**
- Switching between user accounts
- Understanding multi-user systems
- The `su` command and its usage

**Security note:** `su` without `-` doesn't load the user's environment fully. Use `su -` or `su - betty` for proper login.

---

### 1-who_am_i
Displays the username of the current user. Shows which user is currently logged in.

```bash
bash 1-who_am_i
# Output: username (the currently logged-in user)
```

**Commands used:** `whoami` or `id -un`

**What it teaches:**
- Identifying the current user
- Understanding user identity
- Commands: `whoami`, `id`, `whoami`

---

### 2-groups
Displays all groups that the current user belongs to. Shows group membership.

```bash
bash 2-groups
# Output: group1 group2 group3 (user's groups)
```

**Commands used:** `groups`

**What it teaches:**
- Understanding user groups
- Group membership and roles
- The `groups` command

---

### 3-new_owner
Changes the owner of a file named `hello` to the user `betty`. Demonstrates the `chown` command.

```bash
bash 3-new_owner
# Changes owner of 'hello' file to betty
# chown betty hello
```

**Commands used:** `chown`

**What it teaches:**
- Changing file ownership
- The `chown` command syntax
- Understanding file ownership
- Permission to use `chown` (usually requires root)

---

### 4-empty
Creates an empty file named `hello`. Demonstrates file creation.

```bash
bash 4-empty
# Creates empty file: hello
# touch hello
```

**Commands used:** `touch`

**What it teaches:**
- Creating empty files
- The `touch` command
- File creation as foundation for permission exercises

---

### 5-execute
Adds execute permission for the owner of a file named `hello`. Makes a file executable.

```bash
bash 5-execute
# chmod u+x hello
# Adds execute permission for owner
```

**Commands used:** `chmod u+x`

**What it teaches:**
- Adding execute permission
- Symbolic chmod notation (u+x)
- Understanding what execute permission means
- Making scripts executable

---

### 6-multiple_permissions
Adds multiple permissions to a file: owner can read and execute, group can read and execute, others can read only.

```bash
bash 6-multiple_permissions
# chmod 755 hello
# Owner: rwx, Group: r-x, Others: r-x
```

**Commands used:** `chmod 755` or `chmod u+rx,g+rx,o+r`

**What it teaches:**
- Setting multiple permissions at once
- Octal notation for permissions
- Common permission pattern: 755
- Understanding permission combinations

---

### 7-everybody
Adds execute permission for everyone (owner, group, and others) to a file.

```bash
bash 7-everybody
# chmod ugo+x hello
# or chmod a+x hello
# Everyone can execute the file
```

**Commands used:** `chmod a+x` or `chmod ugo+x`

**What it teaches:**
- Adding permissions for all users
- The `a` (all) operator in chmod
- When to make files executable for everyone
- Security considerations of open permissions

---

### 8-James_Bond
Sets specific permissions: owner has no permissions, group has no permissions, others have all permissions (0007).

```bash
bash 8-James_Bond
# chmod 007 hello
# Owner: ---, Group: ---, Others: rwx
```

**Commands used:** `chmod 007`

**What it teaches:**
- Understanding restrictive permission patterns
- Others-only access scenario
- Security risks of open "others" permissions
- Unusual but valid permission combinations

---

### 9-John_Doe
Sets permissions to 753: owner has rwx, group has r-x, others have -wx.

```bash
bash 9-John_Doe
# chmod 753 hello
# Owner: rwx, Group: r-x, Others: -wx
```

**Commands used:** `chmod 753`

**What it teaches:**
- Mixed permission patterns
- Creating specific access scenarios
- Understanding asymmetric permissions
- Practical permission assignment

---

### 10-mirror_permissions
Copies permissions from one file to another. If file `hello` has certain permissions, `olleh` gets the same permissions.

```bash
bash 10-mirror_permissions
# chmod --reference=hello olleh
# Copies all permissions from hello to olleh
```

**Commands used:** `chmod --reference=source destination`

**What it teaches:**
- Copying permissions between files
- The `--reference` option of chmod
- Batch permission application
- Practical permission management

---

### 11-directories_permissions
Changes permissions for all directories recursively, making them readable and executable but not writable for everyone.

```bash
bash 11-directories_permissions
# chmod -R a+rX . (or similar)
# Adds read and execute to all directories
```

**Commands used:** `chmod -R a+rX`

**What it teaches:**
- Recursive permission changes
- The `-R` flag for chmod
- The capital `X` (execute only for directories)
- Directory-specific permissions
- When to apply permissions recursively

---

### 12-directory_permissions
Changes permissions of a single directory, typically making it rwxr-x--- (750).

```bash
bash 12-directory_permissions
# chmod 750 my_dir
# Directory: owner rwx, group r-x, others ---
```

**Commands used:** `chmod 750`

**What it teaches:**
- Setting directory-specific permissions
- Common directory permission pattern: 750
- Directory vs. file permission considerations
- Protecting directory contents

---

### 13-change_group
Changes the group ownership of a file named `hello` to a specified group.

```bash
bash 13-change_group
# chgrp school hello
# Changes group owner to 'school'
```

**Commands used:** `chgrp`

**What it teaches:**
- Changing group ownership
- The `chgrp` command
- Understanding group-based access control
- Managing group membership permissions

---

### 14-change_owner_and_group
Changes both the owner and group of a file in a single command.

```bash
bash 14-change_owner_and_group
# chown betty:school hello
# Changes owner to betty, group to school
```

**Commands used:** `chown user:group` or `chown user:group`

**What it teaches:**
- Changing both owner and group simultaneously
- The colon syntax in chown
- Efficient permission management
- Understanding owner and group roles

---

### 15-symbolic_link_permissions
Changes permissions of a symbolic link itself (not the target file). Demonstrates `chmod -h` or `chmod -L`.

```bash
bash 15-symbolic_link_permissions
# chmod -h 777 _hello (if _hello is a symlink)
# Changes symlink permissions, not target
```

**Commands used:** `chmod -h` (don't follow symlinks)

**What it teaches:**
- Symbolic link permission handling
- The `-h` option to affect symlinks
- Difference between symlink and target permissions
- Advanced permission scenarios

---

### 16-if_only
Changes the owner of a file only if it's currently owned by a specific user. Conditional permission change.

```bash
bash 16-if_only
# chown --from=old_owner new_owner file
# Changes owner only if currently owned by old_owner
```

**Commands used:** `chown --from=`

**What it teaches:**
- Conditional ownership changes
- The `--from=` option
- Safe permission modifications
- Batch ownership changes with conditions

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

# Method 3: View script first
cat script_name
bash script_name
```

### Checking File Permissions

```bash
# View detailed permissions
ls -l filename
ls -ld directory

# View permissions in octal
stat filename

# Example output:
# -rw-r--r-- 1 user group 1024 Dec 15 10:30 filename
# ^--- permission bits
#  ^-- hard link count
#      ^-- owner
#          ^-- group
#              ^-- size
```

### Practical Examples

```bash
# Make a file executable
chmod +x script.sh

# Give full permissions to owner, read to group and others
chmod 744 file.txt

# Remove write permission for everyone
chmod a-w file.txt

# Give group write permission
chmod g+w file.txt

# Change owner and group
chown user:group file.txt

# Recursively change permissions in directory
chmod -R 755 /path/to/directory

# Change permissions of symlinks only
chmod -h 777 symlink_name
```

### Learning Path

Follow this recommended order:

1. Understand user concepts (`0-iam_betty`, `1-who_am_i`, `2-groups`)
2. Learn basic file operations (`4-empty`)
3. Start with simple permissions (`5-execute`, `7-everybody`)
4. Master octal notation (`6-multiple_permissions`, `8-James_Bond`, `9-John_Doe`)
5. Apply advanced techniques (`10-mirror_permissions`, `11-directories_permissions`)
6. Learn ownership changes (`3-new_owner`, `13-change_group`, `14-change_owner_and_group`)
7. Explore advanced scenarios (`15-symbolic_link_permissions`, `16-if_only`)

## 🔐 Permission Concepts <a name = "permissions_concepts"></a>

### Understanding Permission Bits

When you run `ls -l`, the first part shows permissions:

```
-rw-r--r-- 1 user group 1024 date filename
^   ^  ^  ^
|   |  |  +-- Others permissions (last 3 bits)
|   |  +----- Group permissions (middle 3 bits)
|   +-------- Owner/User permissions (first 3 bits)
+----------- File type (- for file, d for directory, l for link)
```

### Permission Types

| Symbol | Value | Meaning |
|--------|-------|---------|
| `r` | 4 | Read - View file contents or list directory |
| `w` | 2 | Write - Modify file or create/delete in directory |
| `x` | 1 | Execute - Run file as program or access directory |
| `-` | 0 | No permission |

### Permission Categories

| Category | Symbol | Meaning |
|----------|--------|---------|
| Owner/User | `u` | The file owner |
| Group | `g` | Members of the file's group |
| Others | `o` | Everyone else |
| All | `a` | Owner, group, and others |

### Common Permission Numbers

| Number | Binary | Permissions | Use Case |
|--------|--------|-------------|----------|
| 777 | 111 111 111 | rwx rwx rwx | Full access for everyone (use cautiously!) |
| 755 | 111 101 101 | rwx r-x r-x | Owner full, others read+execute (common for directories) |
| 750 | 111 101 000 | rwx r-x --- | Owner full, group read, others nothing |
| 644 | 110 100 100 | rw- r-- r-- | Owner write, group and others read-only (common for files) |
| 640 | 110 100 000 | rw- r-- --- | Owner and group read, others nothing |
| 700 | 111 000 000 | rwx --- --- | Owner full, others nothing (private files) |
| 600 | 110 000 000 | rw- --- --- | Owner read+write, others nothing |
| 400 | 100 000 000 | r-- --- --- | Owner read-only |

### File vs Directory Permissions

| Type | r (read) | w (write) | x (execute) |
|------|----------|----------|------------|
| **File** | View contents | Modify file | Run program |
| **Directory** | List contents | Create/delete files | Enter directory |

---

## 🔨 chmod Guide <a name = "chmod_guide"></a>

### Symbolic Method

```bash
# Add permissions
chmod u+x file           # Owner execute
chmod g+w file           # Group write
chmod o+r file           # Others read
chmod a+x file           # All execute

# Remove permissions
chmod u-x file           # Remove owner execute
chmod g-w file           # Remove group write

# Set exact permissions
chmod u=rwx file         # Owner exactly rwx
chmod g=rx file          # Group exactly rx
chmod o= file            # Others nothing
```

### Octal Method

```bash
# Set exact permissions using numbers
chmod 644 file           # rw-r--r--
chmod 755 file           # rwxr-xr-x
chmod 700 file           # rwx------
chmod 600 file           # rw-------

# Multiple files
chmod 755 file1 file2 file3

# Recursively
chmod -R 755 /path
```

### Special Permissions

```bash
# Setuid (run as owner)
chmod 4755 file          # setuid + rwxr-xr-x

# Setgid (run as group)
chmod 2755 file          # setgid + rwxr-xr-x

# Sticky bit (only owner can delete)
chmod 1755 directory     # sticky + rwxr-xr-x
```

---

## 👥 chown and chgrp Guide <a name = "owner_group_guide"></a>

### chown - Change Owner

```bash
# Change owner
chown newuser file

# Change owner and group
chown newuser:newgroup file

# Change owner recursively
chown -R newuser:newgroup /path

# Change only if currently owned by specific user
chown --from=olduser newuser file
```

### chgrp - Change Group

```bash
# Change group
chgrp newgroup file

# Change group recursively
chgrp -R newgroup /path
```

### Practical Scenarios

```bash
# Web server files (usually apache or www-data user)
chown -R www-data:www-data /var/www/html
chmod -R 755 /var/www/html

# User home directory
chown -R user:user /home/user
chmod -R 700 /home/user

# Shared project directory
chown -R :developers /opt/project
chmod -R 770 /opt/project
```

---

## 🔑 Security Best Practices <a name = "security"></a>

### Principle of Least Privilege

- Grant only necessary permissions
- Remove default world-readable/writable permissions
- Regularly audit file permissions

### Common Mistakes

```bash
# DON'T DO THIS - World writable!
chmod 777 file

# DON'T DO THIS - Everyone can execute
chmod 755 data_file.csv

# Better alternatives:
chmod 644 file              # rw-r--r--
chmod 755 script.sh         # rwxr-xr-x (for executables only)
chmod 700 sensitive_data    # rwx------ (private files)
```

### Sensitive File Permissions

```bash
# Private keys - owner only
chmod 600 ~/.ssh/id_rsa
chmod 700 ~/.ssh

# System files - restrictive
chmod 640 /etc/shadow
chmod 755 /etc/passwd

# Configuration files
chmod 640 /etc/database.conf
```

---

## ⛏️ Built Using <a name = "built_using"></a>

- [Bash Shell](https://www.gnu.org/software/bash/) - Command interpreter
- [chmod](https://linux.die.net/man/1/chmod) - Change file permissions
- [chown](https://linux.die.net/man/1/chown) - Change file owner
- [chgrp](https://linux.die.net/man/1/chgrp) - Change group owner
- [Linux](https://www.linux.org/) - Operating system

## ✍️ Authors <a name = "authors"></a>

- [@hugou74130](https://github.com/hugou74130) - Complete work

See also the list of [contributors](https://github.com/hugou74130/holbertonschool-shell/contributors) who participated in this project.

## 📚 Additional Resources <a name = "resources"></a>

- [Linux Permissions Explained](https://www.linux.com/training-tutorials/linux-permissions-explained-7-types-permissions-linux-explained/)
- [chmod Manual](https://linux.die.net/man/1/chmod)
- [chown Manual](https://linux.die.net/man/1/chown)
- [Advanced Bash Scripting Guide - File Permissions](https://www.tldp.org/LDP/abs/html/fprefix.html)
- [umask and Permission Defaults](https://linux.die.net/man/2/umask)

## 🎉 Acknowledgements <a name = "acknowledgement"></a>

- Holberton School for the curriculum and educational projects
- The Linux community for developing robust permission systems
- System administrators everywhere for emphasizing security best practices
- All learners using this resource to master file permissions and access control
