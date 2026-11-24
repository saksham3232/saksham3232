### Experiment 3: File Manipulation Commands & Largest of Three Numbers

#### Part A: Theory — Creating, Viewing, and Managing Text Files

**Objective:**



To create and display text files in Linux and demonstrate the practical usage of `touch`, `cp`, `mv`, and `rm` commands.



**Procedure / Steps:**

1. **Creating an Empty File (`touch`):**
   - Execute `touch notes.txt` to create a zero-byte file. If the file already exists, `touch` updates its access and modification timestamps.
2. **Adding Content and Displaying File Contents (`cat`):**
   - Execute `cat > notes.txt`, type lines of text (e.g., `"Linux Operating System Lab"`), and press `Ctrl+D` to save.
   - Execute `cat notes.txt` to display the entire contents of the file on the terminal standard output.
3. **Copying Files (`cp`):**
   - Execute `cp notes.txt notes_backup.txt` to create an exact copy of `notes.txt` under a new filename.
4. **Moving / Renaming Files (`mv`):**
   - Execute `mv notes_backup.txt final_notes.txt` to rename the file. (If the destination is a directory path, `mv` relocates the file into that directory).
5. **Removing Files (`rm`):**
   - Execute `rm final_notes.txt` to delete the file. Use `rm -i final_notes.txt` to prompt for confirmation before deletion.

**Conclusion:**



Commands such as `touch`, `cat`, `cp`, `mv`, and `rm` form the core toolkit for text file lifecycle management in Linux, enabling rapid file creation, inspection, duplication, relocation, and cleanup.

#### Part B: Shell Program — Largest of Three Numbers

**Objective:**



To write and execute a shell program that compares three numbers entered by the user and identifies the largest among them using `if-elif-else` statements and relational operators.



**Program:**

Bash
```bash
#!/bin/bash
echo -n "Enter first number: "
read a
echo -n "Enter second number: "
read b
echo -n "Enter third number: "
read c

if [ $a -ge $b ] && [ $a -ge $c ]; then
    echo "$a is the largest number."
elif [ $b -ge $a ] && [ $b -ge $c ]; then
    echo "$b is the largest number."
else
    echo "$c is the largest number."
fi

```

**Sample Output:**

Plaintext
```
Enter first number: 45
Enter second number: 89
Enter third number: 32
89 is the largest number.

```

**Conclusion:**



The shell script effectively uses logical AND (`&&`) and greater-than-or-equal-to (`-ge`) comparison operators within multi-branch conditional statements to determine the maximum of three numbers.





