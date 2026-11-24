### Experiment 6: Shell Programming — Sum of Two Numbers & Fibonacci Series

#### Part A: Shell Program — Sum of Two Numbers

**Objective:**



To write and execute a shell script that reads two integers from standard input and computes their sum using arithmetic expansion.



**Program:**

Bash
```
#!/bin/bash
echo -n "Enter first number: "
read a
echo -n "Enter second number: "
read b

sum=$((a + b))
echo "The sum of $a and $b is: $sum"

```

**Sample Output:**

Plaintext
```
Enter first number: 12
Enter second number: 18
The sum of 12 and 18 is: 30

```

**Conclusion:**



The script demonstrates basic input/output handling and integer addition in Bash using the `read` command and `$((...))` arithmetic evaluation.

#### Part B: Shell Program — Generate Fibonacci Series

**Objective:**



To write and execute a shell script that generates and prints the Fibonacci sequence up to $N$ terms specified by the user.



**Program:**

Bash
```
#!/bin/bash
echo -n "Enter the number of terms: "
read n

a=0
b=1

echo "Fibonacci series up to $n terms:"
for (( i=0; i<n; i++ ))
do
    echo -n "$a "
    next=$((a + b))
    a=$b
    b=$next
done
echo ""

```

**Sample Output:**

Plaintext
```
Enter the number of terms: 7
Fibonacci series up to 7 terms:
0 1 1 2 3 5 8 

```

**Conclusion:**



Shell scripting automates repetitive computational tasks in Linux by combining user input (`read`), integer arithmetic (`$((...))`), and iterative control structures (`for` loops) to generate sequential series accurately.
