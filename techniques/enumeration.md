# Enumeration

Notes on enumeration techniques and methodology.

## Nmap
```bash
# Basic scan
nmap -sC -sV -oN nmap/initial <target>

# Full port scan
nmap -p- --min-rate 5000 -oN nmap/allports <target>

# UDP scan
nmap -sU --top-ports 100 -oN nmap/udp <target>
```

## Web Enumeration
```bash
# Directory busting
gobuster dir -u http://<target> -w /usr/share/wordlists/dirb/common.txt

# Subdomain enumeration
gobuster dns -d <domain> -w /usr/share/wordlists/SecLists/Discovery/DNS/subdomains-top1million-5000.txt
```

## SMB Enumeration
```bash
# List shares
smbclient -L //<target> -N

# Enumerate with enum4linux
enum4linux -a <target>
```

---

*Updated as I discover new techniques.*
