# UNIX Commands and Concepts

---

## 1. File and Directory Navigation & Management

### 1.1. **ls**  
- **Purpose:** List directory contents.  
- **Common Options:**
  - **`ls`**: Lists files in the current directory.
  - **`ls -l`**: Long listing format (permissions, owner, size, timestamp).
  - **`ls -a`**: Shows all files including hidden files (those starting with a dot).
  - **`ls -h`**: Human-readable sizes (if used with `-l`), e.g., “1K, 234M”.
  - **`ls -R`**: Recursively lists subdirectories.
- **Example:**  
  ```bash
  ls -la /home/user
  ```

### 1.2. **pwd**  
- **Purpose:** Print Working Directory  
- **Detail:** Displays the full pathname of the current directory.
- **Example:**  
  ```bash
  pwd
  ```

### 1.3. **mv**  
- **Purpose:** Move or rename files and directories.  
- **Options/Usage:**
  - **Moving Files:**  
    ```bash
    mv file1.txt /new/location/
    ```
  - **Renaming Files:**  
    ```bash
    mv oldname.txt newname.txt
    ```
  - **Verbose Option:** Some systems support `-v` to display what is being moved.
  
### 1.4. **cp**  
- **Purpose:** Copy files and directories.  
- **Common Options:**
  - **`cp file1 file2`**: Copy file1 to file2.
  - **`cp -r directory1 directory2`**: Recursively copy a directory.
  - **`cp -p`**: Preserves original file attributes (timestamps, permissions).
- **Example:**  
  ```bash
  cp -rv /source/dir /destination/dir
  ```

### 1.5. **touch**  
- **Purpose:** Update file timestamps or create a new empty file if it doesn’t exist.  
- **Example:**  
  ```bash
  touch newfile.txt
  ```

---

## 2. File Content & Display Commands

### 2.1. **cat**  
- **Purpose:** Concatenate and display file content.  
- **Usage Options:**
  - **View file content:**  
    ```bash
    cat file.txt
    ```
  - **Concatenate multiple files:**  
    ```bash
    cat file1.txt file2.txt > combined.txt
    ```
- **Other options:** `-n` to number the output lines.

### 2.2. **time**  
- **Purpose:** Measure how long a command takes to execute.  
- **Usage:**  
  ```bash
  time ls -l
  ```
- **Output:** Provides real (elapsed) time, user CPU time, and system CPU time.

### 2.3. **cal**  
- **Purpose:** Display a calendar.  
- **Usage:**  
  ```bash
  cal
  ```
- **Options:**  
  - **`cal 2025`**: Displays the calendar for the entire year.
  - Some versions provide options for a specific month.

### 2.4. **bc**  
- **Purpose:** An arbitrary precision calculator language.  
- **Usage:**
  - **Interactive calculation:**  
    ```bash
    echo "scale=2; 5/3" | bc
    ```
  - **Scripting:** Write more complex mathematical expressions inside a bc script file.

---

## 3. Text and File Comparison Utilities

### 3.1. **sort**  
- **Purpose:** Sort lines in a text file.  
- **Options:**
  - **`sort file.txt`**: Sorts the content of file.txt in ascending order.
  - **`sort -r file.txt`**: Reverse order.
  - **`sort -n file.txt`**: Numerical sort.
- **Example:**  
  ```bash
  sort -n numbers.txt
  ```

### 3.2. **diff**  
- **Purpose:** Compare files line by line and display differences.  
- **Options:**
  - **`diff file1 file2`**: Shows differences.
  - **`diff -u file1 file2`**: Unified format (commonly used for patch files).
- **Example:**  
  ```bash
  diff -u oldfile.txt newfile.txt
  ```

### 3.3. **wc**  
- **Purpose:** Count lines, words, and bytes in files.  
- **Options:**
  - **`wc file.txt`**: Displays line, word, and byte counts.
  - **`wc -l file.txt`**: Displays only the line count.
- **Example:**  
  ```bash
  wc -w document.txt
  ```

### 3.4. **comm**  
- **Purpose:** Compare two sorted files line by line.  
- **Details:**  
  - The output displays three columns: lines unique to the first file, lines unique to the second, and common lines.
  - **Usage:**  
    ```bash
    comm file1.txt file2.txt
    ```
  - **Note:** The files must be sorted before use.

### 3.5. **ln** *(often mis-typed as “In”)*  
- **Purpose:** Create hard and symbolic links.  
- **Usage:**
  - **Hard link:**  
    ```bash
    ln original.txt link.txt
    ```
  - **Symbolic (soft) link:**  
    ```bash
    ln -s /path/to/original /path/to/link
    ```

### 3.6. **file**  
- **Purpose:** Determine file type based on its content.  
- **Usage:**  
  ```bash
  file myfile
  ```

---

## 4. Process and System Monitoring

### 4.1. **ps**  
- **Purpose:** Display process status.  
- **Common Options:**
  - **`ps`**: Typically shows processes associated with the current terminal.
  - **`ps aux`**: Shows all running processes in BSD style.
  - **`ps -ef`**: Shows all running processes in System V style.
- **Example:**  
  ```bash
  ps -ef | grep bash
  ```

### 4.2. **du**  
- **Purpose:** Estimate file space usage.  
- **Usage Options:**
  - **`du -sh directory`**: Shows a summarized, human-readable output for a directory.
- **Example:**  
  ```bash
  du -sh /var/log
  ```

### 4.3. **kill**  
- **Purpose:** Terminate processes by process ID (PID).  
- **Usage:**
  - **Basic termination:**  
    ```bash
    kill 1234
    ```
  - **Force termination:**  
    ```bash
    kill -9 1234
    ```

### 4.4. **sleep**  
- **Purpose:** Delay command execution by a specified amount of time.  
- **Usage:**
  - **Pause for 5 seconds:**  
    ```bash
    sleep 5
    ```
  - Useful in scripts to wait for a process to complete or delay retries.

### 4.5. **top**  
- **Purpose:** Monitor system processes in real time.  
- **Features:** Displays CPU, memory usage, and process priorities.  
- **Usage:**  
  ```bash
  top
  ```
- **Note:** You can interactively sort or kill processes while top is running.

### 4.6. **nice** and **renice**  
- **nice:**  
  - **Purpose:** Start a process with a modified scheduling priority.  
  - **Usage:**  
    ```bash
    nice -n 10 command
    ```
- **renice:**  
  - **Purpose:** Change the priority of an already running process.
  - **Usage:**  
    ```bash
    renice +5 -p 1234
    ```
  - **Note:** Lower (more negative) values denote higher priority.

---

## 5. Text Manipulation Commands

### 5.1. **cut**  
- **Purpose:** Remove sections from each line of files, extracting columns or fields.  
- **Usage:**  
  - **Extract specific characters:**  
    ```bash
    cut -c 1-5 file.txt
    ```
  - **Extract fields by delimiter:**  
    ```bash
    cut -d':' -f1 /etc/passwd
    ```

### 5.2. **paste**  
- **Purpose:** Merge lines of files side-by-side (column-wise).  
- **Usage:**  
  ```bash
  paste file1.txt file2.txt
  ```
- **Note:** Useful for combining corresponding lines of two files.

### 5.3. **grep**  
- **Purpose:** Search text using regular expressions (pattern matching).  
- **Common Options:**
  - **`grep "pattern" file.txt`**: Search for “pattern” in file.txt.
  - **`grep -i "pattern" file.txt`**: Case-insensitive search.
  - **`grep -r "pattern" /path/to/directory`**: Recursive search.
  - **`grep -n "pattern" file.txt`**: Shows matching line numbers.
- **Example:**  
  ```bash
  grep -R "error" /var/log
  ```

---

## 6. File Location & Environment Utilities

### 6.1. **whereis**  
- **Purpose:** Locate the binary, source, and manual pages for a command.  
- **Usage:**  
  ```bash
  whereis ls
  ```
- **Note:** Provides a broad search compared to `which`.

### 6.2. **which**  
- **Purpose:** Locate the executable file associated with a command in the system’s PATH.  
- **Usage:**  
  ```bash
  which python
  ```

### 6.3. **echo**  
- **Purpose:** Display a line of text.  
- **Usage:**  
  ```bash
  echo "Hello, World!"
  ```
- **Features:** Often used in scripts to print messages or output environment variable values.

### 6.4. **env**  
- **Purpose:** Display, modify, or remove environment variables.  
- **Usage:**  
  ```bash
  env
  ```
- **Usage in Scripts:** Used to ensure the correct environment is set up before running a command.

### 6.5. **Environment Variables: PATH and CLASSPATH**  
- **PATH:**  
  - **Purpose:** Specifies a list of directories where the shell looks for executable files.
  - **Usage:**  
    ```bash
    echo $PATH
    ```
  - **Modification:** You can add directories, e.g.,  
    ```bash
    export PATH=$PATH:/new/directory
    ```
- **CLASSPATH:**  
  - **Purpose:** (Primarily for Java) Tells the Java runtime and compiler where to find class files.
  - **Usage:**  
    ```bash
    echo $CLASSPATH
    ```
  - **Modification:**  
    ```bash
    export CLASSPATH=.:/path/to/java/classes
    ```

### 6.6. **find**  
- **Purpose:** Search for files and directories recursively under a given path that meet specified criteria.  
- **Common Options:**
  - **By name:**  
    ```bash
    find /path -name "*.txt"
    ```
  - **By type (e.g., directory or file):**  
    ```bash
    find /path -type d  # for directories
    ```
  - **By size, modification time, permissions, etc.:**  
    ```bash
    find /tmp -type f -size +10M
    ```

---

## 7. The vi Editor

### 7.1. **vi/vim**  
- **Purpose:** A powerful screen-based text editor available on most Unix systems.  
- **Modes:**
  - **Normal Mode:** For navigation and executing commands.
  - **Insert Mode:** For inserting text (enter using **`i`** or **`a`**).
  - **Command Mode:** For saving, quitting, or other file operations (enter with **`: `**).
- **Common Commands:**
  - **Navigation:**  
    - `h`, `j`, `k`, `l` move left, down, up, right respectively.
    - `G` goes to the end of the file, `gg` goes to the beginning.
  - **Editing:**  
    - `i`: Insert before the cursor.
    - `a`: Append after the cursor.
    - `x`: Delete character under the cursor.
    - `dd`: Delete the current line.
    - `u`: Undo the last change.
  - **Saving and Quitting:**  
    - `:w` to save.
    - `:q` to quit.
    - `:wq` or `ZZ` to save and exit.
- **Tips:**  
  - Learn how to use search (using **`/pattern`**) and replace commands.
  - Practice navigation to become faster using vi’s numerous shortcuts.

---

## 8. Shell, Wildcards, and Shell Scripting

### 8.1. **Shell**  
- **Definition:** A command-line interpreter that provides a user interface for the Unix operating system.  
- **Popular Shells:** bash, sh, csh, ksh, zsh.
- **Role:** Executes commands, runs scripts, manages process control, and provides programming constructs (loops, conditionals).

### 8.2. **Wildcards (Globbing)**  
- **Purpose:** Patterns used to match file and directory names.
- **Common Wildcards:**
  - **`*`**: Matches any number of characters (including none).
  - **`?`**: Matches a single character.
  - **`[...]`**: Matches any one of the characters enclosed.
- **Example:**  
  ```bash
  ls *.txt    # lists all .txt files
  ls file??   # lists files like file01, fileAB, etc.
  ```

### 8.3. **Shell Script**  
- **Definition:** A file containing a sequence of commands that the shell can execute in batch mode.  
- **Structure & Basics:**
  - **Shebang:** The first line typically starts with `#!/bin/bash` (or another shell) to indicate the interpreter.
  - **Variables:**  
    ```bash
    name="WB-JECA"
    echo "Hello, $name"
    ```
  - **Control Structures:**  
    - **Conditionals:** `if [ condition ]; then ... fi`
    - **Loops:** `for`, `while` loops are commonly used.
  - **Execution:**  
    - Make the script executable:  
      ```bash
      chmod +x script.sh
      ```  
    - Run the script:  
      ```bash
      ./script.sh
      ```
- **Good Practices:**
  - Comment your code.
  - Check for errors (use exit statuses).
  - Use meaningful variable names and indentation for readability.

---

## 9. Summary and Study Tips

- **Review Commands Regularly:** Practice using these commands in the terminal. Create sample files/directories and try out different options.
- **Understand the Options:** Each command may have many options; focus on those most commonly used and understand their impact.
- **Scripting:** Write small shell scripts incorporating these commands to automate routine tasks.
- **Manual Pages:** Use the `man` command (e.g., `man ls`, `man find`) to read more details and explore less commonly used options.
- **Practice Exam Questions:** Prepare by solving sample problems or past questions if available, particularly focusing on process management, file manipulation, and text processing.
