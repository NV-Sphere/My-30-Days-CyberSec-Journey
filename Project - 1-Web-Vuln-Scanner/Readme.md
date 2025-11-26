# 🛡️ Web Application Vulnerability Scanner (Project 01)
## 🚀 Advanced Security Assessment Platform

**Status:** Production Ready

---

### 🎯 Project Overview:
This project is a production-grade vulnerability scanner developed as part of the **ElevateLab Cyber Security Internship**. Moving beyond basic academic requirements, this tool was engineered to be a full-stack **Bug Hunting Framework**.

It is designed to detect critical web vulnerabilities (**OWASP Top 10**) while handling modern security challenges like **WAF Evasion (Cloudflare)** and **Dynamic JavaScript Rendering**.

---

### 🔑 Key Features:
* **WAF Bypass:** Integrated `cloudscraper` to bypass Cloudflare protections.
* **Dynamic Analysis:** Uses Selenium (Headless Chrome) to render JS and detect DOM-based XSS.
* **Modular Payload System:** Attacks are loaded from external `.txt` files, allowing dynamic updates without code changes (Infinitely Scalable).
* **Professional Reporting:** Auto-generates detailed PDF reports with CVSS scoring and mitigation advice.

---

### 📸 Visual Walkthrough:

#### 1. The Dashboard
A real-time, Flask-based interface for managing scans and viewing live findings.
![Dashboard Screenshot](path/to/dashboard_image.png)

#### 2. Modular Architecture Proof (The Payload Engine)
The core strength is the separation of attack logic from the payloads. The scanner automatically adapts to new attack vectors added by researchers.

**Full Scope of Detection Modules:**

| Category | Attack Vector Files (Payloads) | Detection Capability |
| :--- | :--- | :--- |
| **Injection Attacks** | `sqli.txt`, `xss.txt`, `ssti.txt`, `nosql.txt`, `cmd_injection.txt`, `ldap_xpath.txt` | Covers SQL Injection, Cross-Site Scripting, Server-Side Template Injection, NoSQL/LDAP Injection, and OS Command Injection. |
| **Access Control** | `lfi.txt`, `rfi.txt`, `idor_params.txt`, `open_redirect.txt` | Detects Local/Remote File Inclusion, Insecure Direct Object References (IDOR), and Unvalidated Redirects. |
| **Server Misconfig** | `ssrf.txt`, `xxe.txt`, `host_header.txt` | Identifies Server-Side Request Forgery, XML External Entities, and Host Header Injection risks. |

*(The complete structure is verified in the `payloads/` directory.)*

#### 3. Scan Execution (Terminal & Logs)
The multi-threaded engine running in the background, handling complex requests and WAF tokens.
![Terminal Execution](path/to/terminal_image.png)

#### 4. Professional PDF Report
An example of the automated report generated after a scan completion.
![PDF Report Sample](path/to/report_image.png)

---

### 🔧 Technical Architecture:
The tool relies on a **Modular Orchestrator Architecture**:

* **Controller:** Manages the web server and UI logic (`app.py`).
* **Injection Engine:** A specialized fuzzer that iterates through the payload files.
* **Data Layer (`/payloads`):** Contains thousands of attack vectors organized by vulnerability type.

---

### 📦 Dependencies:
* Python 3.x
* Flask (Web Framework)
* Selenium (Browser Automation)
* Cloudscraper (WAF Bypass)
* BeautifulSoup4 (HTML Parsing)
* FPDF (Report Generation)

---

### ⚠️ Disclaimer
> **This tool is for educational and authorized testing purposes only.**
>
> The core scanning engine files (Python source code) have been excluded from this public repository. The structure, payloads, and reports provided here demonstrate the full functionality and architecture of the project.
