### Experiment 4: Network Interface Configuration, DNS Lookup & Factorial Program

#### Part A: Theory — Network Interfaces (`ip addr`) and DNS Resolution (`nslookup`)

**Objective:**



To inspect local network interface configurations and IP addresses using `ip addr`, and resolve domain names to IP addresses using `nslookup`.



**Procedure / Steps:**

1. **Displaying Network Interface Configuration:**
   - Open the terminal and execute `ip addr` (or `ip a`).
   - Observe the listed interfaces:
     - `lo` (Loopback interface): Assigned `127.0.0.1/8` for internal host communication.
     - `eth0` or `enp0s3` / `wlan0` (Ethernet or Wi-Fi interface): Displays the hardware MAC address (`link/ether`), assigned IPv4 address (`inet`), subnet mask prefix, and IPv6 address (`inet6`).
   - Verify that the interface state shows `UP` to confirm active network connectivity.
2. **Finding the IP Address of a Website (`nslookup`):**
   - Execute `nslookup google.com` (or any target domain) in the terminal.
   - Examine the output:
     - The top section (`Server` and `Address`) shows the local DNS resolver handling the query.
     - The `Non-authoritative answer` section displays the resolved IPv4 (`Address`) and IPv6 (`AAAA`) addresses associated with the website's domain name.

**Conclusion:**



The `ip addr` utility provides complete visibility into local network adapter states and assigned IP configurations, while `nslookup` verifies DNS functionality by mapping human-readable web domains to routable IP addresses.

#### Part B: Shell Program — Factorial of a Number

**Objective:**



To write and execute a shell program to compute the factorial of a given non-negative integer using a `for` loop.



**Program:**

Bash
```
#!/bin/bash
echo -n "Enter a non-negative integer: "
read num

fact=1
for (( i=1; i<=num; i++ ))
do
    fact=$((fact * i))
done

echo "Factorial of $num is: $fact"

```

**Sample Output:**

Plaintext
```
Enter a non-negative integer: 5
Factorial of 5 is: 120

```

**Conclusion:**



The shell program successfully computes the factorial of a number iteratively by multiplying sequential integers from $1$ up to $N$ inside a C-style `for` loop.





