### Experiment 2: Basic Linux Commands, File Operations & Sum of Two Numbers

#### Part A: Theory --- Basic Linux Commands and File Operations

**Objective:**

To execute foundational Linux navigation and system information commands
(`pwd`, `ls`, `mkdir`, `cd`, `date`, `whoami`, `uname`) and perform file
creation, copying, renaming, and deletion.

**Procedure / Steps:**

1.  **System and Directory Inspection Commands:**
    -   `pwd` (Print Working Directory): Displays the full absolute path
        of the current directory (e.g., `/home/student`).
    -   `ls` (List): Lists files and subdirectories in the current
        directory. Use `ls -la` to view hidden files and permissions.
    -   `date`: Displays the current system date and time.
    -   `whoami`: Prints the username of the currently logged-in user.
    -   `uname -a`: Displays system information including kernel name,
        hostname, kernel release, and hardware architecture.
2.  **Directory Navigation:**
    -   `mkdir lab_exp2`: Creates a new directory named `lab_exp2`.
    -   `cd lab_exp2`: Changes the current working directory into
        `lab_exp2`.
3.  **File Creation, Copying, Renaming, and Deletion:**
    -   **Create:** Run `touch file1.txt` to create an empty file, or
        `cat > file1.txt` followed by text and `Ctrl+D` to create a file
        with content.
    -   **Copy:** Run `cp file1.txt file2.txt` to duplicate `file1.txt`
        as `file2.txt`.
    -   **Rename:** Run `mv file2.txt renamed_file.txt` to rename
        `file2.txt`.
    -   **Delete:** Run `rm renamed_file.txt` to permanently remove the
        file from the directory.

**Conclusion:**

Basic Linux shell commands allow efficient navigation of the
hierarchical filesystem, inspection of system metadata, and direct
management of files and directories without a graphical interface.

#### Part B: Shell Program --- Sum of Two Numbers

**Objective:**

To write and execute a shell program that accepts two numbers from the
user and calculates their sum using arithmetic expansion.

**Program:**

Bash

    #!/bin/bash
    echo -n "Enter first number: "
    read num1
    echo -n "Enter second number: "
    read num2

    sum=$((num1 + num2))
    echo "Sum of $num1 and $num2 is: $sum"

**Sample Output:**

Plaintext

    Enter first number: 15
    Enter second number: 27
    Sum of 15 and 27 is: 42

**Conclusion:**

The shell script accurately reads two user-supplied integers via the
`read` command, performs addition using `$((...))`, and displays the
resulting sum.
