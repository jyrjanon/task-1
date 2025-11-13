## Overview
In this task, I performed a port scan on my local network to identify active devices, the ports they expose, and potential security risks.  
This helped me understand basic network reconnaissance techniques and how attackers analyze networks.

I used **Zenmap (Graphical Nmap)** to complete this task.

---

## Tools Used
- **Nmap / Zenmap GUI**
- **Windows CMD** (to check local IP range)

---

##  Network Range Scanned
I scanned my private internal subnet:

(Actual IP range hidden in this README.)
You can check .xml file
---

##  Scan Command Used
Generated automatically by Zenmap:


---

##  Scan Summary (IPs Hidden)

A total of **4 devices** were detected on my network:

---

###  **Router (Home Gateway)**
**Open Ports:**
- 21 (FTP) – ⚠ Insecure
- 22 (SSH)
- 80 (HTTP)
- 443 (HTTPS)

**Note:**  
FTP (port 21) should be disabled if not required, as it sends data unencrypted.

---

### 2️ **Smart TV (IoT – LG TV)**
**Open Ports:**
- 3000, 3001, 7000, 8008, 8009, 8443  
These are typical for smart TV services and DLNA/AirPlay functionality.

---

### 3️ **Windows Laptop/PC**
**Open Ports:**
- 135 (MSRPC)
- 139 (NetBIOS)
- 445 (SMB)

**Note:**  
These are normal Windows service ports but can be exploited if malware spreads in the local network.

---

### 4️ **Unknown Device**
- Device was active but had **no open ports**, likely due to strict firewall settings.

---

##  Security Risks Identified
### High Risk
- **FTP on router (port 21)** — should be disabled; sends data without encryption.

###  Medium Risk
- **SMB (445)** on the Windows device — commonly targeted by malware inside LANs.

###  Low Risk / Normal
- Smart TV exposing multiple ports is normal for IoT devices, but still increases attack surface.

---

##  Recommendations
- Disable **FTP (port 21)** on router.
- Update router and IoT firmware regularly.
- Use a strong password for router admin access.
- Restrict SMB (Windows sharing) to trusted devices only.
- Perform periodic Nmap scans to check for unknown devices.


---

##  What I Learned
- How to run a port scan using Nmap/Zenmap  
- How to analyze open ports and services  
- Different device behaviors on a local network  
- Basic identification of network risks  
- Importance of securing internal home/office networks  

---
