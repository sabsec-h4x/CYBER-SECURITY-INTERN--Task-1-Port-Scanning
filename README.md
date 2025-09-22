# CYBER-SECURITY-INTERN--Task-1-Port-Scanning
# Task 1 - Local Network Port Scanning

## Objective
Discover open ports in the local network to understand network exposure.

## Tools Used
- Nmap
- (Optional) Wireshark

## Commands Used
- `ip a` - find local IP and netmask
- `sudo nmap -sS -sV -O 192.168.1.0/24 -oN scan_results.txt`

## Findings (example)
- `192.168.1.5` — Ports: 22/tcp (SSH), 80/tcp (HTTP)
- `192.168.1.10` — Ports: 445/tcp (SMB)

## Risks Identified
- SSH open: possible brute-force attacks — enable key auth, fail2ban
- HTTP open: ensure web server is patched, remove unnecessary pages
- SMB open: disable if not needed or restrict via firewall

## Files in this repo
- `scan_results.txt` — raw nmap output / notes
- `screenshots/` — Nmap/Wireshark screenshots
- `README.md` — this file

## How I ran the scan
1. Determined local IP range with `ip a`.
2. Ran `sudo nmap -sS -sV -O 192.168.1.0/24 -oN scan_results.txt`.
3. Saved screenshots and wrote this README.

