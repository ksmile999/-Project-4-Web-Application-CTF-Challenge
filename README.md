# 🕵️‍♂️ Project 4 — Web Application CTF Challenge

## 📘 Overview
This repository contains documentation and supporting materials for a Capture The Flag (CTF) challenge completed as part of a Cyber Security & Ethical Hacking Internship.

The exercise involved analyzing a vulnerable web application hosted in a VirtualBox sandbox, identifying potential vulnerabilities, and retrieving six hidden flags through manual penetration testing.

---

## 🎯 Objectives
- Deploy and analyze a vulnerable web application.
- Perform reconnaissance, enumeration, and vulnerability testing.
- Identify and capture six (6) planted flags.
- Document findings and recommend mitigations.

---

## 🧰 Tools Used
- **Operating System:** Kali Linux  
- **Tools:** Nmap, Gobuster, Dirb, Burp Suite, Curl, Browser  
- **Environment:** Oracle VirtualBox (Bridged Adapter mode)

---

## ⚙️ Methodology
1. **Reconnaissance:** Used `nmap` to discover open ports and services.  
2. **Enumeration:** Employed `gobuster` to identify hidden directories.  
3. **Analysis:** Investigated accessible pages (`/4dm1n`, `/c0nf1g`, `/robotx.txt`, etc.).  
4. **Exploitation:** Retrieved and documented 6 flags from web-accessible files.  
5. **Reporting:** Findings compiled into a professional PDF report.

---

## 🏁 Findings Summary
| Flag | Location | Description |
|------|-----------|-------------|
| 1 | `/flag1.txt` | Exposed file on web root |
| 2 | `/robotx.txt` | Sensitive file revealed via enumeration |
| 3 | `/pages/BlogPostCcomponent.html` | Flag in HTML source |
| 4 | `/4dm1n` | Admin path exposure |
| 5 | `/c0nf1g` | Misconfigured settings file |
| 6 | `/4dm1n` | Additional flag under admin page |

---

## 📄 Documentation
The full report includes all findings, commands, screenshots, and remediation recommendations.

📘 **[Download Report (PDF)](report/CTF_Report_Project_4_Polished_Final.pdf)**

---

## 🔐 Remediation Recommendations
- Remove sensitive files from webroot.  
- Restrict admin interface access.  
- Disable directory listings.  
- Implement strong authentication and logging.  
- Regularly scan for misconfigurations.

---

## 👤 Author
**Oppong Isaac**  
Cyber Security & Ethical Hacking Internship Project  
October 2025
