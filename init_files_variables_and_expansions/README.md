<p align="center">
  <a href="https://github.com/hugou74130/holbertonschool-shell/tree/main/init_files_variables_and_expansions" rel="noopener">
 <img width=400px height=200px src="https://image.noelshack.com/fichiers/2025/45/3/1762375260-gemini-generated-image-602ke1602ke1602k.png" alt="Project logo"></a>
</p>

<h3 align="center">Init Files, Variables and Expansions - Advanced Shell Scripting</h3>

<div align="center">

[![Status](https://img.shields.io/badge/status-active-success.svg)]()
[![GitHub Issues](https://img.shields.io/github/issues/hugou74130/holbertonschool-shell.svg)](https://github.com/hugou74130/holbertonschool-shell/issues)
[![GitHub Pull Requests](https://img.shields.io/github/issues-pr/hugou74130/holbertonschool-shell.svg)](https://github.com/hugou74130/holbertonschool-shell/pulls)

</div>

---

<p align="center"> Master shell initialization files, environment variables, variable expansions, and advanced arithmetic operations in Bash.
    <br>
Learn how to customize your shell environment and write sophisticated shell scripts using expansions and substitutions.
    <br> 
</p>

## 📝 Table of Contents
- [About](#about)
- [Getting Started](#getting_started)
- [Scripts](#scripts)
- [Usage](#usage)
- [Key Concepts](#key_concepts)
- [Variable Types](#variable_types)
- [Built Using](#built_using)
- [Authors](#authors)
- [Acknowledgments](#acknowledgement)

## 🧐 About <a name = "about"></a>

The Init Files, Variables and Expansions module teaches advanced shell scripting concepts that form the foundation of powerful automation and system administration. You will learn how to work with variables, create aliases, use expansions for text transformation, and perform arithmetic calculations.

These skills enable you to write more sophisticated shell scripts, customize your environment, and manipulate data efficiently. Understanding initialization files, environment variables, and expansions is essential for becoming a proficient shell programmer.

## 🏁 Getting Started <a name = "getting_started"></a>

### Prerequisites

You will need:

```
- A Unix/Linux terminal (Ubuntu, macOS, WSL on Windows)
- Bash shell (version 4.0 or higher recommended)
- Basic understanding of shell basics
- Text editor (Vim, Nano, or your preferred editor)
```

### Setup

Clone the repository and navigate to the init_files_variables_and_expansions folder:

```bash
git clone https://github.com/hugou74130/holbertonschool-shell.git
cd holbertonschool-shell/init_files_variables_and_expansions
```

## 📋 Scripts <a name = "scripts"></a>

### 0-alias
Creates a command alias named `ls` that actually runs `rm *`. This script teaches how aliases work and how dangerous they can be if misused.

```bash
bash 0-alias
# Creates alias: alias ls='rm *'
```

**Commands used:** `alias`

**What it teaches:** 
- Creating command aliases
- How aliases override original commands
- Dangers of alias shadowing
- Alias syntax: `alias name='command'`

---

### 1-hello_you
Creates an alias that displays "hello user" where user is the current user. Uses the `$USER` environment variable.

```bash
bash 1-hello_you
# Output: hello user (where user is replaced with actual username)
```

**Commands used:** `alias`, `$USER` variable

**What it teaches:**
- Using environment variables in aliases
- Variable substitution in command strings
- Creating meaningful aliases

---

### 2-path
Adds `/action` directory to the beginning of the `PATH` variable so that executables in that directory are found first.

```bash
bash 2-path
# Prepends /action to PATH
```

**Commands used:** `export`, `PATH` variable

**What it teaches:**
- Understanding the PATH variable
- How the shell finds executable programs
- Modifying PATH to change command precedence
- Variable manipulation: `PATH="/action:$PATH"`

---

### 3-paths
Counts and prints the number of directories in the `PATH` variable.

```bash
bash 3-paths
# Output: 15 (or whatever number of directories are in PATH)
```

**Commands used:** `echo`, `tr`, `wc`, PATH parsing

**What it teaches:**
- Analyzing the PATH variable structure
- Splitting strings by delimiters
- Using command pipelines for text processing
- Counting elements in a colon-separated list

---

### 4-global_variables
Prints all environment variables (global variables). Shows the difference between local and global scope.

```bash
bash 4-global_variables
# Output: Lists all global variables like USER, HOME, SHELL, etc.
```

**Commands used:** `env` or `printenv`

**What it teaches:**
- Global vs. local variables
- Using `env` to display environment variables
- Common environment variables
- Understanding variable scope

---

### 5-local_variables
Prints all local variables (including global ones). Shows all variables defined in the current shell session.

```bash
bash 5-local_variables
# Output: Shows all variables in current shell
```

**Commands used:** `set`

**What it teaches:**
- Local variables and their scope
- Using `set` to display all variables
- Difference between `env` and `set`
- Variable creation and existence

---

### 6-create_local_variable
Creates a new local variable named `BEST` with value `School`. Demonstrates variable assignment in the shell.

```bash
bash 6-create_local_variable
# Creates: BEST=School
```

**Commands used:** Variable assignment

**What it teaches:**
- Creating local variables
- Variable naming conventions
- Variable scope (local to current shell)
- Using `=` for assignment (no spaces)

---

### 7-create_global_variable
Creates a new global variable named `BEST` with value `School` and exports it so child processes can access it.

```bash
bash 7-create_global_variable
# Creates and exports: BEST=School
```

**Commands used:** `export` command

**What it teaches:**
- Creating global (exported) variables
- The `export` command for variable promotion
- Making variables accessible to child processes
- Difference between local and exported variables

---

### 8-true_knowledge
Tests shell arithmetic and comparison. Demonstrates that 12+1 equals 13 without using calculators.

```bash
bash 8-true_knowledge
# Performs arithmetic: $(( 12 + 1 ))
```

**Commands used:** `$(( ))` arithmetic expansion

**What it teaches:**
- Arithmetic expansion syntax: `$(( expression ))`
- Basic arithmetic operations: +, -, *, /
- Testing mathematical expressions
- Integer arithmetic in Bash

---

### 9-divide_and_rule
Divides a number by another using shell arithmetic. Demonstrates the division operator and arithmetic in scripts.

```bash
bash 9-divide_and_rule
# Performs division: $(( number1 / number2 ))
```

**Commands used:** `$(( ))` arithmetic expansion

**What it teaches:**
- Division operation in shell arithmetic
- Integer division (no decimals)
- Using results of arithmetic in scripts
- Storing arithmetic results in variables

---

### 10-love_exponent_breath
Calculates exponentiation (raising a number to a power). Uses the exponentiation operator `**`.

```bash
bash 10-love_exponent_breath
# Performs exponentiation: $(( 2 ** 8 ))
# Output: 256
```

**Commands used:** `$(( ))` arithmetic expansion with `**` operator

**What it teaches:**
- Exponentiation operator: `**`
- Power calculations in shell scripts
- Practical uses of arithmetic expansion
- Complex numerical calculations

---

### 11-binary_to_decimal
Converts a binary number to its decimal equivalent. Demonstrates number base conversion in Bash.

```bash
bash 11-binary_to_decimal
# Converts binary 10010111 to decimal: $(( 2#10010111 ))
# Output: 151
```

**Commands used:** `$(( ))` with base prefix `base#number`

**What it teaches:**
- Number base conversion syntax: `base#number`
- Binary to decimal conversion
- Understanding different number systems
- Base notation in Bash arithmetic

---

### 12-combinations
Generates all possible combinations of two different single digits (0-9) and prints them separated by commas.

```bash
bash 12-combinations
# Output: 01, 02, 03, 04, 05, 06, 07, 08, 09, 10, 12, ...
```

**Commands used:** Nested loops, variable expansion

**What it teaches:**
- Nested loops in shell scripts
- Generating combinations
- String concatenation
- Loop control and conditional logic

---

### 13-print_float
Prints the result of a division with 2 decimal places precision.

```bash
bash 13-print_float
# Output: 3.14 (or similar, showing proper decimal formatting)
```

**Commands used:** `printf` or `echo` with formatting

**What it teaches:**
- Floating-point arithmetic approximation
- Using `printf` for formatted output
- Decimal precision formatting
- Rounding and display formatting

---

### 14-decimal_to_hexadecimal
Converts a decimal number to its hexadecimal (base 16) equivalent.

```bash
bash 14-decimal_to_hexadecimal
# Converts decimal 256 to hexadecimal: $(( 16#... ))
# Output: 100 (in hex) or using printf format
```

**Commands used:** `printf`, arithmetic expansion

**What it teaches:**
- Hexadecimal number system
- Decimal to hex conversion
- Using `printf` for base conversion
- Number system conversions in scripts

---

### 15-rot13
Implements ROT13 cipher, a simple letter substitution that replaces letters with the 13th letter after it in the alphabet.

```bash
bash 15-rot13
# Input: "Hello"
# Output: "Uryyb"
```

**Commands used:** `tr` (translate) command

**What it teaches:**
- The `tr` command for character translation
- Text transformation and substitution
- ROT13 algorithm understanding
- String manipulation techniques

---

### 16-odd
Prints every other line from input, displaying lines with odd line numbers (1, 3, 5, 7, etc.).

```bash
bash 16-odd
# Input file content:
# Line 1
# Line 2
# Line 3
# Line 4
# Output: Line 1, Line 3
```

**Commands used:** `sed`, `awk`, or `grep` with patterns

**What it teaches:**
- Advanced text processing
- Line selection and filtering
- Regular expressions and patterns
- Using `sed` or `awk` for selective output

---

### 17-water_and_stir
Adds two hexadecimal numbers and converts the result back to hexadecimal format. The variables represent ocean (water) and fire (stir).

```bash
bash 17-water_and_stir
# Adds two hex numbers: water + stir
# Converts result back to hexadecimal
```

**Commands used:** Arithmetic expansion, base conversion

**What it teaches:**
- Hexadecimal arithmetic
- Base conversion in calculations
- Using variable names for readability
- Complex arithmetic operations

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

# Method 3: Source the script (loads variables into current shell)
source script_name
. script_name
```

### Testing Scripts

Some scripts define variables or aliases. Test them:

```bash
# Before running script
echo $BEST  # Empty or previous value

# Run the script
bash 6-create_local_variable

# The variable only exists in the script's subshell
bash 6-create_local_variable; echo $BEST  # Won't show variable

# To load into current shell
source 6-create_local_variable
echo $BEST  # Now shows "School"
```

### Learning Path

Follow this recommended order:

1. Start with aliases (`0-alias`, `1-hello_you`)
2. Learn PATH manipulation (`2-path`, `3-paths`)
3. Understand variable scope (`4-global_variables` through `7-create_global_variable`)
4. Practice arithmetic (`8-true_knowledge` through `10-love_exponent_breath`)
5. Master number conversions (`11-binary_to_decimal`, `14-decimal_to_hexadecimal`)
6. Advanced string manipulation (`12-combinations` through `17-water_and_stir`)

## 🔑 Key Concepts <a name = "key_concepts"></a>

### Aliases

Create shortcuts for commands:

```bash
alias ll='ls -la'
alias cdh='cd ~'
alias clear_screen='clear'
alias grep='grep --color=auto'
```

### Environment and Variables

```bash
# Display environment variables
env
printenv
set

# Create local variable
VARIABLE="value"

# Export to make global
export VARIABLE="value"

# Access variable
echo $VARIABLE
echo ${VARIABLE}
```

### Expansions

**Variable Expansion:**
```bash
echo $USER        # Print current user
echo ${USER}_dir  # Avoid ambiguity
```

**Command Substitution:**
```bash
echo $(pwd)       # Print current directory
echo `pwd`        # Old syntax (avoid)
```

**Arithmetic Expansion:**
```bash
echo $((2 + 2))           # 4
echo $((10 - 3))          # 7
echo $((5 * 3))           # 15
echo $((10 / 2))          # 5
echo $((2 ** 8))          # 256 (exponentiation)
echo $((10 % 3))          # 1 (modulo)
```

**Brace Expansion:**
```bash
echo {1..5}               # 1 2 3 4 5
echo {a..e}               # a b c d e
echo test{1,2,3}          # test1 test2 test3
```

## 📊 Variable Types <a name = "variable_types"></a>

### Environment Variables (Global)

Accessible to all child processes:

| Variable | Purpose |
|----------|---------|
| `USER` | Current username |
| `HOME` | Home directory path |
| `PATH` | Directories for executables |
| `SHELL` | Current shell |
| `PWD` | Current working directory |
| `OLDPWD` | Previous working directory |
| `HOSTNAME` | Computer name |
| `LANG` | Language settings |

### Creating Variables

```bash
# Local variable (this shell only)
MYVAR="value"

# Global variable (exported to child processes)
export MYVAR="value"
```

## 🔢 Number Bases <a name = "number_bases"></a>

### Base Conversion Examples

```bash
# Binary to Decimal
echo $((2#101))           # 5

# Decimal to Binary
echo $(( $(echo "obase=2; 10" | bc) ))

# Hexadecimal to Decimal
echo $((16#FF))           # 255

# Decimal to Hexadecimal
printf "%x\n" 255         # ff

# Octal to Decimal
echo $((8#777))           # 511
```

## 🛠️ Advanced Commands <a name = "advanced_commands"></a>

### Text Processing

```bash
# tr - Translate characters
echo "hello" | tr 'a-z' 'A-Z'    # HELLO
echo "hello" | tr 'helo' '1234'  # 1233o

# sed - Stream editor
sed 's/old/new/' file            # Replace first occurrence
sed 's/old/new/g' file           # Replace all occurrences

# awk - Text processing
awk '{print $1}' file            # Print first column
awk 'NR % 2' file                # Print odd lines
```

### printf for Formatting

```bash
printf "Name: %s\n" "John"       # String formatting
printf "Number: %d\n" 42         # Integer formatting
printf "Float: %.2f\n" 3.14159   # Float with 2 decimals
printf "%x\n" 255                # Hexadecimal (ff)
printf "%o\n" 8                  # Octal (10)
```

## 📁 Initialization Files <a name = "init_files"></a>

### Common Initialization Files

- `.bashrc` - Loaded for non-login interactive shells
- `.bash_profile` - Loaded for login shells
- `.bash_logout` - Executed when exiting a login shell
- `/etc/bashrc` - System-wide configuration
- `/etc/profile` - System-wide login configuration

These files typically contain:
- Aliases
- Environment variables
- Functions
- PATH modifications

## ⛏️ Built Using <a name = "built_using"></a>

- [Bash Shell](https://www.gnu.org/software/bash/) - Command-line shell
- [Linux](https://www.linux.org/) - Operating system
- [GNU Core Utilities](https://www.gnu.org/software/coreutils/) - Standard utilities
- [sed](https://www.gnu.org/software/sed/) - Stream editor
- [awk](https://www.gnu.org/software/gawk/) - Text processing language
- [tr](https://linux.die.net/man/1/tr) - Translate command

## ✍️ Authors <a name = "authors"></a>

- [@hugou74130](https://github.com/hugou74130) - Complete work

See also the list of [contributors](https://github.com/hugou74130/holbertonschool-shell/contributors) who participated in this project.

## 📚 Additional Resources <a name = "resources"></a>

- [GNU Bash Manual - Variables](https://www.gnu.org/software/bash/manual/html_node/Shell-Variables.html)
- [GNU Bash Manual - Expansions](https://www.gnu.org/software/bash/manual/html_node/Expansions.html)
- [Bash Arithmetic](https://www.gnu.org/software/bash/manual/html_node/Arithmetic-Expansion.html)
- [Advanced Bash Scripting Guide](https://www.tldp.org/LDP/abs/html/)
- [Bash Cheat Sheet](https://devhints.io/bash)

## 🎉 Acknowledgements <a name = "acknowledgement"></a>

- Holberton School for the curriculum and advanced projects
- The Linux and Unix communities for creating powerful scripting languages
- The Bash community for continuous improvements and documentation
- All learners using this resource to master shell scripting
