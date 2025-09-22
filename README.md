# Task 1: Local Network Port Scan using Nmap

## 🧠 Objective
Discover devices and open ports on the local network to assess possible exposures.

## 🛠 Tools Used
- [Nmap](https://nmap.org/) for scanning
- Wireshark (optional) for packet analysis
- Windows Command Prompt / PowerShell

## 📝 What I Did
1. Installed Nmap
2. Identified my local IP and subnet (`192.168.1.0/24`) using IPconfig command in Command Prompt.
3. Scanned the network for live devices: nmap -sS 192.168.1.0/24
4. Scanned my own device to check open ports: nmap -sV 192.168.1.35
5. Analyzed the open ports and services
6. Took notes on security risks
7. Saved scan results as `.xml` files

## 📎 Files Included
- `scan_results/full_scan.txt` - Scan of entire subnet
- `scan_results/my_device_scan.txt` - Scan of my own IP
- Screenshots of Nmap output
- This README

## 🛡️ Security Notes
Ports 135, 139, and 445 are potentially risky and should not be exposed outside the LAN.



