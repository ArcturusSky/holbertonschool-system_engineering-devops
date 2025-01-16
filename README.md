# Network Protocols Explained Simply

- [Network Protocols Explained Simply](#network-protocols-explained-simply)
  - [1. Introduction to Network Protocols](#1-introduction-to-network-protocols)
  - [2. OSI Model](#2-osi-model)
  - [3. TCP/IP Model](#3-tcpip-model)
  - [4. Types of Network Protocols](#4-types-of-network-protocols)
  - [5. Implementation and Vulnerabilities](#5-implementation-and-vulnerabilities)
  - [6. Key Protocols for Web and Mobile Development](#6-key-protocols-for-web-and-mobile-development)
    - [6.1 Web Protocols](#61-web-protocols)
    - [6.2 Mobile Protocols](#62-mobile-protocols)
  - [7. Security Considerations](#7-security-considerations)
  - [8. Importance for Developers](#8-importance-for-developers)
- [Understanding IP Addresses](#understanding-ip-addresses)
  - [1. Definition of an IP Address](#1-definition-of-an-ip-address)
  - [2. Types of IP Addresses](#2-types-of-ip-addresses)
  - [3. IP Classes and Reservations (IPv4)](#3-ip-classes-and-reservations-ipv4)
  - [4. Subnets](#4-subnets)
  - [5. Finding Your IP Address](#5-finding-your-ip-address)
- [TCP/IP: Transmission Control Protocol/Internet Protocol](#tcpip-transmission-control-protocolinternet-protocol)
  - [1. Key Components](#1-key-components)
    - [TCP (Transmission Control Protocol)](#tcp-transmission-control-protocol)
    - [IP (Internet Protocol)](#ip-internet-protocol)
  - [2. How TCP/IP Works](#2-how-tcpip-works)
    - [Communication Process](#communication-process)
  - [3. Importance of TCP/IP](#3-importance-of-tcpip)
  - [4. Use Cases](#4-use-cases)
  - [5. TCP vs UDP](#5-tcp-vs-udp)
- [Port Numbers in Networking](#port-numbers-in-networking)
  - [Definition](#definition)
  - [Function](#function)
  - [Key Points](#key-points)
  - [When Port Numbers Matter](#when-port-numbers-matter)
  - [Open vs Closed Ports](#open-vs-closed-ports)
  - [Port Scanning](#port-scanning)
  - [Viewing Active Connections](#viewing-active-connections)


## 1. Introduction to Network Protocols

A network protocol is a set of rules that define how data is formatted, sent, and received between different devices (computers, servers, routers, etc.), regardless of their infrastructure or design.

Key points:
- Enable efficient device communication
- Essential for modern networks like the Internet

## 2. OSI Model

The OSI (Open Systems Interconnection) model organizes protocols into 7 layers:

1. Physical: Transmits bits via cables, fibers, or signals
2. Data Link: Assembles data into blocks and corrects errors
3. Network: Routes and divides data into small packets
4. Transport: Ensures reliable data transmission between devices
5. Session: Manages connections (authentication and synchronization)
6. Presentation: Translates and secures data (encryption, formatting)
7. Application: User interface (email, web browsing, file transfers)

Each layer uses headers or footers to identify and process data.

## 3. TCP/IP Model

The TCP/IP model, the foundation of the Internet, simplifies the OSI model into 4 layers:

1. Application: Protocols like HTTP, SMTP, FTP
2. Transport: Ensures transmission reliability (TCP, UDP)
3. Internet: Addressing and routing (IP, ARP)
4. Network Access: Communicates with hardware (Ethernet, MAC)

## 4. Types of Network Protocols

1. Communication: e.g., HTTP, TCP (for data exchange)
2. Management: e.g., SNMP (for network monitoring and administration)
3. Security: e.g., HTTPS, SSL (for protecting data in transit)

## 5. Implementation and Vulnerabilities

- Protocols are integrated into hardware or software systems
- Vulnerabilities: Some protocols lack protection, facilitating attacks like route hijacking or DDoS attacks (e.g., SYN flood attack)

## 6. Key Protocols for Web and Mobile Development

### 6.1 Web Protocols
- HTTP/HTTPS: Basic protocol for loading web pages. HTTPS adds security via SSL/TLS
- DNS: Translates domain names (e.g., example.com) to IP addresses
- FTP: Allows file transfer to a server

### 6.2 Mobile Protocols
- REST or GraphQL APIs: Often rely on HTTP(S) to exchange data between a mobile app and a server

## 7. Security Considerations

- Common issues: DDoS attacks or eavesdropping
- Best practice: Use HTTPS to secure communications for web and mobile applications

## 8. Importance for Developers

- Understanding protocols like HTTP/HTTPS helps in interacting with servers and diagnosing network issues
- Knowledge of TCP/IP and layers allows for better optimization and security of applications (latency, error handling)
- Data security in transit is critical, especially in mobile applications where users expect maximum protection

Remember: Familiarize yourself with HTTP, HTTPS, TCP, UDP, and DNS, as they form the basis of all modern web and mobile development. Add to this an understanding of network security to ensure a better user experience.

# Understanding IP Addresses

## 1. Definition of an IP Address

An IP (Internet Protocol) address is a unique identifier allowing computers to communicate on a network, similar to a postal address for data.

- IPv4: 32 bits, decimal format (e.g., 192.168.1.1)
- IPv6: 128 bits, hexadecimal format (e.g., 2001:db8::1)
  - Created to address the shortage of IPv4 addresses

## 2. Types of IP Addresses

- Static: Fixed, less common, often used locally
- Dynamic: Temporarily assigned via DHCP, most widespread

## 3. IP Classes and Reservations (IPv4)

Addresses are divided into ranges reserved for specific uses:

- 0.0.0.0: Default network
- 127.0.0.1: Loopback address (refers to the computer itself)
- 169.254.x.x: Automatically assigned in case of DHCP failure
- Classes A, B, C: Used for private and public networks
  - Class A: 10.0.0.0 – 10.255.255.255
  - Class B: 172.16.0.0 – 172.31.255.255
  - Class C: 192.168.0.0 – 192.168.255.255

## 4. Subnets

A subnet divides a network into segments for better management:

Example:
- IP Address: 192.168.1.102
- Subnet Mask: 255.255.255.0
- Subnet Range: 192.168.1.0 – 192.168.1.255

## 5. Finding Your IP Address

- Windows: Open "cmd" → Type ipconfig
- Mac: System Preferences → Network
- Mobile: Settings → WiFi → Network Information

Key takeaway: IP addresses enable communication on networks. Understanding their functioning (IPv4, IPv6, DHCP, subnets) is essential for managing networks or developing connected applications.

# TCP/IP: Transmission Control Protocol/Internet Protocol

TCP/IP is a set of standard protocols that govern how devices communicate on networks like the internet. It forms the foundation of nearly all modern network communications.

## 1. Key Components

### TCP (Transmission Control Protocol)
- Manages data reliability and integrity
- Segments data, transmits it, and reassembles it at the destination
- Ensures retransmission of lost or damaged data
- Example: Sending a file or loading a web page

### IP (Internet Protocol)
- Handles addressing and routing of data
- Ensures data reaches the correct destination using unique IP addresses
- Two versions: IPv4 and IPv6

## 2. How TCP/IP Works

1. Data (text, video, audio) is divided into packets
2. Each packet contains:
   - Source address
   - Destination address
   - Part of the data

### Communication Process
1. Application layer: User interacts with an application (e.g., web browser)
2. Transport layer (TCP): Data is segmented with sequence numbers
3. Internet layer (IP): Packets are sent with IP addresses
4. Network layer: Packets traverse the physical network to the destination
5. Reassembly: TCP reconstructs data for the application

## 3. Importance of TCP/IP

- Interoperability: All TCP/IP devices can communicate regardless of manufacturer
- Reliability: TCP ensures error-free transmission
- Flexibility: Compatible with various network types (WiFi, Ethernet, fiber, etc.)
- Scalability: Adapts to millions of connected devices on the internet

## 4. Use Cases

- Web (HTTP/HTTPS): Loading web pages
- Emails (SMTP, IMAP, POP3): Transmitting electronic messages
- File transfer (FTP, SFTP): Downloading or uploading files
- Streaming (YouTube, Netflix): Real-time video/audio transmission

## 5. TCP vs UDP

- TCP: Reliable but slower (used for web, emails)
- UDP (User Datagram Protocol): Less reliable but faster (used for streaming, online gaming)

In summary, TCP/IP is the universal language of networks, enabling efficient communication between different devices via the internet or other networks.

# Port Numbers in Networking

## Definition
Port numbers are part of the addressing information used to identify senders and receivers of messages in computer networking. They are associated with TCP/IP network connections and can be considered an add-on to the IP address.

## Function
- Allow different applications on the same computer to share network resources simultaneously
- Work like telephone extensions, with the IP address as the main number and ports as extensions

## Key Points
1. Software-based, not related to physical ports
2. Used by both TCP and UDP in TCP/IP networking
3. Range from 0 to 65535
4. Lower ranges dedicated to common internet protocols (e.g., port 25 for SMTP, port 21 for FTP)

## When Port Numbers Matter
1. Network administration: Setting up port forwarding through firewalls
2. Network programming: Specifying port numbers in code
3. URL specification: Sometimes required in URLs (e.g., http://localhost:8080/)

## Open vs Closed Ports
- Open ports: Have an associated application listening for new connection requests
- Closed ports: Do not have an associated listening application

## Port Scanning
- Used by professionals to measure network exposure
- Used by hackers to probe for exploitable open ports

## Viewing Active Connections
Use the `netstat` command in Windows to see information about active TCP and UDP connections.
