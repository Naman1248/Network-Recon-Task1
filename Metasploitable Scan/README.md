
# 🖥 Metasploitable 2 Scan Report

### 🔍 Objective
Perform an advanced Nmap scan on Metasploitable 2 to identify open ports, services, OS details, and potential vulnerabilities.

---

### 🛠 Commands Used
```bash
# Basic service detection scan
nmap -sS -sV 192.168.6.128 -oN metasploitable_basic.txt

# Full port scan
nmap -p- -sS -sV 192.168.6.128 -oN metasploitable_full.txt

# OS detection
nmap -O 192.168.6.128 -oN metasploitable_os.txt

# Vulnerability scan
nmap -sV --script=vuln 192.168.6.128 -oN metasploitable_vuln.txt
```

---

### 📊 Findings
**Open Ports & Services (Highlights):**
- **21/tcp open ftp** (vsftpd 2.3.4) → *Backdoor vulnerability (CVE-2011-2523)*
- **22/tcp open ssh** (OpenSSH 4.7p1)
- **23/tcp open telnet**
- **25/tcp open smtp**
- **80/tcp open http** (Apache httpd 2.2.8)
- **3306/tcp open mysql**
- **5432/tcp open postgresql**
- **8080/tcp open http-proxy (Apache Tomcat)**

**OS Detected:** Linux 2.6.x (Ubuntu-based).

---

### ⚠️ Vulnerabilities Found
- **FTP Backdoor (vsftpd 2.3.4)** → Allows remote shell.
- **Apache HTTPD Slowloris DoS**.
- **Tomcat Manager Remote Code Execution**.
- **SSL POODLE Attack**.
- **Multiple SQL Injection Points (Mutillidae)**.

---

### 🔐 Risk Analysis
Metasploitable 2 is intentionally vulnerable and should never be exposed to the internet. These vulnerabilities can lead to:
- Remote Code Execution
- Privilege Escalation
- Denial of Service
- Data Exfiltration

---
