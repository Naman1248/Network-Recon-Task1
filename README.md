# 🔍 Network Reconnaissance Project – Internship Task 1

This repository contains two major parts:

## 📁 Local-Scan
Local network scanning performed on my home network using **Nmap**. Includes:
- TCP SYN scan on the entire subnet
- Top 1000 ports scan
- UDP top 50 ports scan
- Detailed scan of a specific host (192.168.1.127)
- Full port scan of the same host

[View Local Scan Details](Local-Scan/README.md)

---

## 📁 Metasploitable-Scan
Advanced scanning on **Metasploitable 2** vulnerable machine. Includes:
- Basic service detection scan
- Full port scan
- OS detection
- Vulnerability scan using Nmap scripts

[View Metasploitable Scan Details](Metasploitable-Scan/README.md)

---

### ✅ Objective
Perform network reconnaissance tasks on both:
1. **Secure local network** (expected minimal exposure).
2. **Intentionally vulnerable machine (Metasploitable 2)** to practice finding open ports and vulnerabilities.

---

### 🛠 Tools Used
- **Nmap** (Network Mapper)
- **Metasploitable 2 VM** (Vulnerable Linux machine)

---

### 📌 Key Learnings
- Difference between a secured network and a vulnerable system.
- How to identify open ports and services using different Nmap scan techniques.
- Detecting vulnerabilities using Nmap scripts.
