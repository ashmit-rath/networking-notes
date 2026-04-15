🌐 Networking Concepts

OSI Model (7 Layers)

The OSI model is a conceptual framework that explains how data travels across a network.

Layers (Top → Bottom)

7. Application Layer

- Provides services directly to user applications
- Examples: HTTP, FTP, SMTP

6. Presentation Layer

- Handles data formatting
- Responsible for encoding, encryption, compression

5. Session Layer

- Manages sessions between systems
- Establishes, maintains, and terminates connections

4. Transport Layer

- Ensures end-to-end communication
- Splits data into segments
- Protocols: TCP, UDP

3. Network Layer

- Handles logical addressing (IP)
- Responsible for routing

2. Data Link Layer

- Ensures reliable data transfer between devices
- Uses MAC addresses
- Data is framed here

1. Physical Layer

- Transmits raw bits over hardware
- Includes cables, signals, electrical transmission

---

TCP/IP Model

A practical model used in real-world networking.

Layers:

- Application → HTTP, HTTPS, FTP, DNS
- Transport → TCP, UDP
- Internet → IP, ICMP
- Network Access → Ethernet, WiFi

---

IP Addressing

An IP address uniquely identifies a device on a network.

Private IP Ranges

- 10.0.0.0 – 10.255.255.255
- 172.16.0.0 – 172.31.255.255
- 192.168.0.0 – 192.168.255.255

Used in internal networks (LAN).

---

TCP vs UDP

TCP (Transmission Control Protocol)

- Reliable and connection-oriented
- Ensures data delivery
- Uses 3-way handshake:
  - SYN → request
  - SYN-ACK → response
  - ACK → confirmation

UDP (User Datagram Protocol)

- Fast and connectionless
- No guarantee of delivery
- Used where speed matters

---

Port Numbers

- Range: 1 – 65535
- Port 0 is reserved

Common Ports:

- 80 → HTTP
- 443 → HTTPS
- 22 → SSH
- 21 → FTP

---

Encapsulation

Data is wrapped with headers at each layer:

- Application → Data
- Transport → Segment
- Network → Packet
- Data Link → Frame

This process is called encapsulation.

---

Telnet

A protocol used for remote communication.

- Not secure (data sent in plain text)

Syntax:

telnet <IP> <Port>

Example:

telnet 192.168.1.1 80

---

Notes

- TCP is reliable but slower
- UDP is faster but unreliable
- Telnet is outdated → replaced by SSH
