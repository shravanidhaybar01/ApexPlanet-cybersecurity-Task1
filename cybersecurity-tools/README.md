Cybersecurity Tools – Apex Planet Internship

1. Introduction

Cybersecurity tools help security professionals monitor networks, identify vulnerabilities, inspect web traffic, and troubleshoot communication.

During this internship task, I became familiar with Wireshark, Nmap, Burp Suite, and Netcat.

2. Wireshark

What is Wireshark?

Wireshark is an open-source network protocol analyzer used to capture and inspect network packets.

Main Features

- Captures network traffic.
- Displays packet details.
- Supports protocol filtering.
- Helps troubleshoot network problems.
- Helps analyze suspicious network activity.

Important Display Filters

Filter| Purpose
"icmp"| Displays ICMP packets.
"dns"| Displays DNS packets.
"http"| Displays HTTP packets.
"tcp"| Displays TCP packets.
"udp"| Displays UDP packets.
"ip.addr == 192.168.1.10"| Filters packets involving a particular IP address.

Practical Activity

1. Open Wireshark in Kali Linux.
2. Select the appropriate network interface.
3. Start packet capture.
4. Generate ping traffic to your Ubuntu lab machine.
5. Apply the "icmp" display filter.
6. Observe Echo Request and Echo Reply packets.

Command:

ping -c 4 UBUNTU_IP

3. Nmap

What is Nmap?

Nmap (Network Mapper) is an open-source network scanning tool used to discover hosts and identify open ports and services.

Important Commands

Command| Purpose
"nmap --version"| Checks Nmap version.
"nmap TARGET_IP"| Performs a basic scan.
"nmap -sV TARGET_IP"| Detects service versions.
"nmap -O TARGET_IP"| Attempts operating system detection.
"nmap -p 80,443 TARGET_IP"| Scans selected ports.
"nmap -oN result.txt TARGET_IP"| Saves results in normal text format.

Practical Activity

The following command was used to examine the Ubuntu virtual machine in my own lab:

nmap -sV UBUNTU_IP

The scan reports information about detected ports and services.

Only scan systems for which you have permission.

4. Burp Suite

What is Burp Suite?

Burp Suite is a web application security testing platform used to inspect and test HTTP and HTTPS communication.

Important Components

- Proxy: Intercepts and displays web traffic.
- HTTP History: Displays captured HTTP requests and responses.
- Repeater: Allows manual modification and resending of requests.
- Intruder: Automates customized request testing.
- Decoder: Encodes and decodes data.
- Comparer: Compares two data items.

Practical Activity

1. Open Burp Suite in Kali Linux.
2. Start a temporary project.
3. Open the built-in Burp browser.
4. Visit the DVWA application hosted on your Ubuntu VM.
5. Navigate through DVWA.
6. Open Proxy → HTTP history.
7. Inspect a captured HTTP request.

This activity helped me understand how web browser requests and server responses can be inspected.

5. Netcat

What is Netcat?

Netcat is a networking utility used to establish TCP or UDP connections and exchange data between systems.

It is commonly called the Swiss Army knife of networking.

Important Commands

Command| Purpose
"nc -h"| Displays help information.
"nc -lvnp 4444"| Starts a listener on port 4444.
"nc UBUNTU_IP 4444"| Connects to the Ubuntu listener.
"nc -zv UBUNTU_IP 80"| Checks connectivity to port 80.

Practical Activity – Kali and Ubuntu Communication

Ubuntu Server (Receiver):

nc -lvnp 4444

Kali Linux (Sender):

nc UBUNTU_IP 4444

After connecting, a simple text message can be exchanged between the two systems.

Example:

Hello from Kali Linux
Hello from Ubuntu Server

This demonstrates basic communication between virtual machines.

6. Comparison of Tools

Tool| Main Purpose
Wireshark| Network packet analysis.
Nmap| Network discovery and port scanning.
Burp Suite| Web application security testing.
Netcat| Network connections and communication.

7. Learning Outcomes

Through these tools, I learned:

1. How to capture and inspect network packets.
2. How to identify open ports and detected services.
3. How to inspect HTTP requests.
4. How to establish communication between virtual machines.
5. How cybersecurity tools support network and application security testing.

8. Conclusion

Wireshark, Nmap, Burp Suite, and Netcat are useful tools for learning network analysis and cybersecurity testing. Practising them in a controlled virtual environment helped me understand their basic functions and practical applications.
