<p align="center">
  <a href="https://github.com/hugou74130/holbertonschool-shell" rel="noopener">
 <img width=400px height=200px src="https://image.noelshack.com/fichiers/2025/45/3/1762375260-gemini-generated-image-602ke1602ke1602k.png" alt="Project logo"></a>
</p>

<h3 align="center">Holberton School Shell Projects</h3>

<div align="center">

[![Status](https://img.shields.io/badge/status-active-success.svg)]()
[![GitHub Issues](https://img.shields.io/github/issues/hugou74130/holbertonschool-shell.svg)](https://github.com/hugou74130/holbertonschool-shell/issues)
[![GitHub Pull Requests](https://img.shields.io/github/issues-pr/hugou74130/holbertonschool-shell.svg)](https://github.com/hugou74130/holbertonschool-shell/pulls)

</div>

---

<p align="center"> This repository brings together my progress and solutions for <b>shell scripting (Bash)</b> projects completed as part of the Holberton School curriculum.
    <br>
Each folder represents a project or module, focused on learning basic commands, permissions, redirections, and other fundamental Unix concepts.
    <br> 
</p>

## 📝 Table of Contents
- [About](#about)
- [Project Structure](#project_structure)
- [Usage](#usage)
- [Built Using](#built_using)
- [Authors](#authors)
- [Acknowledgments](#acknowledgement)

## 🧐 About <a name = "about"></a>

This repository contains my work for the Shell modules at Holberton School. Rather than a single large application, it is a collection of scripts and solutions to small exercises.

The objective is to master the fundamentals of the Bash shell, from simple navigation to permission manipulation and stream redirections. These skills form the foundation for working effectively in Unix/Linux environments and writing efficient shell scripts.

## 🏁 Project Structure <a name = "project_structure"></a>

The repository is organized by learning modules. There is **no installation** required, as this is not a single software package. It is a collection of scripts for reference and learning.

Here is a description of the main folders:

### **basics**

This module focuses on the most elementary shell commands (`ls`, `cd`, `pwd`, `mkdir`, etc.) and navigation within the file system. You will learn how to explore directories, view file contents, create and delete files and folders.

Key concepts:
- Directory navigation and listing
- File and folder creation
- Understanding the file system hierarchy
- Basic file operations

### **permissions**

This module covers managing rights and permissions on files and folders (`chmod`, `chown`, `chgrp`). Understanding file permissions is crucial for security and proper access control in multi-user environments.

Key concepts:
- Read, write, and execute permissions
- Changing file ownership
- Understanding user and group permissions
- Using octal notation for permissions
- Special permissions (setuid, setgid, sticky bit)

### **io_redirections_and_filters**

This module is centered on input/output redirections (`<`, `>`, `>>`, `|`) and text filters (`grep`, `sed`, `sort`). Learn how to combine commands powerfully to process and transform data.

Key concepts:
- Standard input, output, and error streams
- Output redirection and appending
- Input redirection
- Piping commands together
- Text processing with grep, sed, awk
- Sorting and unique operations

### **init_files_variables_and_expansions**

This module explores initialization files, environment variables, aliases, and expansions. Understand how to customize your shell environment and write more sophisticated scripts.

Key concepts:
- Shell initialization files (.bashrc, .bash_profile)
- Environment variables and local variables
- Variable expansion and substitution
- Aliases for command shortcuts
- Command substitution
- Arithmetic expansion
- Brace expansion

## 🎈 Usage <a name="usage"></a>

Each folder (for example `basics`, `permissions`) is a standalone project. To explore:

1. Navigate to the folder that interests you
2. Read the script files to see the solution to a given exercise
3. You can run most scripts directly in a Bash terminal

### Running Scripts

To execute a shell script:

```bash
# Method 1: Run directly with bash
bash script_name.sh

# Method 2: Make executable and run
chmod +x script_name.sh
./script_name.sh

# Method 3: Source the script (loads functions into current shell)
source script_name.sh
```

### Example Workflow

```bash
# Clone the repository
git clone https://github.com/hugou74130/holbertonschool-shell.git
cd holbertonschool-shell

# Explore the basics folder
cd basics
ls

# Read a script to understand the solution
cat 0-current_working_directory.sh

# Execute it
bash 0-current_working_directory.sh
```

## 🔧 Key Concepts Covered <a name = "key_concepts"></a>

### File System Navigation
- `pwd` - Print working directory
- `cd` - Change directory
- `ls` - List directory contents
- `mkdir` - Create directories
- `rmdir` - Remove directories

### File Operations
- `touch` - Create empty files
- `cp` - Copy files
- `mv` - Move/rename files
- `rm` - Remove files
- `cat` - Display file contents

### Permissions
- `chmod` - Change file permissions
- `chown` - Change file owner
- `chgrp` - Change file group
- `ls -l` - View detailed permissions

### Input/Output and Filters
- `>` and `>>` - Output redirection
- `<` - Input redirection
- `|` - Piping between commands
- `grep` - Search text patterns
- `sed` - Stream editor
- `awk` - Text processing language
- `sort` - Sort lines
- `uniq` - Remove duplicates

### Variables and Expansions
- Variable declaration and usage
- Environment variables
- Command substitution
- Arithmetic operations
- Brace expansion
- Glob patterns

## 📚 Learning Resources <a name = "resources"></a>

- [GNU Bash Manual](https://www.gnu.org/software/bash/manual/)
- [ShellCheck](https://www.shellcheck.net/) - Shell script linter
- [Linux Command Reference](https://linux.die.net/man/)
- [The Linux Command Line](http://linuxcommand.org/)

## ⛏️ Built Using <a name = "built_using"></a>

- [Shell (Bash)](https://www.gnu.org/software/bash/) - The primary scripting language used
- [Ubuntu](https://ubuntu.com/) - Development and testing environment
- [Vim / Emacs](https://www.vim.org/) - Text editors used for development

## ✍️ Authors <a name = "authors"></a>

- [@hugou74130](https://github.com/hugou74130) - Complete work

See also the list of [contributors](https://github.com/hugou74130/holbertonschool-shell/contributors) who participated in this project.

## 🎉 Acknowledgements <a name = "acknowledgement"></a>

- A big thank you to **Holberton School** for the curriculum and challenging projects
- The Linux and Bash community for creating powerful tools
- All fellow learners who collaborate and share knowledge
- The open-source community for inspiration and support


