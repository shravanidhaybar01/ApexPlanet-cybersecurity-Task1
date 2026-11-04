Linux Commands Cheat Sheet

1. Introduction to Linux

Linux is an open-source operating system widely used in servers, cybersecurity, networking, and system administration.

Kali Linux is a Debian-based Linux distribution commonly used for cybersecurity testing and digital forensics.

2. Basic Navigation Commands

Command| Description| Example
"pwd"| Displays the current working directory.| "pwd"
"ls"| Lists files and directories.| "ls"
"ls -l"| Displays files with detailed information.| "ls -l"
"ls -la"| Displays all files, including hidden files.| "ls -la"
"cd"| Changes the current directory.| "cd Downloads"
"cd .."| Moves to the parent directory.| "cd .."
"cd ~"| Moves to the home directory.| "cd ~"
"clear"| Clears the terminal screen.| "clear"

3. File and Directory Management

Command| Description
"mkdir foldername"| Creates a new directory.
"rmdir foldername"| Removes an empty directory.
"touch file.txt"| Creates an empty file.
"cat file.txt"| Displays file contents.
"nano file.txt"| Opens a file in the Nano text editor.
"cp file1 file2"| Copies a file.
"mv file1 file2"| Moves or renames a file.
"rm file.txt"| Deletes a file.
"find /path -name file.txt"| Searches for a file by name.

Example:

mkdir CybersecurityLab
cd CybersecurityLab
touch notes.txt
ls -la

4. File Permissions and Ownership

Linux permissions control who can read, write, and execute files.

Permission Types

Permission| Symbol| Value
Read| r| 4
Write| w| 2
Execute| x| 1

Important Commands

Command| Description
"ls -l"| Displays file permissions.
"chmod 755 file.txt"| Changes file permissions.
"chmod 644 file.txt"| Gives owner read/write and others read permission.
"chmod +x script.sh"| Adds execute permission.
"chown user:user file.txt"| Changes file owner and group.

Example:

touch test.txt
chmod 644 test.txt
ls -l test.txt

5. Package Management Commands

APT is a package management tool used in Debian-based distributions such as Kali Linux and Ubuntu.

Command| Description
"sudo apt update"| Updates package information.
"sudo apt upgrade"| Upgrades installed packages.
"sudo apt install nmap"| Installs Nmap.
"sudo apt remove nmap"| Removes Nmap.
"sudo apt autoremove"| Removes unnecessary packages.
"dpkg -l"| Lists installed packages.
"dpkg -l nmap"| Checks the Nmap package installation.

6. Networking Commands

Command| Description
"ip a"| Displays network interfaces and IP addresses.
"ip route"| Displays routing information.
"ping -c 4 8.8.8.8"| Tests network connectivity.
"ifconfig"| Displays network interface information.
"netstat -tuln"| Displays listening TCP and UDP ports.
"traceroute google.com"| Displays the route to a destination.
"ss -tuln"| Displays listening network sockets.
"hostname -I"| Displays assigned IP addresses.

Note: Install "net-tools" for "ifconfig" and "netstat", and install "traceroute" if those commands are unavailable.

sudo apt install net-tools traceroute -y

7. Netcat Commands

Netcat is a networking utility used to establish TCP or UDP connections and exchange data.

Command| Description
"nc -h"| Displays Netcat help.
"nc -lvnp 4444"| Listens on port 4444.
"nc 192.168.56.102 4444"| Connects to a listener at the specified IP and port.
"nc -zv 192.168.56.102 80"| Checks connectivity to port 80.

Example: Communication between Kali and Ubuntu

Ubuntu (receiver):

nc -lvnp 4444

Kali (sender):

nc UBUNTU_IP 4444

Replace "UBUNTU_IP" with your actual Ubuntu lab IP address.

8. User and System Information Commands

Command| Description
"whoami"| Displays the current username.
"id"| Displays user and group IDs.
"uname -a"| Displays kernel and system information.
"hostname"| Displays the system hostname.
"date"| Displays the current date and time.
"history"| Displays previously executed commands.
"free -h"| Displays memory usage.
"df -h"| Displays disk space usage.
"top"| Displays running processes and resource usage.
"ps aux"| Displays running processes.

9. Process Management Commands

Command| Description
"ps"| Displays processes.
"ps aux"| Lists running processes.
"top"| Monitors system processes.
"kill PID"| Sends a termination signal to a process.
"kill -9 PID"| Forcefully terminates a process.

Use process termination commands carefully and only on processes you are authorized to manage.

10. Help and Documentation Commands

Command| Description
"man ls"| Opens the manual for the ls command.
"ls --help"| Displays command help.
"history"| Shows command history.
"whatis ls"| Gives a short description of a command.

11. Practical Commands Executed in Kali Linux

The following commands were practised during the internship lab setup:

pwd
ls -la
mkdir CybersecurityLab
cd CybersecurityLab
touch test.txt
chmod 644 test.txt
ls -l
whoami
sudo apt update
sudo apt install net-tools -y
dpkg -l
ip a
ping -c 4 127.0.0.1
netstat -tuln
ifconfig

12. Important Linux Security Practices

1. Avoid running unknown scripts with root privileges.
2. Use "sudo" only when administrative access is required.
3. Apply appropriate file permissions.
4. Keep packages and system software updated.
5. Use strong passwords.
6. Monitor running processes and network connections.
7. Avoid deleting system files without understanding their purpose.

13. Conclusion

Linux commands are essential for cybersecurity professionals because they help manage files, configure permissions, install software, monitor processes, and troubleshoot networks.

Practising these commands in Kali Linux helped develop basic Linux administration and command-line skills.
