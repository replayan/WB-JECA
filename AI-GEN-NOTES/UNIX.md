# UNIX Commands and Concepts

## Basic Commands

### 1. `ls`
- **Purpose**: List directory contents.
- **Options**:
  - `-l`: Long listing format.
  - `-a`: Include hidden files.
  - `-h`: Human-readable file sizes.
  - `-R`: Recursively list subdirectories.
- **Example**: `ls -lha`

### 2. `ps`
- **Purpose**: Report a snapshot of current processes.
- **Options**:
  - `-e`: Show all processes.
  - `-f`: Full-format listing.
  - `-u`: User-oriented format.
- **Example**: `ps -ef`

### 3. `pwd`
- **Purpose**: Print working directory.
- **Options**:
  - None.
- **Example**: `pwd`

### 4. `mv`
- **Purpose**: Move or rename files or directories.
- **Options**:
  - `-i`: Interactive mode (prompt before overwrite).
  - `-v`: Verbose mode.
- **Example**: `mv oldname newname`

### 5. `cp`
- **Purpose**: Copy files or directories.
- **Options**:
  - `-r`: Recursive copy.
  - `-i`: Interactive mode.
  - `-v`: Verbose mode.
- **Example**: `cp -r source destination`

### 6. `touch`
- **Purpose**: Create an empty file or update the timestamp of an existing file.
- **Options**:
  - `-c`: Do not create any files.
  - `-t`: Use specified timestamp.
- **Example**: `touch filename`

### 7. `cat`
- **Purpose**: Concatenate and display file contents.
- **Options**:
  - `-n`: Number the output lines.
  - `-E`: Display $ at the end of each line.
- **Example**: `cat file1 file2`

### 8. `time`
- **Purpose**: Measure the time taken to execute a command.
- **Options**:
  - None specific to command.
- **Example**: `time ls`

### 9. `cal`
- **Purpose**: Display a calendar.
- **Options**:
  - `-y`: Display the calendar for the whole year.
  - `-m`: Display a specific month.
- **Example**: `cal 2024`

### 10. `bc`
- **Purpose**: Arbitrary precision calculator language.
- **Options**:
  - None specific to command.
- **Example**: `echo "scale=2; 5/3" | bc`

### 11. `sort`
- **Purpose**: Sort lines of text files.
- **Options**:
  - `-r`: Reverse the result of comparisons.
  - `-n`: Compare according to string numerical value.
  - `-u`: Output only the first of an equal run.
- **Example**: `sort file`

### 12. `diff`
- **Purpose**: Compare files line by line.
- **Options**:
  - `-q`: Output only whether files differ.
  - `-y`: Side-by-side comparison.
- **Example**: `diff file1 file2`

### 13. `wc`
- **Purpose**: Print newline, word, and byte counts for each file.
- **Options**:
  - `-l`: Lines count.
  - `-w`: Words count.
  - `-c`: Bytes count.
- **Example**: `wc filename`

### 14. `comm`
- **Purpose**: Compare two sorted files line by line.
- **Options**:
  - `-1`: Suppress column 1 (lines unique to file1).
  - `-2`: Suppress column 2 (lines unique to file2).
  - `-3`: Suppress column 3 (common lines).
- **Example**: `comm file1 file2`

### 15. `ln`
- **Purpose**: Create hard and symbolic links.
- **Options**:
  - `-s`: Create symbolic links.
  - `-f`: Remove existing destination files.
- **Example**: `ln -s source target`

### 16. `du`
- **Purpose**: Estimate file space usage.
- **Options**:
  - `-h`: Human-readable format.
  - `-s`: Display only a total for each argument.
- **Example**: `du -sh directory`

### 17. `kill`
- **Purpose**: Send a signal to a process.
- **Options**:
  - `-9`: Forcefully terminate a process.
  - `-l`: List available signal names.
- **Example**: `kill -9 PID`

### 18. `sleep`
- **Purpose**: Delay for a specified amount of time.
- **Options**:
  - Time value in seconds, minutes, hours, or days.
- **Example**: `sleep 5s`

### 19. `chmod`
- **Purpose**: Change file access permissions.
- **Options**:
  - `u`: User.
  - `g`: Group.
  - `o`: Others.
  - `+`, `-`, `=`: Add, remove, or set permission.
- **Example**: `chmod u+x filename`

### 20. `chown`
- **Purpose**: Change file owner and group.
- **Options**:
  - `-R`: Recursive change.
- **Example**: `chown user:group filename`

### 21. `chgrp`
- **Purpose**: Change group ownership.
- **Options**:
  - `-R`: Recursive change.
- **Example**: `chgrp group filename`

### 22. `top`
- **Purpose**: Display tasks and system resource usage.
- **Options**:
  - `-u`: Display tasks for a specific user.
- **Example**: `top`

### 23. `nice`
- **Purpose**: Run a program with modified scheduling priority.
- **Options**:
  - `-n`: Set the nice value.
- **Example**: `nice -n 10 command`

### 24. `renice`
- **Purpose**: Alter priority of running processes.
- **Options**:
  - `-p`: Specify PID.
- **Example**: `renice -n 10 -p PID`

### 25. `cut`
- **Purpose**: Remove sections from each line of files.
- **Options**:
  - `-d`: Specify delimiter.
  - `-f`: Specify fields.
- **Example**: `cut -d':' -f1 /etc/passwd`

### 26. `paste`
- **Purpose**: Merge lines of files.
- **Options**:
  - `-d`: Specify delimiter.
- **Example**: `paste file1 file2`

### 27. `grep`
- **Purpose**: Print lines that match patterns.
- **Options**:
  - `-i`: Ignore case.
  - `-v`: Invert match.
  - `-r`: Recursive search.
- **Example**: `grep -i "pattern" file`

### 28. `file`
- **Purpose**: Determine file type.
- **Options**:
  - None specific to command.
- **Example**: `file filename`

### 29. `whereis`
- **Purpose**: Locate binary, source, and manual pages for a command.
- **Options**:
  - `-b`: Locate binaries.
  - `-m`: Locate manual sections.
  - `-s`: Locate sources.
- **Example**: `whereis ls`

### 30. `which`
- **Purpose**: Locate a command.
- **Options**:
  - None specific to command.
- **Example**: `which ls`

### 31. `echo`
- **Purpose**: Display a line of text.
- **Options**:
  - `-n`: Do not output the trailing newline.
  - `-e`: Enable interpretation of backslash escapes.
- **Example**: `echo "Hello, World!"`

### 32. `env`
- **Purpose**: Display or set environment variables.
- **Options**:
  - None specific to command.
- **Example**: `env`

### 33. `PATH`
- **Purpose**: Environment variable specifying the search path for executable files.
- **Usage**:
  - `export PATH=$PATH:/new/path`
- **Example**: `echo $PATH`

### 34. `CLASSPATH`
- **Purpose**: Environment variable specifying the search path for Java classes.
- **Usage**:
  - `export CLASSPATH=/path/to/classes`
- **Example**: `echo $CLASSPATH`

### 35. `find`
- **Purpose**: Search for files in a directory hierarchy.
- **Options**:
  - `-name`: Search by name.
  - `-type`: Search by file type.
  - `-exec`: Execute command on found files.
- **Example**: `find / -name filename`

---

## VI Editor
- **Purpose**: Text editor in UNIX.
- **Modes**:
  - **Command Mode**: Default mode for navigation and commands.
  - **Insert Mode**: For inserting text.
  - **Command-Line Mode**: For saving, quitting, etc.


- **Basic Commands**:
  - `i`: Switch to insert mode.
  - `:w`: Save the file.
  - `:q`: Quit the editor.
  - `:wq`: Save and quit.
  - `:q!`: Quit without saving.

## Shell
- **Purpose**: Command interpreter for UNIX systems.
- **Types**:
  - **Bourne Shell (sh)**: Original UNIX shell.
  - **Bourne Again Shell (bash)**: Most common and feature-rich.
  - **C Shell (csh)**: Syntax resembles the C programming language.
  - **Korn Shell (ksh)**: Combines features of `sh` and `csh`.

## Wildcard
- **Purpose**: Used in filename expansion and pattern matching.
- **Types**:
  - `*`: Matches zero or more characters.
  - `?`: Matches exactly one character.
  - `[]`: Matches any one of the enclosed characters.
- **Example**: `ls *.txt` lists all `.txt` files.

## Shell Script
- **Purpose**: Script written for the shell, automating tasks.
- **Basic Structure**:
  - **Shebang**: `#!/bin/bash`
  - **Variables**: `VAR=value`
  - **Control Structures**:
    - **If**: `if [ condition ]; then commands; fi`
    - **Loops**: `for VAR in list; do commands; done`
  - **Functions**: `function_name() { commands; }`
- **Example**:
  ```sh
  #!/bin/bash
  echo "Hello, World!"
  ```
