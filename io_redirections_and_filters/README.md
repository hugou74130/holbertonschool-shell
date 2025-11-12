<p align="center">
  <a href="https://github.com/hugou74130/holbertonschool-shell/tree/main/io_redirections_and_filters" rel="noopener">
 <img width=400px height=200px src="https://image.noelshack.com/fichiers/2025/46/3/1762949159-gemini-generated-image-xbiyqnxbiyqnxbiy.jpg" alt="Project logo"></a>
</p>

<h3 align="center">I/O Redirections and Filters - Advanced Text Processing</h3>

<div align="center">

[![Status](https://img.shields.io/badge/status-active-success.svg)]()
[![GitHub Issues](https://img.shields.io/github/issues/hugou74130/holbertonschool-shell.svg)](https://github.com/hugou74130/holbertonschool-shell/issues)
[![GitHub Pull Requests](https://img.shields.io/github/issues-pr/hugou74130/holbertonschool-shell.svg)](https://github.com/hugou74130/holbertonschool-shell/pulls)

</div>

---

<p align="center"> Master input/output redirections, pipes, and powerful text filtering commands in Bash.
    <br>
Learn to combine commands and manipulate data streams to process, transform, and analyze text efficiently.
    <br>
</p>

## 📝 Table of Contents
- [About](#about)
- [Getting Started](#getting_started)
- [Scripts](#scripts)
- [Usage](#usage)
- [I/O Redirection Guide](#io_guide)
- [Filter Commands](#filter_commands)
- [Built Using](#built_using)
- [Authors](#authors)
- [Acknowledgments](#acknowledgement)

## 🧐 About <a name = "about"></a>

The I/O Redirections and Filters module is one of the most powerful aspects of shell scripting. You will learn how to redirect input and output streams, combine commands using pipes, and use powerful text filtering utilities to process data.

These techniques are essential for system administration, data processing, log analysis, and automation. By mastering redirections and filters, you can write sophisticated one-liners and scripts that manipulate text with precision and efficiency.

## 🏁 Getting Started <a name = "getting_started"></a>

### Prerequisites

You will need:

```
- A Unix/Linux terminal (Ubuntu, macOS, WSL on Windows)
- Bash shell
- Text files for practice (will be created during exercises)
- Understanding of basic shell commands
```

### Setup

Clone the repository and navigate to the io_redirections_and_filters folder:

```bash
git clone https://github.com/hugou74130/holbertonschool-shell.git
cd holbertonschool-shell/io_redirections_and_filters
```

## 📋 Scripts <a name = "scripts"></a>

### 0-hello_world
Prints "Hello, World" to standard output. Introduction to output and redirection concepts.

```bash
bash 0-hello_world
# Output: Hello, World
```

**Concepts:** Basic output, `echo` command

**What it teaches:** Foundation for understanding output streams

---

### 1-confused_smiley
Prints a confused smiley face `"(Ôo)'`. Demonstrates handling special characters and escaping.

```bash
bash 1-confused_smiley
# Output: "(Ôo)'
```

**Concepts:** Escaping special characters, quote handling

**What it teaches:** Working with special characters in shell scripts

---

### 2-hellofile
Displays the contents of a file named `hello`. Introduction to file reading.

```bash
bash 2-hellofile
# Output: Contents of the 'hello' file
```

**Commands used:** `cat`

**What it teaches:** Reading file contents with `cat`

---

### 3-twofiles
Displays the contents of two files: `hello` and `world`. Shows concatenating multiple files.

```bash
bash 3-twofiles
# Output: Contents of hello file, then contents of world file
```

**Commands used:** `cat file1 file2`

**What it teaches:** Concatenating multiple files with `cat`

---

### 4-lastlines
Displays the last 10 lines of a file named `iacta`. Uses the `tail` command.

```bash
bash 4-lastlines
# Output: Last 10 lines of the 'iacta' file
```

**Commands used:** `tail`, `tail -10`

**What it teaches:** Using `tail` to view end of files

---

### 5-firstlines
Displays the first 10 lines of a file named `iacta`. Uses the `head` command.

```bash
bash 5-firstlines
# Output: First 10 lines of the 'iacta' file
```

**Commands used:** `head`, `head -10`

**What it teaches:** Using `head` to view beginning of files

---

### 6-third_line
Displays the 3rd line of a file named `iacta`. Combines multiple commands to extract specific lines.

```bash
bash 6-third_line
# Output: The 3rd line of the 'iacta' file
```

**Commands used:** `head -3 | tail -1` or `sed '3!d'`

**What it teaches:** Extracting specific lines using pipes and filters

---

### 7-file
Prints the file type of a file specified by a variable. Uses the `file` command to determine file types.

```bash
bash 7-file
# Output: /etc/passwd: ASCII text
```

**Commands used:** `file`

**What it teaches:** Determining file types with `file` command

---

### 8-cwd_state
Saves the result of `ls -la` to a file. Demonstrates output redirection to files.

```bash
bash 8-cwd_state
# Creates: ls_cwd_content (containing directory listing)
```

**Commands used:** Output redirection `>`, `ls -la`

**What it teaches:** Redirecting output to files with `>`

---

### 9-duplicate_last_line
Appends the last line of a file named `iacta` at the end of the file. Shows output appending.

```bash
bash 9-duplicate_last_line
# Appends last line to iacta file
```

**Commands used:** `tail -1`, append redirection `>>`

**What it teaches:** Appending to files with `>>` instead of overwriting

---

### 10-no_more_js
Deletes all files ending with `.js` in the current directory.

```bash
bash 10-no_more_js
# Removes all *.js files
```

**Commands used:** `rm`, wildcards, file matching

**What it teaches:** Deleting files matching patterns with `rm`

---

### 11-directories
Lists only directories in the current directory and parent directories. Shows selective listing.

```bash
bash 11-directories
# Output: Lists only directories, not files
```

**Commands used:** `ls -d`, filtering

**What it teaches:** Using `ls -d` to list only directories

---

### 12-newest_files
Displays the 10 newest files in the current directory, sorted by modification time.

```bash
bash 12-newest_files
# Output: 10 most recently modified files
```

**Commands used:** `ls -t`, `head -10`

**What it teaches:** Sorting files by time and selecting top results

---

### 13-unique
Takes a list of words that might have duplicates and displays each word only once, sorted alphabetically.

```bash
bash 13-unique
# Input: apple, banana, apple, cherry
# Output: apple, banana, cherry (sorted, no duplicates)
```

**Commands used:** `sort`, `uniq`

**What it teaches:** Removing duplicates with `sort | uniq`

---

### 14-findthatword
Displays lines containing a specific word (pattern) from a file. Uses grep for pattern matching.

```bash
bash 14-findthatword
# Output: Lines containing the search pattern
```

**Commands used:** `grep`

**What it teaches:** Searching for patterns with `grep`

---

### 15-countthatword
Counts the number of times a word appears in a file.

```bash
bash 15-countthatword
# Output: Number of occurrences (e.g., 42)
```

**Commands used:** `grep -c` or `grep | wc -l`

**What it teaches:** Counting pattern matches with `grep -c` or `wc`

---

### 16-whatsnext
Displays lines that appear after a pattern match in a file.

```bash
bash 16-whatsnext
# Output: Lines following the matched pattern
```

**Commands used:** `grep -A` (after context)

**What it teaches:** Using `grep -A` to show context after matches

---

### 17-hidethisword
Displays all lines except those containing a specific word.

```bash
bash 17-hidethisword
# Output: All lines except those matching the pattern
```

**Commands used:** `grep -v` (invert match)

**What it teaches:** Using `grep -v` to exclude matching lines

---

### 18-letteronly
Displays lines containing only letters (no digits or special characters).

```bash
bash 18-letteronly
# Output: Lines with only alphabetic characters
```

**Commands used:** `grep` with regular expressions, `grep "^[a-zA-Z]*$"`

**What it teaches:** Regular expressions for pattern validation

---

### 19-AZ
Replaces all uppercase A with lowercase a, and uppercase Z with lowercase z. Uses sed for substitution.

```bash
bash 19-AZ
# Input: "AMAZING" -> Output: "aMAzING"
```

**Commands used:** `sed 's/A/a/g'`, `sed 's/Z/z/g'`

**What it teaches:** Using `sed` for character substitution

---

### 20-hiago
Removes all uppercase and lowercase forms of a letter from input. Shows character deletion with `tr`.

```bash
bash 20-hiago
# Removes all instances of specified letter variants
```

**Commands used:** `tr -d`

**What it teaches:** Using `tr -d` to delete characters

---

### 21-reverse
Reverses the order of lines in a file. The last line becomes first, first becomes last.

```bash
bash 21-reverse
# Input:
# Line 1
# Line 2
# Output:
# Line 2
# Line 1
```

**Commands used:** `rev` (character reversal) or `tac` (line reversal)

**What it teaches:** Reversing text with `rev` or `tac`

---

### 22-users_and_homes
Displays all users and their home directories, sorted alphabetically.

```bash
bash 22-users_and_homes
# Output:
# bin:/usr/sbin:/sbin
# daemon:/usr/sbin:/sbin
# ...
```

**Commands used:** `cut`, `/etc/passwd` file, `sort`

**What it teaches:** Parsing system files and extracting fields with `cut`

---

### 23-empty_casks
Finds and displays all empty files and directories in the current directory and subdirectories.

```bash
bash 23-empty_casks
# Output: List of empty files and directories
```

**Commands used:** `find -empty`

**What it teaches:** Using `find` to locate empty files

---

### 24-gifs
Displays all files with `.gif` extension in the current and parent directories, sorted alphabetically.

```bash
bash 24-gifs
# Output: Lists all .gif files
```

**Commands used:** `find`, glob patterns

**What it teaches:** Finding files by extension with `find`

---

### 25-acrostic
Decodes an acrostic: takes the first letter of each line to form a message.

```bash
bash 25-acrostic
# Input:
# Apple
# Computer
# Rose
# Output: ACR
```

**Commands used:** `cut`, `tr`

**What it teaches:** Extracting and combining specific characters from lines

---

### 26-the_biggest_fan
Parses Apache log files and lists the 11 hosts that accessed the website most, sorted by access frequency.

```bash
bash 26-the_biggest_fan
# Output: Top 11 hosts accessing the server
```

**Commands used:** `cut`, `sort`, `uniq -c`, pipes

**What it teaches:** Complex text processing for log analysis

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

# Method 3: Run with input redirection
bash script_name < input_file.txt
```

### Working with Files

Many scripts expect input files. Create test files:

```bash
# Create test files
echo "Hello World" > hello
echo "Testing" > world
echo "This is a test file" > iacta
```

### Testing Output Redirection

```bash
# Redirect output to file
echo "Text" > output.txt

# Append to file
echo "More text" >> output.txt

# Redirect error output
command 2> error.txt

# Redirect both output and errors
command &> all_output.txt
```

### Learning Path

Follow this recommended order:

1. Basic output (`0-hello_world`, `1-confused_smiley`)
2. File reading (`2-hellofile` through `7-file`)
3. Output redirection (`8-cwd_state`, `9-duplicate_last_line`)
4. File operations (`10-no_more_js` through `12-newest_files`)
5. Text processing (`13-unique` through `20-hiago`)
6. Advanced filtering (`21-reverse` through `26-the_biggest_fan`)

## 🔧 I/O Redirection Guide <a name = "io_guide"></a>

### Standard Streams

Every process has three standard streams:
- **stdin (0)**: Standard input (keyboard)
- **stdout (1)**: Standard output (screen)
- **stderr (2)**: Standard error (screen)

### Output Redirection

```bash
# Redirect stdout to file (overwrite)
command > file.txt

# Redirect stdout to file (append)
command >> file.txt

# Redirect stderr to file
command 2> error.txt

# Redirect both stdout and stderr
command &> output.txt
command > output.txt 2>&1

# Redirect stderr to stdout
command 2>&1

# Discard output
command > /dev/null
```

### Input Redirection

```bash
# Redirect stdin from file
command < input.txt

# Read from multiple files (here document)
cat << EOF
Multiple lines
of input text
EOF
```

### Piping

```bash
# Pipe stdout of left command to stdin of right command
command1 | command2

# Pipe multiple commands
command1 | command2 | command3 | command4

# Capture output of command
output=$(command)
```

## 🔑 Filter Commands <a name = "filter_commands"></a>

### grep - Search Patterns

```bash
# Find lines matching pattern
grep "pattern" file.txt

# Case-insensitive search
grep -i "pattern" file.txt

# Invert match (lines NOT matching)
grep -v "pattern" file.txt

# Count matching lines
grep -c "pattern" file.txt

# Show context (lines before/after)
grep -A 3 "pattern" file.txt      # 3 lines after
grep -B 3 "pattern" file.txt      # 3 lines before
grep -C 3 "pattern" file.txt      # 3 lines both

# Regular expressions
grep "^pattern" file.txt          # Start of line
grep "pattern$" file.txt          # End of line
grep "[0-9]" file.txt             # Contains digit
```

### sed - Stream Editor

```bash
# Substitute first occurrence per line
sed 's/old/new/' file.txt

# Substitute all occurrences
sed 's/old/new/g' file.txt

# Delete lines matching pattern
sed '/pattern/d' file.txt

# Print specific line
sed -n '5p' file.txt

# Print range of lines
sed -n '5,10p' file.txt

# Delete lines
sed '5d' file.txt                 # Delete line 5
sed '5,10d' file.txt              # Delete lines 5-10
```

### awk - Text Processing

```bash
# Print specific field
awk '{print $1}' file.txt         # Print first field

# Print lines matching condition
awk '/pattern/' file.txt

# Print line if field matches
awk '$1 == "value"' file.txt

# Sum values in column
awk '{sum += $1} END {print sum}' file.txt

# Print with line numbers
awk '{print NR, $0}' file.txt
```

### cut - Extract Columns

```bash
# Extract by character position
cut -c 1-5 file.txt               # Characters 1-5

# Extract by field (delimiter :)
cut -d: -f1 /etc/passwd           # Extract username

# Extract multiple fields
cut -d: -f1,3,6 /etc/passwd       # Fields 1, 3, 6
```

### sort - Sort Lines

```bash
# Sort alphabetically
sort file.txt

# Sort numerically
sort -n file.txt

# Sort in reverse
sort -r file.txt

# Sort by field
sort -k 2 file.txt                # Sort by 2nd field

# Remove duplicates while sorting
sort -u file.txt
```

### uniq - Remove Duplicates

```bash
# Remove duplicate adjacent lines
uniq file.txt

# Count occurrences
uniq -c file.txt

# Show only duplicates
uniq -d file.txt

# Show only unique lines
uniq -u file.txt

# Note: uniq requires sorted input
sort file.txt | uniq
```

### wc - Word/Line Count

```bash
# Count lines
wc -l file.txt

# Count words
wc -w file.txt

# Count characters/bytes
wc -c file.txt

# Count all (lines, words, bytes)
wc file.txt
```

### head and tail

```bash
# First 10 lines
head file.txt

# First 20 lines
head -20 file.txt

# Last 10 lines
tail file.txt

# Last 20 lines
tail -20 file.txt

# Follow file (watch as it grows)
tail -f logfile.txt
```

### tr - Translate Characters

```bash
# Substitute characters
tr 'a-z' 'A-Z' < file.txt         # Lowercase to uppercase

# Delete characters
tr -d '0-9' < file.txt            # Delete all digits

# Squeeze repeating characters
tr -s ' ' < file.txt              # Replace multiple spaces with one
```

### find - Search Files

```bash
# Find by name
find . -name "*.txt"

# Find empty files
find . -empty

# Find by type
find . -type f                    # Regular files
find . -type d                    # Directories

# Find by size
find . -size +1M                  # Larger than 1MB

# Find and execute command
find . -name "*.tmp" -delete
```

## 💡 Common Pipelines <a name = "pipelines"></a>

```bash
# Count occurrences of a word
grep -o "word" file.txt | wc -l

# Find and process files
find . -name "*.log" | xargs grep "ERROR"

# Sort by frequency
sort file.txt | uniq -c | sort -rn

# Extract and sort unique values
cut -d: -f1 /etc/passwd | sort | uniq

# Find large files
find . -type f -size +100M | sort -k5 -rn

# Process log file
tail -f access.log | grep "ERROR"
```

## ⛏️ Built Using <a name = "built_using"></a>

- [Bash Shell](https://www.gnu.org/software/bash/) - Command interpreter
- [grep](https://www.gnu.org/software/grep/) - Pattern matching utility
- [sed](https://www.gnu.org/software/sed/) - Stream editor
- [awk](https://www.gnu.org/software/gawk/) - Text processing language
- [Linux Utilities](https://www.gnu.org/software/coreutils/) - Core utilities

## ✍️ Authors <a name = "authors"></a>

- [@hugou74130](https://github.com/hugou74130) - Complete work

See also the list of [contributors](https://github.com/hugou74130/holbertonschool-shell/contributors) who participated in this project.

## 📚 Additional Resources <a name = "resources"></a>

- [GNU Bash Manual - Redirections](https://www.gnu.org/software/bash/manual/html_node/Redirections.html)
- [grep Manual](https://linux.die.net/man/1/grep)
- [sed Manual](https://linux.die.net/man/1/sed)
- [awk Manual](https://linux.die.net/man/1/awk)
- [Regular Expressions Guide](https://www.regular-expressions.info/)
- [Advanced Bash Scripting Guide](https://www.tldp.org/LDP/abs/html/)

## 🎉 Acknowledgements <a name = "acknowledgement"></a>

- Holberton School for the curriculum and challenging projects
- The Linux community for creating powerful text processing tools
- The GNU project for developing open-source utilities
- All learners using this resource to master text processing and data manipulation
