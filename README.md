# Network Port Scan - Task 1

## Objective
Perform network reconnaissance on local hosts to identify open ports and understand potential security risks.

## Tools Used
- **Nmap** – for scanning hosts and discovering open ports
- **Wireshark** – for analyzing packet captures (SYN/SYN-ACK handshake)
- **PowerShell** – to run Nmap scans and save results

## Steps Taken
1. Installed Nmap and identified the local IP range.
2. Performed a TCP SYN scan using Nmap:  
3. Recorded open ports and host IPs from Nmap output.
4. Captured packet data in Wireshark to verify open ports using SYN → SYN/ACK handshake.
5. Noted the common services running on each open port.
6. Assessed potential security risks associated with each open port.

## Results / Findings
- Open ports for host `Host-1 and Host-0` included:
- **21/tcp (FTP)** – Medium risk, file transfer service
- **445/tcp (SMB)** – High risk, file sharing service
- **139/tcp (NetBIOS-SSN)** – High risk, may leak internal info
- **1521/tcp (Oracle DB listener)** – High risk, database access
- **8000/tcp (HTTP-alt)** – Medium risk, alternative web service
- Wireshark evidence confirmed SYN → SYN/ACK handshake for most ports.

## Files Included
- `Scanning_OpenPorts.html` – open ports, Wireshark evidence(summary), services, and risks


## Conclusion
This task demonstrated basic network reconnaissance skills, including scanning local hosts for open ports, analyzing packet captures, identifying services running on the ports, and assessing potential security risks.
