Basic and Advanced Linux  Interviews Quetions and Answers

1.
What is Linux?

Hide Answer
Linux is an open-source operating system based on the Unix platform. It was first created by Linus Torvalds in 1991 and has since become one of the most popular choices for servers and embedded systems. With its stability, security, and flexibility, Linux allows users to customize and optimize their computing experience. It also supports a wide range of software and applications.

2.
Why is Linux considered more secure than other operating systems?

Hide Answer
Linux is considered more secure than other operating systems for several reasons. Firstly, Linux's open-source nature allows it to be examined and scrutinized by a vast community of developers worldwide, making it harder for potential vulnerabilities to go unnoticed.

Additionally, Linux's file and directory permissions system is stronger than that of other operating systems, granting users only the access they need to perform their tasks, and limiting the potential damage that could be done by a security breach.

Lastly, Linux distributions generally come with fewer software and components installed by default, reducing the overall attack surface of the system. All these features make Linux a solid choice for security-conscious users and organizations.

3.
What is the difference between Linux and Unix?

Hide Answer
linux and unix.webp

4.
What is the core of the Linux operating system?

Hide Answer
The core of the Linux operating system is commonly referred to as the Linux kernel. It is responsible for managing system resources, providing essential services, and facilitating communication between hardware and software components. The Linux kernel is an open-source project developed by a global community of contributors, making it highly customizable and widely used in various devices, from smartphones to servers. The kernel controls the execution of programs, manages memory, handles input/output operations, and enables communication between different components of the system

5.
How can you monitor system resource utilization on Linux? Provide a command to check CPU and memory usage.

Hide Answer
You can use the top command to monitor system resource utilization. Here's how you can check CPU and memory usage. This command will display a real-time view of system statistics. To exit, press q.

6.
What is BASH?

Hide Answer
BASH is a command-line shell and scripting language primarily used in Unix-based systems, including Linux and macOS. It stands for "Bourne Again SHell," indicating its lineage from the original Bourne shell. BASH allows users to interact with the operating system by executing commands, managing files, and automating tasks through script files. It is a powerful and flexible tool for both beginners and advanced users.

7.
What is LILO?

Hide Answer
LILO is a boot loader for Linux operating systems that stands for "LInux LOader." It is responsible for loading the operating system kernel into memory and transferring control to it. LILO is one of the oldest boot loaders in use on Linux systems and has been largely replaced by GRUB (Grand Unified Bootloader) as the preferred boot loader due to its support for contemporary hardware and more advanced features.

8.
Why is the GNU project important?

Hide Answer
The GNU project was started with the goal of creating a free functioning framework for clients. Clients would be able to test, share, circulate, study, update, and improve the product, as well as bring out new features.

The goal of this project was to provide a free functional framework that included "everything valuable that generally accompanies a UNIX framework so that one could get by with no product that wasn't free."

Every other component of the Linux framework, with the exception of the piece, is GNU. It was taken under GNU variation 2 and the name Linux was changed to GNU/Linux as a result.

9.
How can you check the current working directory in a Linux shell script and store it in a variable?

Hide Answer
linux-shell-script.webp

10.
Mention the maximum length for a filename allowed in Linux.

Hide Answer
Linux allows a maximum length of 255 characters for any filename, excluding the pathname. This furthest point does not include the pathname, therefore the total pathname and filename length might easily exceed 255 characters.

Make sure that you mention the exclusion of pathname, as in a Linux interview, the interviewer would definitely ask you about the pathname.

11.
Why do we use LINUX?

Hide Answer
There are several reasons why people choose to use the Linux operating system. To begin with, Linux is known for its stability and security, making it ideal for both personal and professional use. Additionally, Linux also provides a wide range of customization options, allowing users to tailor the system to their specific needs. Furthermore, Linux is an open-source platform, meaning that the source code is available to anyone who wants to modify or enhance it. This promotes a collaborative and innovative community, constantly improving the system. Lastly, Linux offers a variety of distributions, catering to different user preferences and requirements. Overall, Linux provides a powerful and flexible alternative to other operating systems.

12.
Guide me through the Linux boot process, i.e, from when you press the power button to when the Linux login prompt appears.

Hide Answer
These are the six stages of Linux boot process:

BIOS: BIOS or Basic input/output system examines the integrity of the system and looks for the boot loader program on the CD-ROM or hard drive to load and run it. The BIOS grants control to the boot loader program after it has been discovered and loaded into memory. So, in a nutshell, the BIOS loads and executes the MBR bootloader.
MBR: Master Boot Record (MBR) may be found on the bootable disk's first sector. Usually found in dev/hda or dev/sda. It contains GRUB-related information (Grand Unified Bootloader). So, in a nutshell, the MBR loads and runs the GRUB boot loader.
GRUB: The default kernel image given in the grub configuration file is loaded by GRUB. /boot/grub/grub.conf is the location of the grub configuration file. It consists mostly of the kernel and the initrd image (initial ram disc - a method of loading a temporary root file system into memory). In a nutshell, GRUB loads and runs kernel and initrd images.
Kernel: The root file system is mounted, and the /sbin/init program is run. The process id of init is 1 since it is the first program to be executed by the kernel. To double-check, run ps -ef | grep init.
Init: Init determines the Linux run level by looking at the /etc/inittab file. In Linux, the following run levels are available:
halt

Single-user mode

Multi-user mode

Full Multi-user mode

Unused

X11

reboot

Runlevel: Various services may be seen launching up as the Linux system is powering up. These are the runlevel programs, which are executed from the run level directory according to the run level's specifications.
13.
How would you approach the problem of strengthening the security of password files?

Hide Answer
In such Linux interview questions, make sure you talk about how you would approach and solve the problem. If you have any prior experience in solving such issues yourself, that would be a valuable addition in answering this Linux interview question.

/etc/passwd is a text file that Linux uses to store user account information. A one-way encrypted password is also stored in this file. It is accessible by numerous programs to obtain user information, posing a security concern; hence, the file must be 'Word Readable.' We may utilize the shadow password format to reduce the security risk. This approach stores account information in the /etc/passwd file on a regular basis.

The password, on the other hand, is saved as a single "x" character (not actually stored in this file). A second file, "/etc/shadow," stores encrypted passwords as well as other data such as account or password expiration values, and so on. Because the /etc/shadow file is only accessible by the root account, it poses less of a security concern.

14.
In order to secure an ssh connection, what are the basic measures that you need to take?

Hide Answer
Using ssh to connect to servers is extremely frequent. As a result, you can take the following measures to protect the SSH service:

Disabling root login, as well as password-based logins, will improve the server's security.
Disabling password-based logins and permitting key-based logins, which are safe but may be further restricted by only allowing access from specific IP addresses.
Changing the default port to anything else reduces the number of random brute force attacks from the internet.
By requiring the service to use only version 2 of the protocol, security and functionality enhancements will be introduced.
The whitelist strategy may be used, where only people on a certain list are allowed to connect to the server through SSH.
15.
What is the disadvantage of Open Source?

Hide Answer
There are a few disadvantages of open source:

One is the potential lack of support and troubleshooting. Since open source projects are often community-driven, there may not always be dedicated technical support available.
Another disadvantage is the potential for security vulnerabilities if the open source software is not regularly maintained and updated.
Lastly, open source may lack certain features or functionalities that proprietary software may have.
16.
How does a system administrator know whether or not a user account is locked?

Hide Answer
Run the following command in the shell to see if the user account is locked:

passwd –S

Another way is to look for the grep username in the /etc/shadow file, which will add a symbol '!' to the encrypted field in the password box.

Type the following command to simply unlock the password:

passwd –u

Run the following command twice, if there is a double exclamation mark:

usermod –U

17.
List down the steps for how to find out Linux's memory use.

Hide Answer
To find out how much memory Linux is using, use the "Concatenate" command in the Linux shell.

When you use this command, you'll get a list of memory usages by Linux, including Total Memory, Free Memory, Cache Memory, and many others. Other Linux commands include:

$ free –m // this is the most basic command that displays memory use in megabytes
$ vmstat –s // this command generates a virtual memory statistics report
top // this command examines memory and CPU use
htop // this command is very similar to the top command
18.
What is Shell?

Hide Answer
The Shell is a command line interpreter that allows you to interact with the computer's operating system. It provides a way for you to give instructions to the computer by typing commands. The Shell takes these commands and acts as a bridge between the user and the operating system, executing the commands and providing feedback and results. It is a powerful tool for managing files, running programs, and automating tasks.

19.
How many types of Shells are there in Linux?

Hide Answer
Bash (Bourne Again SHell)
Csh (C SHell)
Tcsh (TENEX C Shell)
Ksh (Korn SHell)
Zsh (Z SHell)
Each shell has its own unique features and capabilities, so users can choose the one that best suits their needs and preferences.

20.
What are the basic components of Linux?

Hide Answer
Linux has three major components:

The kernel which is responsible for managing hardware resources and memory allocation,
The shell which is responsible for managing user input and output
The utilities which provide additional functionality to interact with the kernel and shell.
These components work together to provide a robust and flexible operating system suitable for a wide range of applications and devices.

21.
How can you change the permissions of a file named "file.txt" to give read, write, and execute permissions to the owner, and only read permission to others?

Hide Answer
Assuming you want to give read, write, and execute permissions to the owner, and only read permission to others, you can use the following command:

chmod 750 file.txt

This command will set the permissions of "file.txt" as desired.The first digit (7) refers to the owner's permissions (read, write, and execute)

The second digit (5) refers to the group permissions (read and execute only)
The third digit (0) refers to the permissions for others (no permissions)
22.
Create a symbolic link named "mylink" that points to a file named "target.txt" using the ln command.

Hide Answer
To create a symbolic link named "mylink" that points to a file named "target.txt" using the ln command, you can use the following command:

ln -s target.txt mylink

This will create a symbolic link called "mylink" that points to the file "target.txt" in the current directory.

23.
What is the GUI?

Hide Answer
The GUI, or Graphical User Interface, is a visual interface that allows users to interact with a computer system through icons, menus, and windows. Instead of using command lines, a GUI provides a more user-friendly way to navigate and use software applications. It simplifies the user experience by using visual elements that are familiar and easy to understand.

24.
Explain File Permissions types in Linux?

Hide Answer
Read: Allows a user to view the contents of a file.
Write: Allows a user to modify the contents of a file.
Execute: Allows a user to execute a file as a program.
These permissions can be assigned to three categories: owner, group, and others. Permissions can be viewed using the ls -l command and modified using the chmod command.

25.
What are the environmental variables?

Hide Answer
Environmental variables are dynamic values that can affect the behavior of software running on a system. They are stored in the operating system and can be accessed and modified by software applications. Common examples include the PATH variable, which tells the system where to look for executables, and the HOME variable, which defines the default user directory. Environmental variables are useful for customizing the software environment and improving compatibility.

26.
What are the symbolic links?

Hide Answer
Symbolic links, also known as soft links, are files that act as pointers to another file or directory within a file system. They are commonly used in Unix-based systems as a way to create shortcuts to files and directories, allowing for easier navigation and organization. A symbolic link appears to be a regular file or folder, but it only contains a path to the original file or folder, rather than actual data.

27.
What are the hard links?

Hide Answer
Hard links are file system links that point directly to an inode, or index node, of a file. They provide multiple directory entries for the same file, allowing it to be accessed from different locations. Unlike symbolic links, hard links do not maintain a separate file path; they refer to the same physical data. This means changes made to one hard link will be reflected in all other hard links to the same file.

28.
What is redirection?

Hide Answer
Redirection is the process of sending the output of a command to a file or another command instead of the default output destination (console). This allows you to save the output in a file for later use or to send it as input to another command.

29.
What are Daemons?

Hide Answer
In Linux, daemons are background processes that run continuously, providing specific services to other applications or users. They usually start during system boot and do not require any user intervention. Daemons are often used to handle network services, such as web servers (Apache), email servers (Postfix), or database servers (MySQL).

30.
Describe the root account.

Hide Answer
The root account is the highest level of administrative privileges in Linux. It has complete control over the system and can perform any task, including modifying system files, installing software, and creating/deleting user accounts. It is recommended to use the root account sparingly and instead use sudo (Superuser Do) to execute commands with elevated privileges.

31.
Write a command to show the first 10 lines of a text file named "example.txt."

Hide Answer
To show the first 10 lines of a text file named "example.txt" in Linux, you can use the head command with the -n option. Here's the command:

head -n 10 example.txt

This will display the first 10 lines of the "example.txt" file.

32.
What are the different modes when using the vi editor?

Hide Answer
When using the vi editor, there are three modes:

Command mode: This is the default mode when you start vi. It allows you to navigate and operate on the text.
Insert mode: In this mode, you can enter and edit text. Pressing the "i" key switches to insert mode.
Visual mode: This mode is used for selecting or highlighting text. Pressing the "v" key switches to visual mode.
33.
What are inode and process id?

Hide Answer
The inode (index node) is a data structure in a Unix-like file system that stores information about a file, such as its permissions, size, modification time, and the location of its data blocks.

A process ID (PID) is a unique numeric identifier assigned to each running process in Linux. It is used by the operating system to track and manage processes. The PID is essential for performing process-related operations, such as sending signals or terminating a process.

34.
What are the Process states in Linux?

Hide Answer
In Linux, a process can be in one of the following states:

Running: The process is actively executing on the CPU.
Sleeping: The process is waiting for an event, such as I/O completion.
Stopped: The process has been stopped, either by a user or a signal.
Zombie: The process has completed execution but still has an entry in the process table. It is waiting for its parent process to acknowledge its termination.
35.
Explain Process Management System Calls in Linux.

Hide Answer
Process Management System Calls are a set of functions provided by the Linux kernel to manage processes. They include functions such as fork(), exec(), wait(), and kill(), which allow creating new processes, executing programs, waiting for process termination, and sending signals to processes.

36.
What is a File system in Linux? Explain different file system types in Linux

Hide Answer
A file system in Linux is a method used to organize and store files and directories on a storage device such as a hard disk. It provides mechanisms for creating, modifying, and deleting files, it also manages access permissions, file attributes, and directory structures.

There are several types of file systems in Linux, including,

ext4: The default file system for most Linux distributions. It provides good performance, scalability, and support for large file sizes.
ext3: The predecessor to ext4, it is compatible with ext4 and offers journaling for improved reliability.
XFS: Designed for high-performance systems, XFS supports large storage and file systems. It includes features like online resizing and snapshot support.
Btrfs: A copy-on-write file system with advanced features like RAID, snapshots, and volume management. It is still under development but offers experimental support in some distributions.
NTFS: Although primarily used by Windows, Linux also has NTFS support to read and write files on NTFS partitions.
37.
How can you mount a partition with the NTFS file system type in read-write mode in Linux?

Hide Answer
To mount a partition with the NTFS file system type in read-write mode, you can use the mount command with the -o option. For example:

mount -t ntfs-3g /dev/sdX1 /mnt/ntfs

This command mounts the NTFS partition on /dev/sdX1 to the /mnt/ntfs directory in read-write mode using the ntfs-3g driver.

38.
Why is LVM required?

Hide Answer
Logical Volume Manager (LVM) is required in Linux for several reasons, like:

Flexibility: LVM provides a flexible approach to managing storage by abstracting physical disks and allowing for dynamic resizing of logical volumes without unmounting the file system.

Volume management: LVM simplifies storage management by providing features like volume grouping, resizing, snapshotting, and mirroring.

Storage efficiency: LVM enables the efficient utilization of available storage space by allowing logical volumes to span multiple physical disks.

39.
What is umask?

Hide Answer
Umask is a 3-digit octal value used to determine the default permissions for newly created files and directories in Linux. The mask value is subtracted from the base permission set to determine permissions.

40.
How to set the mask permanently for a user?

Hide Answer
To set the umask permanently for a user, the umask value can be modified in the user's shell profile configuration file such as .bashrc or .bash_profile. The umask value is set using the umask command with the desired octal value.

41.
What is network bonding in Linux?

Hide Answer
Network bonding, also known as link aggregation or NIC teaming, is a technique in Linux that allows multiple network interfaces to act as a single bonded interface. This provides increased bandwidth, fault tolerance, and load balancing.

42.
What are the different modes of Network bonding in Linux?

Hide Answer
The different modes of network bonding in Linux are:

Mode 0 (Round-robin): Packets are transmitted sequentially over each bonded interface in a round-robin fashion.
Mode 1 (Active-standby): One interface is active while the other is in standby mode for failover.
Mode 2 (Load balancing): Load balancing is based on a hashing algorithm of source and destination MAC addresses, IP addresses, and port numbers.
Mode 3 (Broadcast): All interfaces in the bond participate in transmitting and receiving packets.
Mode 4 (IEEE 802.3ad): Implements the IEEE 802.3ad Link Aggregation Control Protocol (LACP) for dynamic link aggregation.
43.
How to check the default route and routing table?

Hide Answer
To check the default route and routing table in Linux, you can use the ip route show or netstat -nr command. These commands display the routing table, including the default route (0.0.0.0/0).

44.
How to check which ports are listening in my Linux Server?

Hide Answer
To check which ports are listening on a Linux server, you can use the netstat or ss command with appropriate options. For example, netstat -tuln or ss -tuln will display TCP and UDP listening ports.

45.
Explain what a Linux kernel module is and provide an example of how to write one.

Hide Answer
A Linux kernel module is a piece of code that can be dynamically loaded and unloaded into the Linux kernel at runtime, without requiring a reboot. It can extend or modify the kernel's functionality. Here's an example of a simple "Hello World" kernel module:

linux kernel module.webp

46.
How to change the default run level in Linux?

Hide Answer
The method to change the default run level in Linux depends on the distribution. In most modern distributions that use systemd, you can use the systemctl command to change the default run level. For example, to set the default run level to multi-user.target (equivalent to runlevel 3), you can use the command sudo systemctl set-default multi-user.target. In older distributions that use SysV init, you can modify the /etc/inittab file to change the default run level.

Looking for remote developer job at US companies?
Work at Fortune 500 companies and fast-scaling startups from the comfort of your home

Apply Now
INTERMEDIATE LINUX INTERVIEW QUESTIONS AND ANSWERS
1.
Mention the default ports used for DHCP, SSH, SMTP, DNS, FTP, and squid?

Hide Answer
Default ports used for:

SMTP (Simple Mail Transfer Protocol):

Port: 25
Used for sending email.
DNS (Domain Name System):

Port: 53
Converts domain names to IP addresses.
FTP (File Transfer Protocol):

Ports: 20 (Data), 21 (Control)
Used for file transfers.
DHCP (Dynamic Host Configuration Protocol):

Ports: UDP 67 (Server), UDP 68 (Client)
Assigns IP addresses automatically.
SSH (Secure Shell):

Port: 22
Provides secure remote access.
Squid (Proxy Server):

Port: 3128
Acts as an intermediary for web requests.
2.
How to lock a user account in Linux?

Hide Answer
To lock a user account in Linux, you can use the 'passwd' command with the '-l' option, followed by the username. This will lock the specified user account.

sudo passwd -l username

3.
What is the 'ls' command? How can you use the 'ls' command to display hidden files and directories?

Hide Answer
The 'ls' command is used to list files and directories in Linux. It provides information such as permissions, ownership, size, and modification time of the files/directories in a specified location. To display hidden files and directories, you can use the '-a' or '--all' option with the 'ls' command. For example, ls -a or ls --all will show both visible and hidden files and directories in the current directory.

ls /path/to/directory

4.
What is the tail command in Linux? How can you display the last 10 lines of a file using 'tail'?

Hide Answer
The 'tail' command is used to display the last n lines of a file in Linux. By default, it shows the last 10 lines of a file.

tail -n <number_of_lines> filename

To display the last 10 lines of a file using 'tail', you can use the following command:

tail -n 10 filename

5.
What is grep command in Linux? How do you use grep to search for a specific word in a single file?

Hide Answer
The 'grep' command is used for searching patterns in files. It can be used to extract lines that match a specific pattern or regular expression.

grep "pattern" filename

You can use the following command to search for a specific word (e.g., "search_term") in a single file:

grep "search_term" filename

6.
What is the ps command in Linux? How can you display a hierarchical view of processes using the ps command?

Hide Answer
The 'ps' command is used to display information about the running processes in Linux. By default, it shows the processes of the current user.

You can use the ps -e --forest command to display processes in a hierarchical tree-like structure, showing parent-child relationships between processes.

7.
What is the env command in Linux? How can you use the 'env' command to unset an environment variable?

Hide Answer
The 'env' command is used to display the current environment variables in Linux.

You can use the 'env' command to unset an environment variable by setting it to an empty value. For example, to unset a variable named 'VAR_NAME,' you can do the following:

env VAR_NAME= your_command

8.
What is the top Command in Linux? How can you start the 'top' command in Linux, and are there any useful command-line options to customize its behavior?

Hide Answer
The 'top' command is used to monitor the system in real-time. It provides a dynamic view of the processes running on the system, sorted by their resource consumption.

You can start the 'top' command by opening a terminal and simply typing 'top' and pressing Enter. To customize its behavior, you can use various command-line options. For example:

top commands linux.webp

9.
What is the netstat command in Linux? How can you view all established connections with netstat?

Hide Answer
The 'netstat' command is used to display network connections and routing tables. It provides information about active network connections, listening ports, and various network interfaces.

To view all established connections, you can use the following command:

netstat -tuln | grep 'ESTABLISHED'

This command lists all established TCP connections.

10.
What is lsof command in Linux? How can you install 'lsof' on a Linux system if it's not already installed?

Hide Answer
The 'lsof' command is used to list open files and the processes that have opened them. It can also display network connections, file descriptors, and other related information.

You can typically install 'lsof' on a Linux system using your system's package manager. For example, on Debian-based systems like Ubuntu, you can use the following command:

sudo apt-get install lsof

On Red Hat-based systems like CentOS or Fedora, you can use 'yum' or 'dnf':

sudo yum install lsof

11.
Explain about chmod command?

Hide Answer
The chmod command in Linux is used to change the permissions of a file or directory. chmod stands for "change mode." The command allows you to set permissions for three different types of users: the owner of the file, the group that the file belongs to, and all other users.

The chmod command uses a combination of letters and numbers to set permissions. The letters 'r', 'w', and 'x' represent read, write, and execute permissions, respectively. The numbers 4, 2, and 1 are used to calculate the total permissions for each user type.

For example, chmod 752 filename will give the owner read, write, and execute permissions, the group read and execute permissions, and all other users read permissions.

12.
Explain about the chown command?

Hide Answer
The chown command in Linux is used to change the ownership of files and directories. It allows you to transfer the ownership of a file or a directory from its current owner to a new owner. In order to use this command, you must be the owner of the file or directory, or you should have root privileges. The syntax of the command is chown [user][:[group]] file, where the user is the new owner of the file and :[group] specifies the group to which the file belongs. If you omit the group, the file will be owned by the user specified and the file's group will remain unchanged. The chown command is a powerful tool that can be used to manage file permissions and access rights.

13.
What is the cp command in Linux?

Hide Answer
The cp command, short for "copy", is a command in Linux that allows the user to create copies of files and directories. This command can be used to duplicate a single file or an entire directory of files, and can be done either within the same location or between different directories. Additionally, the cp command can be used to preserve file attributes such as timestamps, permissions, and ownership. The cp command is a fundamental tool in Linux, commonly used in everyday tasks and administrative tasks, making it a key command for anyone who works with Linux systems.

14.
How to remove a file or directory from the system in Linux?

Hide Answer
To remove a file or directory in Linux, you can use the command "rm". To remove a file, you can use the command followed by the name of the file you want to delete. For example, "rm filename.txt" will delete the file named "filename.txt". However, if you want to remove a directory, you need to add the "-r" flag to the command to remove the directory and all its contents. For example, "rm -r directoryname" will delete the directory named "directoryname" and any files or directories it contains. Note that these commands can permanently delete files and directories, so use them with caution.

15.
What is mkdir in Linux?

Hide Answer
mkdir stands for "make directory" and is a command in Linux used to create new directories (or folders) within the file system. When you execute the mkdir command followed by a directory name, it creates a new directory with that name in the current working directory. You can also specify a complete path to create a directory in a specific location.

For example, mkdir /home/user/documents would create a directory named "documents" within the "user" directory, which is inside the "home" directory. mkdir is a simple but useful command for organizing and managing your files in Linux.

16.
Explain rmdir command in Linux?

Hide Answer
The rmdir command in Linux removes an empty directory from the file system. It is a simple command that only requires specifying the name of the directory to be removed. This command does not work for removing a directory that has contents in it as it will trigger an error.

The syntax for the rmdir command is rmdir [option(s)] directory_name. Some useful options that can be used with the command include -p which allows the removal of parent directories, and -v which enables verbose output.

Overall, the rmdir command is a handy tool for quickly cleaning up empty directories on a Linux system.

17.
How to exit from vi editors?

Hide Answer
To exit from the vi editor, you can use the following steps:

Ensure you are in the command mode by pressing the Esc key.
Type :q and press Enter to quit vi if you have not changed the file.
If you have made changes and want to exit without saving, type :q! and press Enter.
To save any changes you have made and exit, type :wq and press Enter.
If you are experiencing difficulties or want to exit without saving changes, you can also force vi to quit by pressing Ctrl + C twice in quick succession.
18.
How to delete information from a file in vi?

Hide Answer
To delete information from a file using vi, you can use the "delete" or "yank" commands. To delete a single character, move the cursor to that character and press the "x" key. To delete an entire line, move the cursor to the line and press the "dd" keys.

If you want to delete multiple lines, press the "Esc" key to enter command mode, then type the range of lines you want to delete followed by "dd". For example, to delete lines 5 through 8, type "5,8dd" and press enter. To undo a deletion, press the "u" key.

19.
Enlist some Linux to file content commands.

Hide Answer
Here are some common Linux commands to manipulate and view file content:

cat: Concatenate and display file contents.
head: Display the first few lines of a file.
tail: Display the last few lines of a file.
less: View file contents page by page.
grep: Search for specific patterns in a file.
wc: Count the number of lines, words, and characters in a file.
sed: Stream editor for filtering and transforming text.
awk: Text processing tool for manipulating and extracting data from files.
cut: Cut out selected portions of a file.
sort: Sort the lines of a file.
20.
Enlist some Linux distributors (Distros) along with their usage.

Hide Answer
Here are some of the most popular Linux Distributions (Distros) along with their usage:

Ubuntu: This is one of the most popular Linux distros and is known for its user-friendly interface. It is used for personal use as well as servers.
Debian: One of the oldest Linux distros, Debian is known for its stability and reliability. It is typically used for servers and workstations.
Red Hat Enterprise Linux (RHEL): One of the most widely used Enterprise Linux distros, it is designed for mission-critical systems. It is often used in corporate environments where stability and support are crucial.
CentOS: This open-source community-based distro is known for its stability, security, and long-term support. It is commonly used for servers and web hosts.
Fedora: This is a community-based version of Red Hat that offers newer versions of software than RHEL5. It is a popular choice for developers and has a shorter release cycle than RHEL.
21.
Write a Bash script that checks if a user exists on the system.

Hide Answer
Here is a simple Bash script that checks if a user exists on the system:

bash script.webp

You can save this script in a file, for example check_user.sh. Then, make the file executable by running chmod +x check_user.sh. Now you can run the script by executing ./check_user.sh and it will prompt you to enter a username. After entering a username, it will check if the user exists on the system and display a corresponding message.

22.
Write a Bash script that checks if a given process is running and prints a message accordingly.

Hide Answer
Here's a simple Bash script that checks if a given process is running and prints a message accordingly:

Image 21-09-23 at 6.09 PM.webp

To use this script, replace your_process_name with the actual name of the process you want to check. Save the script to a file (e.g., check_process.sh), make it executable using chmod +x check_process.sh, and run it using ./check_process.sh.

The script uses the pgrep command to check if the process is running by searching for its exact name. If the process is found, it prints a message indicating that it is running. Otherwise, it prints a message indicating that it is not running.

23.
Differentiate between BASH and DOS?

Hide Answer
BASH (Bourne Again SHell) and DOS (Disk Operating System) are both command line interfaces used to interact with the operating system. However, there are some key differences between them.

Syntax: BASH follows the syntax of Unix-like operating systems, while DOS uses a different syntax.
Compatibility: BASH is primarily used on Unix-like systems such as Linux, while DOS is mainly used on Windows systems.
Features: BASH offers advanced features like scripting, command substitution, and piping, while DOS has simpler commands and a limited set of features.
File system: BASH supports a hierarchical file system, while DOS uses a flat file system.
In summary, BASH is more powerful and flexible, while DOS is simpler and more limited in functionality.

24.
What is meant by internal commands and external commands?

Hide Answer
Internal commands and external commands are terms used in computing. Internal commands are built into the operating system of a computer, and are a part of its functionality. These commands are typically small, and help the user to perform basic functions like copy, move, and delete files. External commands, on the other hand, are programs or utilities that are not part of the operating system. They need to be installed separately, and offer a wider range of functions. External commands often provide additional functionality, such as compression or encryption, that is not available with internal commands. Overall, both types of commands are essential for users to perform various tasks on their computers.

25.
What is meant by PIPE in Linux?

Hide Answer
In Linux, a PIPE is a mechanism that allows the output of one command to be supplied as input to another command. It is a form of interprocess communication that allows separate processes to communicate with each other without the need for intermediate files. The PIPE command '|' is used to create a pipeline that connects a series of commands. For example, if we want to take the output of the 'ls' command and then sort it alphabetically, we could use the command 'ls | sort'. This would take the output from the 'ls' command and pipe it to the 'sort' command for sorting. Piping is a powerful function in Linux that enables commands to work together in powerful ways.

26.
Describe how a parent and child process communicate with each other.

Hide Answer
In a computer system, a parent process and a child process can communicate with each other using various interprocess communication mechanisms. One common method is through pipes, which allow the parent and child to share data by writing to and reading from the pipe.

Another way is through shared memory, where both processes can access and modify a common memory region. Additionally, they can use signals to notify each other about specific events. The parent process can send a signal to the child process, and the child process can handle the signal to perform a certain action. Overall, these communication mechanisms enable effective coordination and information sharing between the parent and child processes.

27.
What is a Stateless Linux Server? Explain the features of Stateless Linux Server?

Hide Answer
A stateless Linux server is a type of server that does not retain any user-specific data or configuration settings. It operates without persistent storage, meaning that upon reboot, all previous data and settings are lost. This type of server typically relies on network-based storage, such as a network file system (NFS) or Internet Small Computer System Interface (iSCSI), to provide necessary files and resources. Stateless Linux servers are highly scalable and can be easily deployed and replicated. They are commonly used in cloud computing environments where quick provisioning and easy management are essential. By being stateless, these servers offer increased flexibility and simplicity in deployment and administration.
This configuration offers several benefits:

Easy Scalability: Stateless servers can be easily replicated and deployed in a distributed system, ensuring high availability and load balancing.
Simplified Maintenance: With no local data, it becomes easier to update or replace a server without impacting the system's overall functionality.
Enhanced Security: Since there is no local storage, there is a reduced risk of sensitive information being compromised if a server is compromised.
Streamlined Configuration Management: Stateless servers can be quickly and uniformly configured using automation tools, leading to improved efficiency and consistency in deployments.
28.
How do you ensure data consistency and synchronization among stateless server instances in a distributed system?

Hide Answer
To ensure data consistency and synchronization among stateless server instances in a distributed system, one can employ techniques like distributed databases, distributed caches, or distributed consensus protocols like Paxos or Raft. These approaches enable servers to share and update data in a coordinated manner, maintaining consistency even in the face of failures or network issues.

Additionally, versioning, timestamping, and conflict resolution mechanisms can help reconcile conflicting updates. Load balancers and service discovery tools can ensure clients connect to available instances. Regular data replication and periodic consistency checks further bolster data integrity, making the distributed system robust and reliable.

29.
What is Zombie Process? Can Zombie Processes cause any issues or performance problems on a Linux system?

Hide Answer
A Zombie Process is a type of process that has completed its execution but still has an entry in the process table. In other words, it's a process that has terminated, but its parent process has not yet received its status. This usually happens when the parent process fails to invoke the wait system call after its child has completed execution. As a result, the operating system cannot remove the entry from the process table, and the terminated child process remains in a zombie state as a dormant process. Zombie processes occupy system resources and can lead to performance degradation if not taken care of in time.

Zombie Processes, by themselves, do not cause performance problems or issues on a Linux system. However, if a large number of zombies accumulate and are not reaped by their parent processes, they can consume entries in the process table, potentially leading to resource exhaustion.

30.
Explain the work of the Ctrl+Alt+Del key combination on the Linux operating system?

Hide Answer
The Ctrl+Alt+Del key combination on Linux system is typically used to perform a system reboot or shutdown. However, this is not a default key combination on most Linux distributions. On Linux operating system, the Ctrl+Alt+Del combination can be configured through the systemd software suite. This suite provides a central management system for systems and service configuration. In order to configure this key combination, the user must create a custom systemd target file. Once created and properly configured, this key combination can be used as intended to initiate a system reboot or shutdown, working similar to the traditional means on Windows or other operating systems.

31.
Write a script that takes a directory path as an argument and lists all the files in that directory.

Hide Answer
Here's a sample Linux script that lists all the files in a given directory:

directory path.webp

To use this script, you can save it in a file, e.g., list_files.sh. Then, give it execute permissions by running chmod +x list_files.sh. Finally, you can execute the script by running ./list_files.sh /path/to/directory where /path/to/directory is the directory for which you want to list the files.

32.
Can you specify a different number of lines to be displayed with the 'tail' command? If so, how?

Hide Answer
Yes, the 'tail' command allows you to specify the number of lines to be displayed. By default, it displays the last 10 lines of a file. However, you can change this behavior by using the '-n' option followed by the desired number of lines.

For example, to display the last 5 lines, you would use the command 'tail -n 5 filename'. This will show the last 5 lines of the specified file. You can adjust the number as needed to display a different number of lines.

33.
Is it possible to use the 'cat' command to create a new file or overwrite an existing file? If so, how?

Hide Answer
Yes, it is possible to use the 'cat' command to create a new file or overwrite an existing file. To create a new file using 'cat', you can run cat > filename.txt and then start typing the content of the file. Press Ctrl + D to save and exit. This will create a new file with the specified name. To overwrite an existing file, you can run cat > existing_file.txt and then type the new content you want to overwrite with. Again, press Ctrl + D to save and exit. This will replace the content of the existing file with the new content you provided.

34.
How can you use the grep command to perform a case-insensitive search?

Hide Answer
To perform a case-insensitive search using the grep command, you can use the -i option. By adding -i before the search pattern, grep will ignore the case of the letters and match both uppercase and lowercase versions of the pattern.

For example, to search for the word "example" in a file called "text.txt" without considering the case, you can use the following command:

grep -i 'example' text.txt

This will display all the lines in "text.txt" that contain the word "example" regardless of the case used.

35.
What is the top Command in Linux?

Hide Answer
The top command is a powerful utility in Linux that provides a real-time view of running processes and resource usage on a system. With its user-friendly display, it can show vital information such as CPU usage, memory usage, and the list of processes managed by the Linux Kernel. top also supports features like color customization, highlighting, and even elementary graphs for better visualization. It can be used to monitor system performance, troubleshoot performance issues, and identify resource-hungry processes. Overall, top is a valuable command for system monitoring and management in Linux environments.

Looking for remote developer job at US companies?
Work at Fortune 500 companies and fast-scaling startups from the comfort of your home

Apply Now
ADVANCED LINUX INTERVIEW QUESTIONS AND ANSWERS
1.
How are shadow passwords given in Linux?

Hide Answer
In Linux, shadow passwords are given by storing the hashed passwords in a separate file /etc/shadow instead of storing them in the world-readable file /etc/passwd . Access to the shadow file is restricted to privileged users only.

The /etc/shadow file contains one entry per line for each user listed in the /etc/passwd file. Each line in /etc/shadow consists of nine fields, separated by colons ( : ), with the fields having the following meanings:

Login name
Password hash
Date of the last password change
Password minimum age
Password maximum age
Password warning period
Password inactivity period
Account expiration date
A reserved field for future use
To create and manage shadow passwords, the passwd command can be used which will encrypt the password using a hashing algorithm such as MD5, SHA-256 or SHA-512 and store it in the /etc/shadow file .

2.
What daemon is used for scheduling commands?

Hide Answer
The daemon used for scheduling commands in Linux is typically cron. Cron (short for chronograph) is a time-based job scheduler in Unix-like operating systems that is used to schedule commands or scripts to run automatically at specified intervals of time or dates. It runs in the background as a daemon process and triggers commands at the appropriate time according to the specified schedule.

Cron relies on a file called crontab, which is a table of commands with their specific execution times. The crontab file is edited using the crontab command and can be customized to include specific schedules for running commands or scripts.

Furthermore, there is another daemon for scheduling commands in Linux called at. The at daemon allows you to schedule a one-time task that will run at a specific scheduled time. The commands and tasks that are scheduled with the at daemon are stored in a queue, where each task will run at its designated time.

Both cron and at daemons are commonly used in Linux for scheduling commands and tasks based on specific timeframes.

3.
Write a shell script that takes a filename as an argument and checks if the file exists in the current directory. If it exists, display a message indicating its presence; otherwise, show an error message.

Hide Answer
Here is a sample shell script that checks if the file exists in the current directory and displays the appropriate message:

Image 21-09-23 at 6.28 PM.webp

4.
What shell does a Linux Administrator assign to a POP3 mail-only account?

Hide Answer
A Linux Administrator typically assigns the /bin/false shell to a POP3 mail-only account.

This shell is commonly used when you want to provide a user with mail access only and prevent them from having shell access to the system.

Please note that assigning the /bin/false shell ensures that the user cannot log in to the system using that account.

5.
If a volume group named VG0 already exists and we need to extend this volume group up to 4 GB, how do we do it?

Hide Answer
To extend an existing Linux volume group named VG0 up to 4 GB, you can follow these general steps:

Check the available space in the Volume Group: Use the vgdisplay command to check the current available space in the VG0.
Allocate additional physical volumes: If there are no available physical volumes, you may need to add new physical volumes to the volume group. You can use the **pvcreate **command to initialize the new physical volumes.
Add the new physical volumes to the volume group: Once the physical volumes are created, you can use the vgextend command to add them to the existing VG0.
Resize the logical volume(s): After extending the volume group, you can resize the logical volume(s) within it to allocate the desired additional space. Use the lvresize command to resize the logical volume(s) within VG0.
Resize the underlying filesystem: Once the logical volume(s) are resized, you may need to resize the filesystem(s) within them to make use of the additional space. Depending on the filesystem type, you can use commands like resize2fs for ext-based filesystems or xfs_growfs for XFS filesystems.
6.
Is there any relation between the modprobe.conf file and network devices?

Hide Answer
Yes, there is a relation between the modprobe.conf file and network devices. The modprobe.conf file is used in Linux systems to specify various module options and dependencies. Network devices in Linux are often managed by kernel modules or drivers.

By configuring the modprobe.conf file, you can specify the behavior of the kernel modules related to network devices. This includes specifying options for network device drivers, enabling or disabling specific modules, and setting parameters for network interfaces.

Overall, the modprobe.conf file plays a role in managing and configuring network devices by controlling the behavior of kernel modules related to networking.

7.
What is YUM? How does YUM handle package dependencies in Linux?

Hide Answer
YUM stands for Yellowdog Updater Modifier and it is a package management utility commonly used in Linux operating systems. YUM enables users to easily manage software packages by providing a user-friendly interface for installing, updating, and removing packages. With YUM, you can search for specific packages, resolve dependencies, and handle package repositories. It is widely used in Red Hat-based distributions such as CentOS and Fedora.

YUM handles package dependencies by automatically resolving and installing the required packages when you request the installation or update of a particular software package. It checks the package database and retrieves the necessary dependencies from configured software repositories, ensuring that the software functions correctly.

8.
What is the role of Kudzu? Are there any alternatives to Linux Kudzu for hardware detection and configuration in modern Linux systems?

Hide Answer
Kudzu is a program that runs on the Linux operating system. Its main role is to detect and configure hardware changes that occur on a computer system. When new hardware is added or removed from a system, Kudzu detects these changes and takes appropriate action to configure the system to work with the new hardware. For example, if a new network card is added to a system, Kudzu will detect it and configure the system to use the new card. Similarly, when the hardware is unplugged or removed from the system, Kudzu will detect this and make any necessary configuration changes.

Yes, in modern Linux systems, hardware detection and configuration are typically handled by the udev subsystem along with tools like systemd-udev or eudev. These tools provide dynamic device management, automatic hardware detection, and robust support for hot-plugging devices, making them suitable replacements for Kudzu.

9.
What is the difference between ext2 and ext3 file systems?

Hide Answer
ext2 vs ext3.webp

10.
Explain the /proc file system.

Hide Answer
The /proc file system in Linux is a virtual file system that exists only in memory and allows access to kernel data structures through regular files. The files and directories in /proc are not actual physical files, rather they represent kernel data structures that can be accessed using standard I/O system calls like read, write, and open.

The /proc file system provides a way for users and programs to access and gather information about the current state of the system. This information includes system hardware, memory, running processes, system configuration parameters, and other kernel statistics that can be useful to system administrators and developers.

For example, the /proc/cpuinfo file provides information about the CPU installed on the system, while /proc/mounts lists all mounted file systems. The /proc file system also allows users to interact with kernel modules, monitor system performance, and modify kernel parameters at runtime.

Since /proc files are generated dynamically by the kernel, they can be used to monitor the system in real time and provide instant access to system information, as opposed to static configuration files that require a system restart to take effect.

11.
How would you create an ext4 file system?

Hide Answer
To create an ext4 file system, you can use the mkfs.ext4 or mke4fs command to format a partition with the ext4 file system type. Here's an example command to format a new partition with the ext4 file system using the mkfs.ext4 command:

sudo mkfs.ext4 /dev/sdX1

Replace sdX1 with the appropriate device name and partition number. Please note that this will erase all the data on the partition.

12.
How to enable ACLs for the /home partition?

Hide Answer
Here are the steps to enable ACLs (Access Control Lists) for the /home partition in Linux:

Open the /etc/fstab file in a text editor:

sudo nano /etc/fstab

Find the line that corresponds to your /home partition. This should look similar to the following line:

UUID=<your_partition_UUID> /home ext4 defaults 0 2

Replace <your_partition_UUID> with the UUID of your /home partition, which you can find with the blkid command.

Add acl to the list of mount options for the /home partition. The resulting line should look like this:

UUID=<your_partition_UUID> /home ext4 defaults,acl 0 2

Save the changes and exit the text editor.

Remount the /home partition for the changes to take effect:

sudo mount -o remount /home

After completing these steps, you should have enabled ACLs for the /home partition in Linux and be able to set more specific permissions for files and directories within the /home directory.

13.
How can you create a software RAID (RAID 1) in Linux to mirror two disks for data redundancy?

Hide Answer
To create a software RAID 1 in Linux for data redundancy by mirroring two disks, follow these steps:

First, ensure that both disks you want to use for the RAID are connected and recognized by your system. You can verify their names using the lsblk command.

Partition both disks. You can use a utility like fdisk or parted to create a partition on each disk. Make both partitions of the same size and type. Typically, the partition type for RAID is "Linux raid autodetect" (type code fd).

Create the RAID array using the mdadm (Multiple Device Admin) command. Use the following command to create the RAID 1 array, replacing /dev/sdX1 and /dev/sdY1 with the appropriate partition names for your disks:

software raid.webp

After completing these steps, you should have successfully created a software RAID 1 in Linux with two disks for data redundancy. The RAID array will be automatically mounted on system startup and you can start using it for reliable and redundant storage.

14.
How can you configure a Linux firewall to allow or block specific incoming and outgoing traffic?

Hide Answer
To configure a Linux firewall and control incoming and outgoing traffic, you can use the built-in firewall management tools such as iptables or ufw. Here's a basic outline of the process:

Identify the specific incoming and outgoing traffic that you want to allow or block.
Use the appropriate commands to add rules to the firewall configuration.
Specify the type of traffic (TCP, UDP, etc.), the source and destination IP addresses, and the port numbers.
Verify the rules using the appropriate command.
Save the firewall configuration to make it persistent across reboots.
15.
How do you configure a Linux system to automatically mount an NFS share at startup?

Hide Answer
Open the terminal and login as root or a user with sudo privileges.
Create a directory where you want to mount the NFS share, e.g., sudo mkdir /mnt/nfs_share.
Edit the /etc/fstab file using a text editor, e.g., sudo nano /etc/fstab.
Add the following line at the end of the file:
< NFS-Server-IP >:< NFS-Share-Path > /mnt/nfs_share nfs defaults 0 0
Save the file and exit the editor.
Test the configuration by running sudo mount -a.
If there are no errors, the NFS share should be mounted.
Reboot your system, and the NFS share will be automatically mounted at startup.
16.
How can you find and kill all processes using a specific port in Linux?

Hide Answer
Open the terminal on your Linux system.
Use the lsof command followed by the port number to find the processes using that port. For example, lsof -i :80 will list all processes using port 80.
Note down the process IDs (PIDs) of the processes using the specific port.
Use the kill command followed by the PID(s) to terminate the processes. For example, kill PID will kill the process with the specified PID.
Confirm that the processes are terminated by re-running the lsof command.
17.
How do you analyze and optimize the boot process of a Linux system?

Hide Answer
Identify bottlenecks: Start by examining the boot logs to identify any processes or services that are taking longer to start. Look for any errors or warnings that may be impacting the boot time.
Disable unnecessary services: Disable any unnecessary services or daemons that are not required during the boot process. This can help reduce the overall boot time.
Optimize init scripts: Review and optimize the init scripts to ensure they are executing efficiently. This may involve simplifying or rewriting certain scripts.
Analyze hardware: Check the hardware configuration and ensure that the system has adequate resources to boot efficiently. Upgrading hardware, such as adding more RAM or replacing a slow hard drive, can significantly improve boot times.
Monitor boot time: Use tools like systemd-analyze or bootchart to measure and monitor the boot time. This will help identify any improvements made and the impact of any changes.
18.
How do you find the top 10 largest files and directories on your Linux system?

Hide Answer
To find the top 10 largest files and directories on your Linux system, you can use the 'du' (disk usage) command. First, navigate to the root directory of your system using the command line. Then, use the following command:

du -ah | sort -rh | head -n 10

This command will display the top 10 largest files and directories on your system, sorted in descending order with human-readable file sizes. The 'head -n 10' limits the output to only display the top 10 results. You can adjust the number to get more or fewer results. This command can help you identify large folders and files that are taking up valuable space on your system.

19.
How can you set up a Linux system as a router using IP forwarding and iptables?

Hide Answer
To set up a Linux system as a router using IP forwarding and iptables, there are several steps to follow. First, enable IP forwarding by editing the /etc/sysctl.conf file and uncommenting the line "net.ipv4.ip_forward=1". Then, configure the network interfaces with appropriate IP addresses. Next, use iptables to set up packet filtering and NAT rules to forward traffic between interfaces. The NAT rules allow private IP addresses to communicate with external networks by masquerading as the public IP address of the Linux system. Finally, save the iptables rules and configure them to be loaded upon boot. With these steps completed, the Linux system is now configured as a router.

20.
How do you check the integrity of a downloaded file using GPG signatures in Linux?

Hide Answer
gpg signatures.webp

21.
How do you set up SSH public key authentication between two Linux servers?

Hide Answer
On the client server, generate a key pair (public and private) using the ssh-keygen command.
Copy the public key to the remote server using the ssh-copy-id command.
On the remote server, modify the permissions of the ~/.ssh directory to 700 and the authorized_keys file to 600.
Disable password authentication on the remote server by modifying the sshd_config file and setting 'PasswordAuthentication' to 'no'.
Restart the sshd service on the remote server.
Now, whenever you connect to the remote server from the client server, SSH will use the public key to authenticate the connection, without the need for a password.
22.
How can you mount a USB drive automatically on system startup?

Hide Answer
To automatically mount a USB drive on system startup, you can modify the /etc/fstab file. First, find the UUID of the USB drive by using the following command: sudo blkid. Next, create a mount point for the USB drive using the following command: sudo mkdir /media/usb. Finally, edit the /etc/fstab file and add the following line: UUID=[UUID of USB] /media/usb [file system type] [options] 0 2. Replace the [UUID of USB], [file system type], and [options] with the respective values from the output of the sudo blkid command. Save and close the file. Now, the USB drive will be automatically mounted on system startup.

23.
How can you mount a USB drive automatically on system startup?

Hide Answer
mount usb drive.webp

24.
How can you recursively find all files containing a specific string in their content?

Hide Answer
To recursively find all files containing a specific string in their content, you can use a simple recursive function. Here's a basic approach:

Start at the root directory.
Iterate through each file and folder in the directory.
If it's a directory, recursively call the function with that directory as the new root.
If it's a file, read the file's content and check if the specific string is present.
If the string is found, store the file path.
Repeat steps 2-5 for all subdirectories and files.
Return the list of file paths containing the specific string.
25.
How do you set up a crontab to run a script every 15 minutes?

Hide Answer
To set up a crontab to run a script in Linux every 15 minutes, you can add the following line to your crontab file:

*/15 * * * * /path/to/your_script

This will run your_script every 15 minutes. The */15 means "every 15 minutes," while the five asterisks denote the time and date fields for minute, hour, day of the month, month, and day of the week, respectively . Make sure to replace /path/to/your_script with the actual path to your script.
Senario Based Quetions and answers:

### Question 1: In Ubuntu server, what is a public key and private key?

**Answer:**  
In Ubuntu server, a public key and a private key are cryptographic keys used in asymmetric encryption systems such as RSA. 

- **Public Key:** The public key is used for encryption and is freely distributable. It is typically shared with others to encrypt messages or data that can only be decrypted by the corresponding private key. In Ubuntu servers, public keys are often used for SSH authentication, allowing users to securely access remote servers without needing to transmit sensitive information like passwords.

- **Private Key:** The private key is kept secret and is used for decryption. It is essential for decrypting data or messages encrypted with the corresponding public key. In Ubuntu servers, the private key is securely stored on the client-side and is used to authenticate and establish secure connections to remote servers, such as SSH connections.

Public and private key pairs form the basis of secure communication and authentication in many applications, including SSH, SSL/TLS, and digital signatures.

### Question 2: Write a script of what you do daily?

**Answer:**  
As an example, here's a basic shell script that I might use for routine tasks:

```bash
#!/bin/bash

# Script for daily routine tasks

# Update package repositories and install updates
sudo apt update
sudo apt upgrade -y

# Clean up unused packages and cache
sudo apt autoremove -y
sudo apt autoclean

# Backup important files or directories
# For example, backup important configuration files
cp /etc/nginx/nginx.conf /home/user/backups/nginx.conf_backup

# Send a notification email confirming tasks completion
echo "Daily routine tasks completed." | mail -s "Daily Task Report" user@example.com
```

This script performs tasks such as updating packages, cleaning up the system, backing up important files, and sending a notification email upon completion. It can be customized to include specific tasks based on individual requirements.

### Question 3: `chmod 444 <filename.txt>` in root user? Change the above permissions to 777?

**Answer:**  
The command `chmod 444 <filename.txt>` sets read-only permissions for all users (owner, group, and others) on the specified file `<filename.txt>`. The permissions are represented as `-r--r--r--`, meaning the file is readable but not writable or executable by anyone.

To change the permissions to `777`, allowing all users to read, write, and execute the file, you can use the command:

```bash
sudo chmod 777 <filename.txt>
```

This command grants read, write, and execute permissions to the owner, group, and others on the specified file. However, it's important to use caution when granting such broad permissions, as it can pose security risks, especially for sensitive files.

### Question 4: `curl www.google.com` is not working, but `telnet www.google.com` is working. Why?

**Answer:**  
The command `curl www.google.com` attempts to retrieve the content of the specified URL using the HTTP/HTTPS protocol. If it's not working, it indicates a potential issue with the HTTP/HTTPS connection, such as network configuration, firewall settings, or connectivity problems.

On the other hand, `telnet www.google.com` establishes a TCP connection to the specified host and port (default is port 23 for telnet). If it's working, it suggests that there is connectivity between the client and the server on the specified port (in this case, port 23).

Possible reasons why `curl` is not working while `telnet` is:

1. **Firewall Restrictions**: The server may be blocking outgoing HTTP/HTTPS traffic, but allowing outgoing TCP traffic on port 23 (used by telnet).

2. **Proxy Configuration**: If a proxy server is required for HTTP/HTTPS connections, but not for plain TCP connections, `curl` may fail to connect due to incorrect proxy settings.

3. **DNS Resolution**: There could be DNS resolution issues preventing `curl` from resolving the hostname `www.google.com` to an IP address.

4. **Protocol Issues**: If `curl` is configured to use HTTPS, but the server only supports HTTP, or vice versa, it may fail to establish a connection.

Troubleshooting involves checking network configurations, firewall rules, DNS settings, and proxy configurations to identify and resolve the underlying issue.

### Question 5: What is SSL, and how does it work internally?

**Answer:**  
SSL (Secure Sockets Layer) is a cryptographic protocol used to secure communication over a network, typically between a client (e.g., web browser) and a server (e.g., web server). It ensures that data transmitted between the client and server is encrypted and protected from eavesdropping, tampering, or forgery.

Internally, SSL works through a process called the SSL handshake, which establishes a secure connection between the client and server. The SSL handshake involves the following steps:

1. **Client Hello**: The client sends a hello message to the server, indicating the SSL version and supported cryptographic algorithms.

2. **Server Hello**: The server responds with a hello message, selecting the SSL version and cryptographic algorithms to use for the connection.

3. **Certificate Exchange**: The server sends its digital certificate to the client, containing its public key and other identifying information. The client verifies the authenticity of the certificate and extracts the server's public key.

4. **Key Exchange**: The client generates a random session key, encrypts it with the server's public key from the certificate, and sends it to the server. Both the client and server now have a shared session key for symmetric encryption.

5. **Session Encryption**: Once the session key is established, both the client and server use it to encrypt and decrypt data transmitted during the SSL session. This provides confidentiality and integrity for the exchanged data.

6. **Secure Communication**: With the session key in place, the client and server can securely exchange data over the encrypted SSL connection. The data is encrypted before transmission and decrypted upon receipt, ensuring secure communication.

SSL utilizes cryptographic techniques such as asymmetric encryption (for key exchange and authentication) and symmetric encryption (for data encryption) to achieve secure communication between parties. It forms the basis of modern security protocols such as TLS (Transport Layer Security), which has largely superseded SSL but retains its name for historical reasons.

### 6: What is SSL? And how it works internally?

**Answer:** 
**SSL (Secure Sockets Layer)** is a cryptographic protocol designed to secure communication over a network, typically between a client (such as a web browser) and a server (such as a web server). SSL ensures that data transmitted between the client and server is encrypted and protected from eavesdropping, tampering, or forgery.

Internally, SSL works through a process called the SSL handshake, which establishes a secure connection between the client and server:

1. **Client Hello:** The client initiates the SSL handshake by sending a "hello" message to the server, specifying the SSL version and supported cryptographic algorithms.

2. **Server Hello:** The server responds with its own "hello" message, selecting the SSL version and cryptographic algorithms to use for the connection.

3. **Certificate Exchange:** The server sends its digital certificate to the client, containing its public key and other identifying information. The client verifies the authenticity of the certificate and extracts the server's public key.

4. **Key Exchange:** The client generates a random session key, encrypts it with the server's public key from the certificate, and sends it to the server. Both the client and server now have a shared session key for symmetric encryption.

5. **Session Encryption:** With the session key established, both the client and server use it to encrypt and decrypt data transmitted during the SSL session. This provides confidentiality and integrity for the exchanged data.

6. **Secure Communication:** Once the SSL handshake is complete, the client and server can securely exchange data over the encrypted SSL connection. The data is encrypted before transmission and decrypted upon receipt, ensuring secure communication.

SSL utilizes cryptographic techniques such as asymmetric encryption (for key exchange and authentication) and symmetric encryption (for data encryption) to achieve secure communication between parties. It forms the basis of modern security protocols such as TLS (Transport Layer Security), which has largely superseded SSL but retains its name for historical reasons.

### 7: What is Lambda and how it works?

**Answer:** 
**AWS Lambda** is a serverless computing service provided by Amazon Web Services (AWS) that allows you to run code without provisioning or managing servers. Lambda enables you to execute code in response to events such as changes in data, system state, or user actions. Here's how Lambda works:

1. **Event Sources:** Lambda functions are triggered by various event sources, such as changes to Amazon S3 buckets, updates to DynamoDB tables, HTTP requests via Amazon API Gateway, or scheduled events from Amazon CloudWatch Events. These event sources invoke Lambda functions asynchronously, triggering the execution of the associated code.

2. **Execution Environment:** When an event triggers a Lambda function, AWS automatically provisions and manages the execution environment for the function. This includes allocating compute resources (CPU, memory), initializing the runtime environment (e.g., Node.js, Python, Java), and managing dependencies.

3. **Code Execution:** The Lambda function's code is executed within the provided execution environment. The function processes the incoming event, performs the required computations or operations, and generates output as needed. Lambda functions are stateless, meaning they do not retain any state between invocations.

4. **Scalability and Concurrency:** Lambda automatically scales to handle incoming requests, invoking multiple instances of the function in parallel as needed to accommodate fluctuations in workload. Each instance of the function executes independently, allowing for concurrent execution of multiple requests.

5. **Billing Model:** Lambda follows a pay-as-you-go pricing model, where you are billed based on the number of invocations and the duration of code execution. You are charged only for the compute resources consumed during the execution of your function, with no charges for idle time or server maintenance.

6. **Integration with AWS Services:** Lambda integrates seamlessly with various AWS services, allowing you to build serverless architectures and event-driven workflows. You can use Lambda to process data from Amazon S3, trigger notifications via Amazon SNS, process streaming data from Amazon Kinesis, or execute business logic in response to API requests.

Lambda simplifies the development and deployment of applications by abstracting away infrastructure management, enabling developers to focus on writing code and building innovative solutions without worrying about server provisioning, scaling, or maintenance.

### Answer 8: What are the most frequently asked questions on networking, ports, and protocols?


**Answer:** 
**Networking, ports, and protocols** are fundamental aspects of IT infrastructure and often form the basis of technical interviews. Some frequently asked questions in this domain include:

1. **Difference between TCP and UDP:** TCP (Transmission Control Protocol) is a connection-oriented protocol that guarantees delivery of data packets in sequence, while UDP (User Datagram Protocol) is connectionless and does not guarantee delivery or sequencing of packets.

2. **Port Numbers:** Port numbers are used to identify specific services or processes running on a computer. Common examples include port 80 for HTTP, port 443 for HTTPS, port 22 for SSH, and port 25 for SMTP.

3. **DNS (Domain Name System):** DNS is a hierarchical decentralized naming system for computers, services, or other resources connected to the Internet. It translates domain names into IP addresses, allowing users to access websites using human-readable names.

4. **OSI Model:** The OSI (Open Systems Interconnection) model is a conceptual framework that standardizes the functions of a telecommunication or computing system into seven abstraction layers, from physical transmission to application-specific functionality.

5. **IPv4 vs. IPv6:** IPv4 (Internet Protocol version 4) is the fourth revision of the Internet Protocol and uses 32-bit addresses, while IPv6 (Internet Protocol version 6) is the most recent version and uses 128-bit addresses to accommodate the growing number of devices connected to the Internet.

6. **NAT (Network Address Translation):** NAT is a technique used in networking to map private IP addresses to public IP addresses and vice versa, allowing multiple devices on a local network to share a single public IP address.

7. **Firewalls:** Firewalls are security devices or software that monitor and control incoming and outgoing network traffic based on predetermined security rules. They help protect networks from unauthorized access and cyber threats.

8. **Routing:** Routing is the process of selecting the best path for network traffic to reach its destination. Routers use routing tables and algorithms to determine the optimal route based on factors such as network topology, traffic load, and link availability.

9. **Subnet Masks:** Subnet masks are used to divide IP networks into smaller subnetworks, allowing for efficient use of IP addresses and logical segmentation of network traffic.

10. **DHCP (Dynamic Host Configuration Protocol):** DHCP is a network protocol that automatically assigns IP addresses and other network configuration parameters to devices on a network, simplifying network administration and configuration.

Understanding these concepts is essential for networking professionals and IT professionals working with network infrastructure, security, and systems administration.
