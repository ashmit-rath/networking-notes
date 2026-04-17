# Tcpdump: The Basics

## Introduction

tcpdump is a command-line packet analyzer used to capture and inspect network traffic in real-time.

- Works at packet level
- Lightweight (no GUI)
- Common in debugging, monitoring, and CTFs

---

## Basic Syntax

tcpdump [options] [filter]

Example:
tcpdump -i eth0

---

## Core Options (with File Usage)

- -i <interface> → Interface select (eth0, wlan0)
- -c <count> → Limit packets
- -w <filename>.pcap → SAVE packets to file
- -r <filename>.pcap → READ packets from file
- -n → No DNS resolution
- -nn → No DNS + no port resolution
- -v / -vv / -vvv → Verbosity levels

---

## Basic Packet Capture

### Capture live traffic (no file)
tcpdump -i eth0

### Capture limited packets
tcpdump -i eth0 -c 50

### Capture on all interfaces
tcpdump -i any

---

## Saving Packets (IMPORTANT)

👉 Filename ALWAYS comes after `-w`

### Basic save
tcpdump -i eth0 -w capture.pcap

### Save with packet limit
tcpdump -i eth0 -c 100 -w limited_capture.pcap

### Save filtered traffic
tcpdump -i eth0 port 80 -w http_traffic.pcap

---

## Reading Packets from File

👉 Filename ALWAYS comes after `-r`

### Read file
tcpdump -r capture.pcap

### Read with filters
tcpdump -r capture.pcap port 80

---

## Filtering Expressions

### By Host
tcpdump host 192.168.1.10

### By Source/Destination
tcpdump src host 192.168.1.10  
tcpdump dst host 192.168.1.10  

### By Port
tcpdump port 80  
tcpdump src port 22  
tcpdump dst port 443  

### By Protocol
tcpdump tcp  
tcpdump udp  
tcpdump icmp  

---

## Combined Filters

### AND
tcpdump host 192.168.1.10 and port 80

### OR
tcpdump port 80 or port 443

### NOT
tcpdump not tcp

---

## Practical Examples (WITH FILE POSITION CLEAR)

### SSH traffic capture + save
tcpdump -i any tcp port 22 -w ssh_capture.pcap

### DNS traffic capture + save
tcpdump -i any port 53 -w dns_capture.pcap

### HTTPS traffic (specific host)
tcpdump -i eth0 host example.com and tcp port 443 -w example_https.pcap

### NTP traffic capture
tcpdump -i wlan0 udp port 123 -w ntp_capture.pcap

---

## Displaying Packet Data

### ASCII output
tcpdump -A

### Hex + ASCII output
tcpdump -X

---

## Key Understanding

- `-w <filename>` → used when you want to SAVE packets  
- `-r <filename>` → used when you want to READ packets  
- File is usually `.pcap` format  
- You can later open `.pcap` files in Wireshark  
- Filters apply BEFORE saving (important for clean data)

---
