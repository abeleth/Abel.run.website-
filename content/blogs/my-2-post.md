+++
title = 'Second post how to use them'
date = 2024-08-17T18:08:04-06:00
draft = false
+++


21. **`diff`**: To find the differences between two files, use **`diff`** followed by the file names. For example, **`diff file1.txt file2.txt`** will display the lines that differ between "file1.txt" and "file2.txt".
22. **`cmp`**: Use **`cmp`** followed by the two file names to check if two files are identical. If there is no output, it means the files are the same. For example, **`cmp file1.txt file2.txt`**.
23. **`comm`**: **`comm`** compares two sorted files line by line and displays lines that are common or unique between the files. Use **`comm`** followed by the file names. For example, **`comm file1.txt file2.txt`**.
24. **`sort`**: To sort the content of a file, use **`sort`** followed by the file name. It will display the sorted output. For example, **`sort myfile.txt`**.
25. **`export`**: To set environment variables, use **`export`** followed by the variable name and value. For example, **`export MY_VAR="Hello"`**.
26. **`zip`**: Use **`zip`** followed by the archive name and the files/directories you want to zip. For example, **`zip archive.zip file1.txt file2.txt`** will create a zip archive containing "file1.txt" and "file2.txt".
27. **`unzip`**: To extract files from a zip archive, use **`unzip`** followed by the archive name. For example, **`unzip archive.zip`**.
28. **`ssh`**: Use **`ssh`** followed by the username and the remote host to establish a secure shell connection. For example, **`ssh username@remote_host`**.
29. **`service`**: To start or stop services in Linux, use **`service`** followed by the service name and the action (start, stop, restart, etc.). For example, **`service apache2 start`** will start the Apache service.
30. **`ps`**: Use **`ps`** to display active processes. The command **`ps aux`** shows a detailed list of all processes running on the system.
31. **`kill`** and **`killall`**: To terminate a process, use **`kill`** followed by the process ID (PID). For example, **`kill 1234`**. **`killall`** allows you to terminate processes by name. For example, **`killall firefox`** will terminate all Firefox processes.
32. **`df`**: Typing **`df`** displays disk usage and filesystem information.
33. **`mount`**: Use **`mount`** to mount file systems in Linux. Provide the device or file system and the mount point. For example, **`mount /dev/sdb1 /mnt`** will mount the device **`/dev/sdb1`** to the **`/mnt`** directory.
34. **`chmod`**: To change file permissions, use **`chmod`** followed by the desired permission settings and the file/directory. For example, **`chmod 755 myfile.txt`** sets read, write, and execute permissions for the owner, and read and execute permissions for group and others.
35. **`chown`**: Use **`chown`** followed by the new owner and the file/directory to change ownership. For example, **`chown newuser myfile.txt`** changes the owner of "myfile.txt" to "newuser".
36. **`ifconfig`**: Typing **`ifconfig`** displays network interfaces and their associated IP addresses.
37. **`traceroute`**: Use **`traceroute`** followed by the destination IP or domain name to trace the network hops to reach the destination. For example, **`traceroute google.com`** will show the network path to reach Google's servers.
38. **`wget`**: To download files from the internet, use **`wget`** followed by the URL of the file you want to download. For example, **`wget https://example.com/file.txt`** will download "file.txt" from the given URL.
39. **`ufw`**: **`ufw`** is the uncomplicated firewall command in Linux. You can use it to manage the firewall rules. For example, **`ufw allow 22`** allows incoming SSH connections on port 22.
40. **`iptables`**: **`iptables`** is the base firewall utility that provides more advanced configuration options for the firewall. It allows you to define specific firewall rules and policies.
41. **`apt`**, **`pacman`**, **`yum`**, **`rpm`**: These are package managers used in different Linux distributions. You can use these commands to install, update, or remove software packages. The usage may vary depending on the specific distribution you are using.
42. **`sudo`**: To escalate privileges in Linux and execute commands with administrative privileges, prefix the command with **`sudo`**. For example, **`sudo apt-get update`** will update the package list using elevated privileges.
43. **`cal`**: Typing **`cal`** will display a command-line calendar for the current month.
44. **`alias`**: To create custom shortcuts for regularly used commands, use **`alias`** followed by the desired alias name and the command you want to associate with it. For example, **`alias ll='ls -l'`** creates an alias "ll" for the command **`ls -l`**.
45. **`dd`**: **`dd`** is used for low-level copying and conversion of data. To create a bootable USB stick, you can use **`dd`** to copy the ISO image to the USB device. For example, **`dd if=image.iso of=/dev/sdb bs=4M`** will copy the "image.iso" file to the USB device **`/dev/sdb`**.
46. **`whereis`**: Use **`whereis`** followed by the command name to locate the binary, source code, and manual pages for a command. For example, **`whereis ls`** will display the location of the "ls" command.
47. **`whatis`**: To find a brief description of what a command is used for, use **`whatis`** followed by the command name. For example, **`whatis ls`** will provide a short description of the "ls" command.
48. **`top`**: Typing **`top`** displays a live view of active processes, system usage, and resource statistics.
49. **`useradd`** and **`usermod`**: To add a new user, use **`useradd`** followed by the username. For example, **`useradd newuser`** creates a new user with the username "newuser". **`usermod`** is used to modify existing user accounts.
50. **`passwd`**: To create or update passwords for existing users, use **`passwd`** followed by the username. For example, **`passwd username`** will prompt you to enter a new password for the specified user.