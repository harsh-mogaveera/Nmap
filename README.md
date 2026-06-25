# Nmap
Scanning the network!
#  Network Scanning and Enumeration using Nmap

##  Project Overview

This project demonstrates network scanning and reconnaissance techniques using Nmap. The objective was to identify active hosts, discover open ports, detect running services, and analyze network exposure within a local network environment.


##  Objectives

* Perform host discovery in a local network
* Identify open and closed ports
* Detect running services and versions
* Analyze network security exposure
* Understand network structure and connectivity


##  Tools Used

* Kali Linux
* Nmap


##  Methodology

### 1. Host Discovery

Identified active devices in the network using ping scan:

``Bash : 
nmap -sn 192.168.x.x
``

### 2. Basic Port Scanning

Scanned a specific host to identify open ports:

``Bash:
nmap 192.168.x.x
``

### 3. Stealth (SYN) Scan

Performed a stealth scan to detect open ports without completing full connections (without completing 3-way handshake method) or half scan:

``bash:
nmap -sS 192.168.x.x
``

### 4. Service Version Detection

Identified services and their versions running on open ports:

``bash:
nmap -sV 192.168.x.x
``

### 5. Aggressive Scan

Performed detailed scan including OS detection, version detection, and traceroute:

``bash:
sudo nmap -A 192.168.x.x
``

### 6. Network-Wide Scan

Scanned the entire subnet to identify all active hosts:

``bash:
nmap 192.168.x.0/24
``

### 7. Fast Scan

Performed a quick scan of common ports:

``bash:
nmap -F 192.168.x.x
``


### 8. Specific Port Scan

Scanned selected ports for targeted analysis:

``bash:
nmap -p 22,80,443 192.168.x.x
``

22- ssh, 80-http, 443-https

### 9. OS Detection

Detects Operating System

``bash:
nmap -O 192.168.x.x
``


##  Results and Findings

* Identified multiple active hosts within the network
* Discovered open ports such as RPC (135), NETBIOS SSN (139), SMB (445) and MYSQL (3306) in entire network scanning
* Discovered open port such as DNS (53) in single host scan 
* Detected services in file sharing services
* Observed closed/open ports indicating firewall presence
* Traceroute analysis showed network proximity of target systems



##  Security Analysis

* Systems with multiple open ports present a higher attack surface
* Open services such as SMB and HTTP may expose vulnerabilities but for internet surface for home network can be safe
* Filtered ports indicate firewall or security controls in place
* Lack of services on common ports suggests reduced exposure



## Limitations

* Scans were limited to a local network environment
* Results may depending on firewall and network configuration
* No active exploitation was performed



##  Conclusion

This project provided practical experience in network reconnaissance and port scanning. It helped in understanding how attackers and security professionals identify exposed services and assess potential risks in a network.



