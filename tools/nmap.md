# Nmap

Network scanning and enumeration tool.

## Basic Syntax
```bash
nmap [options] <target>
```

## Common Scans

| Command | Purpose |
|---------|---------|
| `nmap -sC -sV <target>` | Default scripts + version detection |
| `nmap -p- <target>` | Scan all 65535 ports |
| `nmap -sU <target>` | UDP scan |
| `nmap -A <target>` | Aggressive scan (OS, version, scripts, traceroute) |
| `nmap -sn <target>` | Ping sweep, no port scan |

## Output Formats
```bash
-oN filename    # Normal output
-oX filename    # XML output
-oG filename    # Greppable output
-oA filename    # All formats simultaneously
```

## Useful Options
```bash
--min-rate 5000     # Speed up scan
--max-retries 1     # Reduce retries
-T4                 # Aggressive timing template
-v                  # Verbose output
```

## My Standard Starting Scan
```bash
# Step 1 - Quick initial scan
nmap -sC -sV -oN nmap/initial <target>

# Step 2 - Full port scan
nmap -p- --min-rate 5000 -oN nmap/allports <target>

# Step 3 - Targeted scan on discovered ports
nmap -sC -sV -p <ports> -oN nmap/targeted <target>
```

---

*Updated as I learn new options and techniques.*
