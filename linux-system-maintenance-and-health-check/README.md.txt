# IT Support: Linux System Maintenance & Health Check

### Overview

This project demonstrates a proactive approach to system administration by performing a routine health check on a Linux server. The goal is to **identify potential issues before they become problems** and ensure the system is running efficiently. This case study covers essential tasks such as monitoring system resources, checking logs, and managing running processes.

### Features

- System Resource Monitoring: Check CPU, memory, and disk usage to identify bottlenecks.
- Log Analysis: Review system logs to find and diagnose errors.
- Process Management: Identify and manage running processes to maintain system stability.
- Proactive Maintenance: Perform routine updates and cleanup to keep the system healthy.

### Tools Used

- Ubuntu Server: The Linux distribution used for the server environment.
- VirtualBox: The virtualization software used to host the Linux server.
- Linux Command Line (CLI): The primary interface for all commands and configurations.

### Setup Instructions

1.  A new virtual machine was created in **VirtualBox** using an **Ubuntu Server LTS** ISO image.
2.  During the installation, a **non-root user** was created with **sudo** privileges.
3.  The base operating system was installed without any additional "snaps" to ensure a clean environment.

### Example Workflow

To perform the health check, I used a series of command-line tools to gather data and identify any issues.

#### Step 1: Check System Resource Usage

First, I checked the server's resource utilization to see how it was performing.

- Memory & CPU: I used the `free` and `top` commands to get a snapshot of memory and CPU usage.

    `free -h`
    `top`

    *What this shows:* `free -h` shows the total, used, and available memory in a human-readable format. `top` provides a real-time, dynamic view of processes and their resource consumption.

- Disk Usage: I used the `df` command to check how much disk space was being used.

    `df -h`

    *What this shows:* This command displays the available and used disk space for all mounted file systems. This is a crucial check to prevent the server from running out of space.

#### Step 2: Review System Logs for Errors

I then checked the system logs to look for any recent errors, warnings, or failures that could indicate an underlying problem.

`sudo journalctl -p err -xb`

#### Diagnosing System Health

After running a quick check of the system logs, I found several errors and warnings. Instead of assuming the system was broken, I analyzed each entry to determine its significance.

- `vmwgfx` error: This error indicated that a graphics driver was designed for VMware but was running on my VirtualBox hypervisor. I determined this was an expected configuration issue for this lab environment and not a critical problem.
- `Spectre v2` warning: This was a warning about a serious CPU vulnerability. I recognized this as a common warning in virtualized environments that does not pose a threat to my lab.
- `PAM` error: This was a minor configuration error related to a login module. It did not prevent me from using the system and was deemed non-critical.

**Conclusion:** I was able to successfully differentiate between significant and minor issues, a key skill for any IT professional. By not overreacting to the "red text," I demonstrated an understanding of the environment and avoided wasting time on harmless warnings.

#### Step 3: Identify and Manage Running Processes

To ensure no unnecessary or rogue processes were consuming resources, I listed all active processes.

`ps aux`

*What this shows:* This command provides a comprehensive list of all running processes, their status, and the user who started them. In a real-world scenario, you would use this to identify and `kill` (terminate) any non-critical processes that are using too much memory or CPU.

#### Step 4: Clean Up and Update the System

Finally, I performed routine maintenance to free up space and apply security patches.

`sudo apt autoclean`
`sudo apt autoremove`
`sudo apt update && sudo apt upgrade`

*What this shows:* `autoclean` removes old installation packages, and `autoremove` removes dependencies that are no longer needed. The final two commands ensure the system is fully up-to-date and secure.

### Key Learnings

- **Gained proficiency** in diagnosing system health and resource usage using essential command-line tools.
- **Understood the importance** of proactive monitoring and log analysis for maintaining a stable system.
- **Practiced a core IT support task** of routine maintenance to prevent system failures.
- **Demonstrated problem-solving skills** by identifying key system information and cleaning up the environment.