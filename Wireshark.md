# Wireshark: The Basics

## Introduction

Wireshark is a network protocol analyzer used to capture and inspect network traffic in real time.

- Used for packet analysis, troubleshooting, and security analysis  
- Works on packet-level inspection  
- Supports live capture and offline analysis (PCAP files)  

---

## Tool Overview

### Main Interface Components

- **Packet List Pane** → Shows captured packets  
- **Packet Details Pane** → Displays protocol layers (Ethernet, IP, TCP, etc.)  
- **Packet Bytes Pane** → Raw data in hex and ASCII  

### Capture Process

- Select network interface (Wi-Fi / Ethernet)  
- Start capture  
- Stop capture when needed  

---

## Packet Dissection

Each packet is broken into layers:

- **Frame Layer** → Physical transmission details  
- **Data Link Layer** → MAC addresses  
- **Network Layer** → IP addresses  
- **Transport Layer** → TCP/UDP ports  
- **Application Layer** → Protocol data (HTTP, DNS, etc.)  

### Key Fields to Observe

- Source IP / Destination IP  
- Source Port / Destination Port  
- Protocol type  
- Packet length  

---

## Packet Navigation

- Use packet numbers to track communication  
- Follow streams:
  - Right click → **Follow → TCP Stream**
- Helps reconstruct full conversations  

### Useful Navigation Tricks

- Sort packets by column (IP, protocol, length)  
- Use coloring rules to differentiate traffic  
- Identify request-response patterns  

---

## Packet Filtering

### Display Filters (Wireshark)

Used to filter captured traffic.

Examples:
- `ip.addr == 192.168.1.1` → Filter by IP  
- `tcp.port == 80` → Filter HTTP traffic  
- `dns` → Show only DNS packets  
- `http` → Show HTTP traffic  

### Capture Filters (before capture)

- `port 80` → Capture only HTTP traffic  
- `host 192.168.1.1` → Capture specific host  

---

## Common Use Cases

- Network troubleshooting  
- Detecting suspicious traffic  
- Analyzing protocols (HTTP, DNS, TCP)  
- Packet inspection in CTFs  

---

## Key Notes

- Wireshark does not generate traffic, only captures it  
- Requires proper permissions to capture packets  
- Encrypted traffic (HTTPS) cannot be fully read without keys  
- Filtering is essential for large captures
