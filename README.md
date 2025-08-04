# 🔍 Task 1: Local Network Port Scanning using Nmap & Wireshark

## 🧠 Objective
To perform network reconnaissance on the local network to identify active devices, open ports, running services, and understand how attackers can use port scanning to assess network exposure.

---

## 🛠️ Tools Used
- **Nmap** – for scanning IP ranges and identifying open ports and services.
- **Wireshark** – for capturing and analyzing TCP handshakes during Nmap scans.
- **Linux (Kali)** – as the virtual lab environment.

---

## 🧪 Scanning Techniques Performed

### 1. `-sS` (TCP SYN Scan)
- Stealthy half-open scan.
- Identifies open ports without completing the TCP handshake.

### 2. `-sV` (Service Version Detection)
- Detects the version of services running on open ports.
- Useful for identifying vulnerabilities tied to specific software versions.

### 3. `-O` (OS Detection)
- Attempts to identify the operating system running on target hosts.

### 4. `-PN` (No Ping Scan)
- Skips host discovery (treats all IPs as alive).
- Useful when ICMP is blocked by firewalls.

### 5. `-sn` (Ping Scan)
- Detects live hosts without performing port scans.
- Useful for network inventory and availability checking.

---

## 📁 Example Scan Commands Used 
```bash
nmap -sS 192.168.1.0/24
nmap -sV 192.168.1.0/24
nmap -O 192.168.1.0/24
nmap -PN 192.168.1.0/24
nmap -sn 192.168.1.0/24

