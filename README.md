# 🕵️‍♂️ Project 4 — Web Application CTF Challenge

## 📘 Overview
This repository documents my **Capture The Flag (CTF)** project from the **Cyber Security & Ethical Hacking Internship**.  
The challenge involved analyzing a vulnerable web application deployed on a local VirtualBox machine, performing reconnaissance and enumeration, exploiting vulnerabilities, and capturing six hidden flags.

---

## 🎯 Objectives
- Deploy and analyze a vulnerable web application.
- Perform reconnaissance, enumeration, and vulnerability analysis.
- Identify and capture six (6) hidden flags.
- Document findings and remediation recommendations.

---

## 🧰 Tools & Environment
| Tool | Purpose |
|------|----------|
| Kali Linux | Attacker system |
| Oracle VirtualBox | VM host for vulnerable machine |
| Nmap | Port and service discovery |
| Gobuster / Dirb | Directory enumeration |
| Burp Suite | HTTP interception and testing |
| Curl / Browser | Manual inspection and validation |

**Network Mode:** Bridged Adapter  
**Target VM IP:** `192.168.248.96`

---

## 💾 Virtual Machine
Due to GitHub file size limits, the vulnerable VirtualBox machine (≈3 GB) is hosted externally.  

📦 **Download Link:**  
👉 [Google Drive – CTF Challenge VM](https://drive.google.com/file/d/1nYg_YWRvZn1ERzJ9hYO-umF7fo4RcXGs/view?usp=drive_link)

After downloading:
1. Open **Oracle VirtualBox**
2. Go to **File → Import Appliance**
3. Select the `.ova` file and import it
4. Set Network Mode to **Bridged Adapter**
5. Start the machine and note the IP displayed on startup

---

## 🖼️ Screenshots

- `vm_import.png`
- `nmap_scan.png`
- `gobuster_output.png`
- `flag1_found.png`
- `flag_summary.png`
- `report_cover.png`

### 🧩 VM Deployment
*(Importing the CTF Appliance in VirtualBox)*  
![VM Setup](screenshots/vm_import.png)

---

### 🔍 Reconnaissance
**Nmap Scan** — discovering open ports and services  
![Nmap Scan](screenshots/nmap_scan.png)

**Gobuster Enumeration** — discovering hidden directories  
![Gobuster Output](screenshots/gobuster_output.png)

---

### 🏁 Flag Discovery
Each flag was obtained by inspecting web directories and source code:

| Flag | Path | Method |
|------|------|---------|
| 1 | `/flag1.txt` | Direct access |
| 2 | `/robotx.txt` | Discovered via enumeration |
| 3 | `/pages/BlogPostCcomponent.html` | Found in HTML comments |
| 4 | `/4dm1n` | Exposed admin area |
| 5 | `/c0nf1g` | Configuration file |
| 6 | `/4dm1n` | Additional flag in admin panel |

Example flag discovery:  
![Flag Found](screenshots/flag1_found.png)

---

## ⚙️ Methodology
1. **Reconnaissance** — Identify open ports with `nmap`.  
2. **Enumeration** — Use `gobuster` or `dirb` to reveal hidden paths.  
3. **Manual Analysis** — Inspect pages, comments, and configurations.  
4. **Flag Collection** — Retrieve all six hidden flags.  
5. **Reporting** — Document findings and propose mitigations.

---

## 🔐 Vulnerability Analysis
| Issue | Description | Risk |
|-------|--------------|------|
| Exposed config files | Contain sensitive info (credentials) | High |
| Weak admin access control | Accessible via predictable `/4dm1n` path | High |
| Hidden files in webroot | Leakage of internal data | Medium |
| Lack of directory restrictions | Easy brute-force enumeration | Medium |

---

## 🛡️ Recommendations
- Restrict admin access (strong authentication, MFA).
- Remove sensitive files from the web root.
- Disable directory listing.
- Implement proper access controls and logging.
- Regularly scan for exposed resources.

---

## 📄 Documentation
The complete report includes detailed findings, commands, screenshots, and recommendations.

📘 **[View Report (PDF)](report/CTF_Report_Project_4_Polished_Final.pdf)**

---

## 👤 Author
**Oppong Isaac**  
Cyber Security & Ethical Hacking Internship — Project 4  
October 2025  

---
