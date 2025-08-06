
# 🔍 Network Reconnaissance Task – Internship Task 1

## ✅ Objective
Perform a local network scan to identify open ports and understand network exposure.

---

## 🛠 Tools Used
- **Nmap** (Network Mapper)
- Optional: Wireshark (not used in this task)

---

## 📜 Task Steps
1. **Find Local IP Range**
   - Example: `192.168.1.0/24`
   - Command:
     ```bash
     ip addr show
     ```
   
2. **Run TCP SYN Scan on Entire Network**
   ```bash
   nmap -sS 192.168.1.0/24 -oN scan_results.txt
   ```
   
3. **Scan Top 1000 Ports**
   ```bash
   nmap -sS --top-ports 1000 -T4 192.168.1.0/24 -oN top_ports.txt
   ```

4. **UDP Scan for Top 50 Ports**
   ```bash
   nmap -sU --top-ports 50 -T4 192.168.1.0/24 -oN udp_top50.txt
   ```

5. **Detailed Scan on a Specific Host**
   ```bash
   nmap -sV -O -Pn 192.168.1.127 -oN detailed_127.txt
   ```

6. **Full Port Scan on a Specific Host**
   ```bash
   nmap -sS -sV -O -p- 192.168.1.127 -oN full_scan_127.txt
   ```

---

## 📊 Findings
- **All TCP ports** across the network appeared **filtered** (no response).
- **UDP ports** showed as **open|filtered** (common due to firewalls).
- Host `192.168.1.127`:
  - No open TCP ports found (all filtered).
  - OS detection unreliable due to lack of open ports (guessed D-Link firewall, HP printer, older Windows versions).

---

## 🔐 Analysis
- **Why no open ports?**
  - Likely due to **firewall settings** or **router security features** blocking Nmap probes.
- **Risk Level**:
  - Minimal exposure (good security posture).
  - No visible attack surface for external attackers.

---

## ✅ What I Learned
- How to perform TCP and UDP scans.
- How firewalls affect scanning results.
- Importance of open ports for OS and service detection.

---

## 📂 Files in This Repo
- `scan_results.txt` – Initial network scan
- `top_ports.txt` – Top 1000 TCP ports scan
- `udp_top50.txt` – Top 50 UDP ports scan
- `detailed_127.txt` – Detailed scan of host 192.168.1.127
- `full_scan_127.txt` – Full port scan of host 192.168.1.127

---

## 📌 Conclusion
The local network is highly secured with no exposed open ports, demonstrating strong firewall policies.

---
