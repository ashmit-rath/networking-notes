# Networking Core Protocols

## DNS (Domain Name System)

Resolves domain names to IP addresses. Operates at the application layer.

- Uses UDP (default) and TCP (fallback) on port 53  
- UDP is faster; TCP is used for large responses or reliability  

### DNS Record Types
- A Record → Maps domain to IPv4 address  
- AAAA Record → Maps domain to IPv6 address  
- CNAME Record → Alias for another domain name  
- MX Record → Specifies mail servers for a domain  

---

## WHOIS

Used to retrieve information about domain ownership.

- Shows registrar details, registration dates, and ownership info  
- Example:
  whois example.com  

---

## HTTP / HTTPS

Protocols used for communication between client (browser) and server.

- HTTP (Port 80) → Unencrypted  
- HTTPS (Port 443) → Encrypted using TLS  

### Key Points
- Stateless protocol  
- Request-response model  
- Common methods: GET, POST, PUT, DELETE  

---

## IMAP (Internet Message Access Protocol)

Used for retrieving emails from a mail server.

### Common Commands
- LOGIN <username> <password> → Authenticate user  
- SELECT <mailbox> → Select mailbox  
- FETCH <message> → Retrieve email  
- MOVE <sequence-set> → Move messages  
- COPY <sequence-set> → Copy messages  
- LOGOUT → End session  

- Runs on TCP port 143  
- Secure version (IMAPS) uses port 993  

---

## Common Protocols and Ports

TELNET → TCP → 23  
DNS → UDP/TCP → 53  
HTTP → TCP → 80  
HTTPS → TCP → 443  
FTP → TCP → 21  
SMTP → TCP → 25  
POP3 → TCP → 110  
IMAP → TCP → 143  

---

## Notes

- DNS translates domain names to IP addresses  
- HTTPS is secure version of HTTP using encryption  
- IMAP keeps emails on server (unlike POP3)  
- Ports are important for identifying services in networking
