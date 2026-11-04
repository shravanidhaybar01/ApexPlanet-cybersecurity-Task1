Networking Fundamentals – Apex Planet Internship

1. Introduction to Computer Networking

Computer networking is the process of connecting two or more devices to share information, resources, and services.

Networking is important in cybersecurity because it helps security professionals understand how devices communicate and how network attacks can occur.

2. OSI Model

The OSI (Open Systems Interconnection) model explains network communication through seven layers.

Layer| Name| Function
7| Application| Provides network services to applications.
6| Presentation| Handles data formatting, encryption, and compression.
5| Session| Establishes and manages communication sessions.
4| Transport| Provides end-to-end data delivery using TCP or UDP.
3| Network| Handles logical addressing and routing.
2| Data Link| Handles frames and MAC addresses.
1| Physical| Transmits raw bits through physical media.

3. TCP/IP Model

The TCP/IP model is used for communication over the internet.

Layer| Function
Application| Provides services such as HTTP, DNS, and FTP.
Transport| Handles communication using TCP and UDP.
Internet| Handles IP addressing and routing.
Network Access| Handles communication over the local network.

TCP vs UDP

TCP| UDP
Connection-oriented| Connectionless
Reliable data delivery| Does not guarantee delivery
Uses acknowledgements| No built-in acknowledgements
Used by HTTPS and SSH| Used by DNS queries and streaming applications

4. IP Addressing

An IP address is a logical address assigned to a device on a network.

Types of IP Addresses

- IPv4: Uses a 32-bit address, for example, 192.168.1.10.
- IPv6: Uses a 128-bit address.
- Public IP: Used for communication over the internet.
- Private IP: Used within private networks.

Private IPv4 Address Ranges

Range| Address Block
Class A private range| 10.0.0.0/8
Class B private range| 172.16.0.0/12
Class C private range| 192.168.0.0/16

5. Subnetting

Subnetting is the process of dividing a larger network into smaller networks.

It improves network organization, address management, and network segmentation.

Example:

192.168.1.0/24

- Network address: 192.168.1.0
- Subnet mask: 255.255.255.0
- Total IPv4 addresses: 256
- Usable host addresses: 254

6. DNS (Domain Name System)

DNS converts human-readable domain names into IP addresses.

Example:

When a user visits example.com, DNS helps find the IP address associated with that domain.

Common DNS record types:

Record| Purpose
A| Maps a domain to an IPv4 address.
AAAA| Maps a domain to an IPv6 address.
MX| Specifies mail servers.
CNAME| Creates a domain alias.
NS| Identifies authoritative name servers.
TXT| Stores text information, often used for verification.

7. HTTP and HTTPS

HTTP (Hypertext Transfer Protocol) is used for communication between web browsers and web servers.

HTTPS is the secure version of HTTP. It uses TLS to protect communication.

HTTP| HTTPS
Does not provide TLS encryption| Uses TLS encryption
Commonly uses port 80| Commonly uses port 443
Data is not protected by TLS| Data is protected during transmission by TLS

8. NAT (Network Address Translation)

NAT translates IP addresses between networks.

It is commonly used by routers to allow multiple private network devices to share a public IP address.

Types:

- Static NAT
- Dynamic NAT
- PAT (Port Address Translation)

9. Important Networking Commands

Command| Purpose
"ip a"| Displays IP addresses and interfaces.
"ip route"| Displays routing information.
"ping -c 4 8.8.8.8"| Tests network connectivity.
"traceroute example.com"| Displays the route to a destination.
"netstat -tuln"| Displays listening ports.
"ss -tuln"| Displays listening sockets.
"nslookup example.com"| Queries DNS information.
"hostname -I"| Displays assigned IP addresses.

10. Practical Networking Activities

During the lab setup, networking commands were practised in Kali Linux.

Activities included:

1. Checking IP addresses using "ip a".
2. Testing connectivity using "ping".
3. Viewing listening ports using "netstat".
4. Examining network routes using "traceroute".
5. Testing communication between Kali Linux and Ubuntu Server.

11. Conclusion

Networking fundamentals are essential for understanding communication between systems, IP addressing, routing, and network security. Knowledge of these concepts helps cybersecurity professionals identify and troubleshoot network-related security issues.
