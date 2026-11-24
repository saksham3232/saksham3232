### Experiment 5: Routing Table, Route Tracing & Prime Number Program

#### Part A: Theory — Displaying the Routing Table and Tracing Network Paths

**Objective:**



To examine the kernel IP routing table and trace the network path (hops) packets take to reach a remote host.



**Procedure / Steps:**

1. **Displaying the Routing Table:**
   - Execute `ip route` (or `route -n` / `netstat -rn`) in the terminal.
   - Analyze the routing entries:
     - **Default Gateway (`default via <IP>`):** The router IP address to which all external traffic outside the local subnet is forwarded.
     - **Destination Network & Interface (`dev eth0` / `wlan0`):** Indicates which local network interface handles traffic for specific subnets.
2. **Tracing the Route to a Remote Host:**
   - Execute `traceroute google.com` (or `tracepath google.com` if `traceroute` is not installed).
   - Observe the numbered list of intermediate routers (**hops**) between the local machine and the destination server.
   - Note the three round-trip time (RTT) measurements in milliseconds (`ms`) per hop; asterisks (`* * *`) indicate routers configured not to respond to probe packets.

**Conclusion:**



Inspecting the routing table confirms how local outbound traffic is directed through the default gateway, while `traceroute` maps the exact hop-by-hop path across intermediate networks and helps isolate latency or packet drops.

#### Part B: Shell Program — Check Prime Number

**Objective:**



To write and execute a shell program that determines whether a given positive integer is a prime number by testing divisibility up to its square root.



**Program:**

Bash
```bash
#!/bin/bash
echo -n "Enter a positive integer: "
read num

if [ $num -le 1 ]; then
    echo "$num is NOT a prime number."
    exit 0
fi

is_prime=1
for (( i=2; i*i<=num; i++ ))
do
    if [ $((num % i)) -eq 0 ]; then
        is_prime=0
        break
    fi
done

if [ $is_prime -eq 1 ]; then
    echo "$num is a Prime number."
else
    echo "$num is NOT a Prime number."
fi

```

**Sample Output:**

Plaintext
```less
Enter a positive integer: 29
29 is a Prime number.

Enter a positive integer: 18
18 is NOT a Prime number.

```

**Conclusion:**



The shell script efficiently determines primality by checking factors from $2$ up to $\sqrt{n}$, using a flag variable and `break` statement to terminate early when a divisor is found.
