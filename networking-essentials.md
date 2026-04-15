# Networking Essentials

## DHCP (Dynamic Host Configuration Protocol)

Automatically assigns IP configuration (IP address, subnet mask, gateway) to devices in a network.

### DORA Process
- **Discover** → Client broadcasts to locate DHCP server  
- **Offer** → Server offers an IP configuration  
- **Request** → Client requests the offered IP  
- **Acknowledge** → Server confirms and assigns IP  

---

## ARP (Address Resolution Protocol)

Used to map an IP address to a MAC address within a local network.

- **ARP Request** → Broadcast asking for MAC of a specific IP  
- **ARP Reply** → Device responds with its MAC address  

---

## ICMP (Internet Control Message Protocol)

Used for network diagnostics and error reporting.

- `ping` → Checks connectivity between devices  
- `traceroute` → Displays path taken by packets  

---

## Routing

Routing is the process of determining the best path for data transmission.

### OSPF (Open Shortest Path First)
- Link-state routing protocol  
- Uses shortest path algorithm (Dijkstra)

### EIGRP (Enhanced Interior Gateway Routing Protocol)
- Hybrid routing protocol  
- Shares routing info to find optimal path  

### RIP (Routing Information Protocol)
- Distance-vector routing protocol  
- Uses hop count (max 15 hops)

### BGP (Border Gateway Protocol)
- Used for routing between large networks (Internet)  
- Path selection based on policies  

---

## NAT (Network Address Translation)

Translates private IP addresses into public IP addresses.

- Allows multiple devices to use a single public IP  
- Conserves IP addresses  
- Adds a layer of isolation  

---

## Key Notes

- DHCP removes manual IP configuration  
- ARP works only inside LAN  
- ICMP is used for diagnostics, not actual data transfer  
- Routing protocols differ based on use-case  
- NAT is common in routers and firewalls
