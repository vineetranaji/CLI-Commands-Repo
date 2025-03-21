# Linux Commands

This document provides a list of useful Linux commands for managing your system.

## File and Directory Management

### `ls`
- Lists the files and directories in the current directory.

### `ls -l`
- Lists the files and directories in long format (permissions, ownership, size, etc.).

### `ls -a`
- Lists all files, including hidden files (those starting with a dot).

### `cd <directory>`
- Changes the current directory to the specified directory.

### `cd ..`
- Moves up one directory level.

### `pwd`
- Displays the current working directory.

### `mkdir <directory_name>`
- Creates a new directory.

### `rmdir <directory_name>`
- Removes an empty directory.

### `rm <file>`
- Removes a file.

### `rm -r <directory>`
- Removes a directory and its contents recursively.

### `cp <source> <destination>`
- Copies a file or directory to the specified destination.

### `cp -r <source> <destination>`
- Recursively copies a directory and its contents.

### `mv <source> <destination>`
- Moves or renames a file or directory.

### `touch <file>`
- Creates an empty file or updates the timestamp of an existing file.

### `find <path> -name <file_name>`
- Searches for a file by name in the specified directory or subdirectories.

### `locate <file_name>`
- Searches for a file using a prebuilt database (faster than `find`).

### `updatedb`
- Updates the database used by the `locate` command.

### `tree`
- Displays the directory structure in a tree-like format.

### `stat <file>`
- Displays detailed information about a file or directory (e.g., permissions, size, etc.).

## File Permissions

### `chmod <permissions> <file>`
- Changes the file permissions (e.g., `chmod 755 <file>`).

### `chown <user>:<group> <file>`
- Changes the ownership of a file or directory.

### `chgrp <group> <file>`
- Changes the group ownership of a file or directory.

### `umask`
- Displays or sets the default file creation mask.

## File Viewing and Editing

### `cat <file>`
- Displays the contents of a file.

### `more <file>`
- Displays the contents of a file, one screen at a time.

### `less <file>`
- Displays the contents of a file, one screen at a time (with scrollback support).

### `head <file>`
- Displays the first 10 lines of a file.

### `head -n <number> <file>`
- Displays the first N lines of a file.

### `tail <file>`
- Displays the last 10 lines of a file.

### `tail -f <file>`
- Continuously displays the last lines of a file (useful for log files).

### `nano <file>`
- Opens a file in the nano text editor.

### `vim <file>`
- Opens a file in the Vim text editor.

### `vi <file>`
- Opens a file in the vi text editor.

### `grep "<pattern>" <file>`
- Searches for a pattern in a file and displays matching lines.

### `grep -r "<pattern>" <directory>`
- Searches for a pattern recursively in a directory.

### `sed 's/<pattern>/<replacement>/g' <file>`
- Replaces all occurrences of a pattern with a replacement in a file.

### `awk '{print $1}' <file>`
- Prints the first field of each line in a file (useful for text processing).

## System Information and Management

### `uname -a`
- Displays system information (kernel version, OS, etc.).

### `hostname`
- Displays or sets the system's hostname.

### `uptime`
- Displays the system uptime and load averages.

### `top`
- Displays real-time system processes and resource usage.

### `htop`
- Displays an interactive view of system processes (requires `htop` to be installed).

### `ps`
- Displays the current processes.

### `ps aux`
- Lists all running processes with detailed information.

### `df`
- Displays disk space usage.

### `df -h`
- Displays disk space usage in human-readable format (e.g., GB, MB).

### `du -sh <directory>`
- Displays the total disk space used by a directory in a human-readable format.

### `free`
- Displays memory usage (RAM and swap).

### `free -h`
- Displays memory usage in a human-readable format.

### `whoami`
- Displays the current user.

### `id`
- Displays user and group IDs of the current user.

### `last`
- Displays the login history of users.

### `who`
- Displays who is currently logged in.

### `uptime`
- Shows how long the system has been running, along with the load averages.

### `shutdown -h now`
- Shuts down the system immediately.

### `reboot`
- Reboots the system.

### `sudo <command>`
- Executes a command with superuser (root) privileges.

### `sudo su`
- Switches to the root user (superuser).

### `sudo !!`
- Repeats the last command with `sudo` privileges.

## Package Management (Debian-based)

### `apt update`
- Updates the package list from repositories.

### `apt upgrade`
- Upgrades installed packages to their latest version.

### `apt install <package>`
- Installs a package.

### `apt remove <package>`
- Removes a package.

### `apt purge <package>`
- Removes a package and its configuration files.

### `apt search <package>`
- Searches for a package in the repositories.

### `apt show <package>`
- Displays detailed information about a package.

## Package Management (Red Hat-based)

### `yum update`
- Updates all installed packages.

### `yum install <package>`
- Installs a package.

### `yum remove <package>`
- Removes a package.

### `yum search <package>`
- Searches for a package in the repositories.

### `yum info <package>`
- Displays detailed information about a package.

## Networking Commands

### `ping <host>`
- Pings a host to check if it is reachable.

### `ifconfig`
- Displays network interfaces and their configuration.

### `ip a`
- Displays network interfaces and their configuration (alternative to `ifconfig`).

### `ip link set <interface> up`
- Brings a network interface up.

### `ip link set <interface> down`
- Brings a network interface down.

### `netstat`
- Displays network connections, routing tables, and interface statistics.

### `ss`
- Displays socket statistics (faster and more modern alternative to `netstat`).

### `traceroute <host>`
- Traces the route packets take to reach a network host.

### `dig <domain>`
- Queries DNS for information about a domain.

### `curl <url>`
- Transfers data from or to a server using various protocols (HTTP, FTP, etc.).

### `wget <url>`
- Downloads files from the web using HTTP, HTTPS, or FTP.

## Disk and Storage Management

### `lsblk`
- Lists information about block devices (disks, partitions).

### `fdisk -l`
- Lists all available disk partitions.

### `mount <device> <mount_point>`
- Mounts a device (e.g., disk or partition) to a directory.

### `umount <device>`
- Unmounts a device.

### `mkfs.ext4 <device>`
- Formats a device with the ext4 file system.

### `fsck <device>`
- Checks and repairs the file system of a device.

### `tune2fs -l <device>`
- Displays information about an ext4 file system.

## Archiving and Compression

### `tar -czvf <archive_name>.tar.gz <directory>`
- Compresses a directory into a `.tar.gz` archive.

### `tar -xzvf <archive_name>.tar.gz`
- Extracts a `.tar.gz` archive.

### `zip <archive_name>.zip <file1> <file2>`
- Compresses files into a `.zip` archive.

### `unzip <archive_name>.zip`
- Extracts a `.zip` archive.

### `gzip <file>`
- Compresses a file using the gzip compression algorithm.

### `gunzip <file.gz>`
- Decompresses a `.gz` file.

## Process Management

### `ps aux`
- Lists all running processes.

### `kill <pid>`
- Terminates a process with the specified PID.

### `kill -9 <pid>`
- Forcefully terminates a process with the specified PID.

### `pkill <process_name>`
- Kills all processes with the specified name.

### `top`
- Displays a dynamic view of system processes.

### `htop`
- Displays an interactive, enhanced version of `top`.

### `nice <command>`
- Starts a command with a specified priority (nice value).

### `renice <pid> <priority>`
- Changes the priority of an already running process.

## Disk Usage and System Monitoring

### `df -h`
- Displays disk space usage in a human-readable format.

### `du -sh <directory>`
- Displays the total disk space used by a directory in a human-readable format.

### `free -h`
- Displays memory usage in a human-readable format.

### `uptime`
- Displays how long the system has been running and the load average.

### `top`
- Displays the system’s current processes and their resource usage.

### `iostat`
- Displays CPU and I/O statistics.

### `vmstat`
- Displays system performance information.

## User Management

### `adduser <username>`
- Adds a new user to the system.

### `usermod -aG <group> <username>`
- Adds a user to a specific group.

### `passwd <username>`
- Changes the password of a user.

### `deluser <username>`
- Deletes a user from the system.

### `groupadd <groupname>`
- Adds a new group to the system.

### `groups <username>`
- Displays the groups a user belongs to.

### `whoami`
- Displays the current logged-in user.

## System Logging

### `dmesg`
- Displays kernel ring buffer messages (boot and system messages).

### `journalctl`
- Displays systemd logs.

### `tail -f /var/log/syslog`
- Displays the system log in real-time (useful for debugging).

### `cat /var/log/messages`
- Displays the system message log.

