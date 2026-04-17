# Nmap: The Basics

## Introduction

Nmap (Network Mapper) is a network scanning tool used to discover hosts, open ports, services, and system details.

- Used in reconnaissance phase
- Works by sending packets and analyzing responses
- Can detect OS, services, and vulnerabilities (basic level)

---

## Basic Syntax

nmap [options] <target>

Example:
nmap 192.168.1.1

---

## Host Discovery

### List targets (no scan)
nmap -sL 192.168.1.0/24

### Ping scan (who is online)
nmap -sn 192.168.1.0/24

### Skip host discovery (treat all as alive)
nmap -Pn 192.168.1.1

---

## Port Scanning Techniques

### TCP Connect Scan (default, no root)
nmap -sT 192.168.1.1

### SYN Scan (stealth, requires root)
nmap -sS 192.168.1.1

### UDP Scan
nmap -sU 192.168.1.1

---

## Port Selection

### Scan specific ports
nmap -p 22,80,443 192.168.1.1

### Scan range
nmap -p 1-1000 192.168.1.1

### Scan all ports
nmap -p- 192.168.1.1

### Fast scan (top 100 ports)
nmap -F 192.168.1.1

---

## Service & OS Detection

### Service version detection
nmap -sV 192.168.1.1

### OS detection
nmap -O 192.168.1.1

### Aggressive scan (OS + version + scripts)
nmap -A 192.168.1.1

---

## Timing Control

### Timing templates (0–5)
nmap -T0 192.168.1.1   # slow (stealth)
nmap -T3 192.168.1.1   # default
nmap -T5 192.168.1.1   # fastest

---

## Advanced Performance Options

### Parallel probes
nmap --min-parallelism 10 --max-parallelism 50 192.168.1.1

### Packet rate
nmap --min-rate 100 --max-rate 1000 192.168.1.1

### Timeout control
nmap --host-timeout 30s 192.168.1.1

---

## Output & File Saving

👉 Filename ALWAYS comes after output flag

### Normal output
nmap -oN output.txt 192.168.1.1

### XML output
nmap -oX output.xml 192.168.1.1

### Grepable output
nmap -oG output.grep 192.168.1.1

### All formats
nmap -oA scan_result 192.168.1.1

👉 This creates:
- scan_result.nmap
- scan_result.xml
- scan_result.gnmap

---

## Verbosity & Debugging

### Verbosity
nmap -v 192.168.1.1
nmap -vv 192.168.1.1

### Debug mode
nmap -d 192.168.1.1
nmap -d9 192.168.1.1

---

## Practical Examples

### Basic scan
nmap 192.168.1.1

### Scan all ports + save output
nmap -p- -oN full_scan.txt 192.168.1.1

### Stealth scan + version detection
nmap -sS -sV 192.168.1.1

### Aggressive scan + save all outputs
nmap -A -oA aggressive_scan 192.168.1.1

### Scan network range
nmap -sn 192.168.1.0/24

---

## Key Notes

- Default scan uses TCP connect (non-root)
- SYN scan requires root privileges
- -Pn skips host discovery (useful if ICMP blocked)
- -A is powerful but noisy
- Output files are important for reporting and later analysis
