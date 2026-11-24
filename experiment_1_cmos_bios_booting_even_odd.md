### Experiment 1: CMOS/BIOS Settings, Booting Process & Even/Odd Shell Program

#### Part A: Theory --- CMOS/BIOS Settings and Booting Process

**Objective:**

To understand the role of BIOS/UEFI and CMOS in computer hardware
initialization, how to access and modify system firmware settings, and
the step-by-step booting sequence of an operating system.

**Procedure / Steps:**

1.  **Power On and POST:** When the power button is pressed, the Power
    Supply Unit (PSU) sends a "Power Good" signal to the motherboard.
    The CPU executes the firmware stored in the ROM/Flash chip (BIOS or
    UEFI), triggering the **Power-On Self-Test (POST)** to verify RAM,
    CPU, keyboard, and storage drives.
2.  **Accessing CMOS/BIOS Setup:** During the initial splash screen,
    press the designated setup key (`F2`, `F10`, `F12`, or `Delete`,
    depending on the motherboard manufacturer) to enter the setup
    utility.
3.  **Inspecting and Configuring CMOS Settings:**
    -   **System Time & Date:** Stored in the battery-backed CMOS RAM.
    -   **Boot Priority / Boot Order:** Navigate to the **Boot** tab to
        arrange the sequence of bootable devices (e.g., USB Drive, Hard
        Disk/SSD, Optical Drive, Network PXE).
    -   **Hardware & Security Settings:** Review virtualization support
        (Intel VT-x / AMD-V), Secure Boot status, and administrator
        passwords.
4.  **Saving and Exiting:** Press `F10` (Save & Exit) to commit changes
    to CMOS memory and reboot the system.
5.  **Bootloader and OS Kernel Loading:**
    -   BIOS/UEFI locates the highest-priority bootable device and reads
        the Master Boot Record (MBR) or GUID Partition Table (GPT) to
        load the **Bootloader** (e.g., GRUB in Linux, Windows Boot
        Manager).
    -   The bootloader loads the operating system kernel and initial RAM
        disk (`initramfs`) into main memory.
    -   The kernel initializes system hardware, mounts the root
        filesystem, and starts the `init` / `systemd` process,
        presenting the user login screen.

**Conclusion:**

The booting process bridges hardware initialization and software
execution. Properly configuring CMOS/BIOS settings ensures hardware
components are recognized accurately and the system boots from the
intended storage medium.

#### Part B: Shell Program --- Check Even or Odd

**Objective:**

To write and execute a shell program that checks whether a given integer
is even or odd using the modulus (`%`) operator and `if-else`
conditional statements.

**Program:**

Bash

``` bash
#!/bin/bash
echo -n "Enter a number: "
read num

if [ $((num % 2)) -eq 0 ]; then
    echo "$num is an Even number."
else
    echo "$num is an Odd number."
fi
```

**Sample Output:**

Plaintext

``` csharp
Enter a number: 24
24 is an Even number.

Enter a number: 17
17 is an Odd number.
```

**Conclusion:**

The shell script successfully determines whether an input number is even
or odd by evaluating the remainder when divided by 2 using arithmetic
expansion and conditional branching.
