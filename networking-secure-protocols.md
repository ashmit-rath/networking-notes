# Networking Secure Protocols

## TLS (Transport Layer Security)

TLS is a cryptographic protocol used to secure communication over a network.

- Provides encryption, integrity, and authentication  
- Used by many secure protocols (HTTPS, SMTPS, IMAPS, etc.)  
- Replaced SSL (older and insecure)  

---

## HTTPS (HTTP Secure)

Secure version of HTTP using TLS.

- Port: 443  
- Encrypts data between client and server  
- Prevents eavesdropping and man-in-the-middle attacks  

---

## Secure Email Protocols

### SMTPS (Secure SMTP)
- Port: 465 / 587  
- Used to send emails securely  
- Encrypts email transmission  

### POP3S (Secure POP3)
- Port: 995  
- Secure version of POP3  
- Downloads emails from server with encryption  

### IMAPS (Secure IMAP)
- Port: 993  
- Secure version of IMAP  
- Allows access to emails while keeping them on server  

---

## SSH (Secure Shell)

Used for secure remote access to systems.

- Port: 22  
- Encrypted alternative to Telnet  
- Used for remote login, command execution, file transfer  

---

## Secure File Transfer

### SFTP (SSH File Transfer Protocol)
- Runs over SSH  
- Secure file transfer with encryption  
- More secure than FTP  

### FTPS (FTP Secure)
- Uses TLS for encryption  
- Secure version of FTP  

---

## VPN (Virtual Private Network)

Creates a secure encrypted tunnel over a public network.

- Protects data from interception  
- Hides user IP address  
- Used for privacy and secure remote access  

---

## Insecure vs Secure Protocols

| Insecure | Port | Secure | Port      |
|----------|------|--------|-----------|
| HTTP     | 80   | HTTPS  | 443       |
| SMTP     | 25   | SMTPS  | 465 / 587 |
| POP3     | 110  | POP3S  | 995       |
| IMAP     | 143  | IMAPS  | 993       |

---

## Notes

- Secure protocols use encryption (mostly via TLS)  
- Insecure protocols transmit data in plaintext  
- SSH replaces Telnet for secure remote access  
- SFTP/FTPS are preferred over FTP  
- VPN adds an extra layer of security over networks
