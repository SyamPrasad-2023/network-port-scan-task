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
4. Scanned my own device to check open ports: nmap -sV 192.168.1.**
5. Analyzed the open ports and services
6. Took notes on security risks
7. Saved scan results as `.xml` files

## ✅ Key Results
Scanned IP: **192.168.1.** (this machine)**  
Discovered **16 open TCP ports**, including:
- RPC: 135
- SMB: 139, 445
- Oracle DB: 1521
- Node-RED: 1880
- Web services: 8080, 7070
- Windows system ports: 5040, 7680
- Dynamic high ports: 49664–49686

## ⚠️ Security Considerations
- Legacy ports (135, 139, 445) are often targeted — should be firewalled or disabled
- Oracle DB and Node-RED ports should not be exposed without proper authentication
- Web services (8080, 1880) must be hardened if public

## 📎 Files
- `nmap_Intense_scan_all_TCP_Ports.xml`: Full port scan results
- `nmap_Intense Scan plus UDP.xml` : scan result
- Screenshots of Nmap output


## 🛡️ Security Notes
Ports 135, 139, and 445 are potentially risky and should not be exposed outside the LAN.



