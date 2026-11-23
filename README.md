
<div align="center">

# NETWORKWALKS CYBERSECURITY INTERNSHIP

### WEEK 4 — MEDIROZA GENERAL HOSPITAL
### PENETRATION TESTING PROJECT

<p>
  <img src="https://img.shields.io/badge/NETWORKWALKS-CYBERSECURITY-1565C0?style=for-the-badge" alt="NetworkWalks Cybersecurity">
  <img src="https://img.shields.io/badge/BATCH-B084-2E7D32?style=for-the-badge" alt="Batch B084">
  <img src="https://img.shields.io/badge/WEEK-04-ED6C02?style=for-the-badge" alt="Week 4">
  <img src="https://img.shields.io/badge/PROJECT-PENETRATION_TESTING-8E24AA?style=for-the-badge" alt="Penetration Testing">
</p>

<p>
  <img src="https://img.shields.io/badge/Kali_Linux-557C94?style=flat-square&logo=kalilinux&logoColor=white" alt="Kali Linux">
  <img src="https://img.shields.io/badge/Nmap-Network_Scanning-004B87?style=flat-square" alt="Nmap">
  <img src="https://img.shields.io/badge/John_the_Ripper-Password_Auditing-333333?style=flat-square" alt="John the Ripper">
  <img src="https://img.shields.io/badge/ExifTool-Metadata_Analysis-00796B?style=flat-square" alt="ExifTool">
  <img src="https://img.shields.io/badge/Focus-Web_Application_Security-red?style=flat-square" alt="Web Application Security">
</p>

**A practical penetration testing project covering reconnaissance, initial access, sensitive data exposure, PDF password assessment and security reporting.**

[GitHub Profile](https://github.com/josuemutsiirwa) •
[LinkedIn Profile](https://www.linkedin.com/in/josue-matembera-37a269407/)

</div>

---

# 1. Project Overview

Welcome to my **Week 4 Cybersecurity Internship Project**, completed as part of the NetworkWalks Cybersecurity Internship, Batch B084.

This project focuses on a black-box penetration testing assessment of **Mediroza General Hospital**. The objective was to assess the security of the authorized target, identify vulnerabilities, demonstrate their potential impact through the assigned lab activities, and document the findings in a professional penetration testing report.

The assignment was divided into four milestones:

| Milestone | Title | Main Objective |
|---|---|---|
| M1 | Initial Access | Identify weaknesses in the website and retrieve three patient PDF lab reports. |
| M2 | Data Extraction | Assess and recover access to the encryption-protected PDF files. |
| M3 | Attack (Cracking) | Identify the hospital employees' salaries and shareholder details, and investigate further exposure. |
| M4 | Penetration Testing Report | Document the assessment, evidence, risk ratings and remediation recommendations. |

This repository documents the practical activities, tools, observations and evidence associated with these milestones.

## Project Information

| Item | Details |
|---|---|
| Program | NetworkWalks Cybersecurity Internship |
| Batch | B084 |
| Project | Week 4 – Mediroza Penetration Testing |
| Client | Mediroza General Hospital |
| Target | `https://medirozahospital.com` |
| Assessment Type | Black-box Penetration Testing |
| Testing Environment | Kali Linux |
| Milestones | M1, M2, M3 and M4 |
| Authorization | Written authorization stated in the project brief |

---

# 2. Intern Information

| Detail | Information |
|---|---|
| Full Name | **Mutsiirwa Matembera Josué** |
| Program | Cybersecurity Internship |
| Training Organization | NetworkWalks |
| Batch | B084 |
| Project Week | Week 4 |
| Project Title | Mediroza General Hospital Penetration Testing |

**Professional Profiles**

- GitHub: [github.com/josuemutsiirwa](https://github.com/josuemutsiirwa)
- LinkedIn: [Josué Matembera](https://www.linkedin.com/in/josue-matembera-37a269407/)

---

# 3. Project Scope and Authorization

The Week 4 project brief defines the engagement as a full black-box penetration test of the Mediroza General Hospital web infrastructure.

### 3.1 Scope

The assessment focused on:

- Reconnaissance and identification of exposed entry points.
- Enumeration of accessible website resources and services.
- Examination of authentication and user-input handling.
- Assessment of access to restricted website areas.
- Retrieval and password-protection assessment of the three assigned PDF reports.
- Examination of exposed database material and document metadata.
- Documentation of vulnerabilities and remediation recommendations.

### 3.2 Rules of Engagement

The assessment followed the restrictions specified in the project brief:

1. Testing was limited to the authorized target domain.
2. Social engineering was not permitted.
3. Denial-of-service testing was not permitted.
4. Testing outside the agreed scope was not permitted.
5. Activities were conducted for the authorized educational exercise.

> **Authorization notice:** The project brief states that written authorization was granted for the assessment. These techniques must never be used against systems without explicit permission from their owners.

---

# 4. Methodology

The project followed a structured penetration testing workflow.

| Phase | Activity | Purpose |
|---|---|---|
| 01 | Preparation | Prepare Kali Linux and the required security tools. |
| 02 | Reconnaissance | Gather domain, DNS, HTTP and website information. |
| 03 | Enumeration | Discover accessible directories, login pages and network services. |
| 04 | Initial Access | Investigate authentication and access-control weaknesses. |
| 05 | Data Retrieval | Retrieve and identify the three assigned PDF files. |
| 06 | Password Assessment | Extract PDF hashes and assess password protection. |
| 07 | Data Analysis | Examine the exposed database material and PDF metadata. |
| 08 | Reporting | Organize evidence, assess risks and recommend remediation. |

---

# 5. Tools and Technologies Used

The following tools were used during the practical assessment.

| Tool | Purpose |
|---|---|
| Kali Linux | Main penetration testing environment |
| WHOIS | Domain registration information |
| `dig` | DNS record investigation |
| `nslookup` | Domain name resolution |
| DNSRecon | DNS enumeration |
| cURL | HTTP requests, response headers and file retrieval |
| Gobuster | Directory and resource discovery |
| Nmap | Network service and port discovery |
| OpenSSL | TLS certificate and connection inspection |
| Firefox | Browser-based application assessment |
| John the Ripper | PDF password-recovery exercise |
| QPDF | PDF encryption and document checks |
| ExifTool | Document metadata inspection |
| `file` | File-type identification |
| `md5sum` | File integrity comparison |
| `csvlook` | Structured data review |

---

# 6. Milestone 1 — Initial Access

<details>
<summary><strong>M1: Website assessment and retrieval of three PDF lab reports</strong></summary>

### Objective

Investigate the target website, identify exposed entry points, examine authentication behaviour and retrieve the three PDF lab reports specified in the assignment.

### Activities Performed

**1. Reconnaissance**

Collected domain registration, DNS, HTTP, TLS and website technology information.

**2. Directory and resource discovery**

Used web enumeration techniques to identify accessible paths and investigate the patient and staff areas.

**3. Authentication assessment**

Examined the login workflow and investigated how the application handled specially crafted user input.

**4. Restricted-area access**

The lab assessment identified an authentication weakness that allowed access to the patient portal.

**5. PDF retrieval**

Retrieved the three PDF files made available through the portal and verified their file types and integrity information.

### Main Observations

- The website exposed several discoverable application paths.
- The patient portal contained an authentication weakness.
- Access to the portal exposed links to three PDF reports.
- A legacy database backup was also found in a publicly accessible directory.

### Evidence

| Screenshot | Description |
|---|---|
| `01-whois-reconnaissance.png` | Domain reconnaissance |
| `02a-dns-basic-records.png` | Basic DNS records |
| `02b-dns-mail-and-text-records.png` | Mail and TXT records |
| `02c-dns-enumeration.png` | DNS enumeration |
| `02d-dns-enumeration.png` | DNS enumeration continuation |
| `03-whois-key-details.png` | WHOIS details |
| `04-http-headers.png` | HTTP response headers |
| `05-html-metadata.png` | Website metadata |
| `06a-gobuster-scan.png` | Directory enumeration |
| `06b-directory-discovery-summary.png` | Discovered directories |
| `07-login-forms-reconnaissance.png` | Login form inspection |
| `08-tls-and-http-security-analysis.png` | TLS and HTTP security analysis |
| `09-nmap-service-discovery.png` | External service discovery |
| `10-sql-injection-error.png` | SQL error evidence |
| `11-portal-pdfs-browser-view.png` | Patient portal evidence |
| `12-portal-pdfs-curl-output.png` | Portal response evidence |
| `13-kali-downloaded-pdfs.png` | Retrieved PDF identification |
| `14-exposed-backup-directory.png` | Exposed legacy directory |
| `15-downloaded-database-backup.png` | Database backup identification |

**Milestone 1 result:** The three assigned PDF files were retrieved, and an exposed legacy database backup was identified.

</details>

---

# 7. Milestone 2 — Data Extraction

<details>
<summary><strong>M2: Password assessment of the three retrieved PDF files</strong></summary>

### Objective

Analyse the encryption applied to all three retrieved PDF files and recover access to their contents using appropriate password-assessment tools.

### Activities Performed

1. Identified and verified the three PDF files.
2. Examined their encryption characteristics.
3. Extracted the password hashes required for the recovery exercise.
4. Used John the Ripper and appropriate password-recovery techniques.
5. Verified successful access to the recovered PDF documents.

### Tools Used

- `file`
- QPDF
- John the Ripper
- PDF hash-extraction utilities

### Evidence

| Screenshot | Description |
|---|---|
| `16-pdf-file-identification.png` | Identification of PDF files |
| `17-pdf-report1-hash-extraction.png` | PDF hash extraction |
| `18-pdf-report1-password-cracking.png` | Report 1 password-recovery evidence |
| `19-pdf-report2-password-cracking.png` | Report 2 password-recovery evidence |
| `20-pdf-report3-password-cracking.png` | Report 3 password-recovery evidence |
| `21-pdf-report1-decryption-content-verification.png` | Report 1 access verification |
| `22-pdf-report2-decryption-content-verification.png` | Report 2 access verification |
| `23-pdf-report3-decryption-content-verification.png` | Report 3 access verification |

**Milestone 2 result:** Password recovery was successfully demonstrated for all three assigned PDF files, and access to their contents was verified.

</details>

---

# 8. Milestone 3 — Attack (Cracking) and Data Analysis

<details>
<summary><strong>M3: Identification of staff salaries, shareholder details and further exposure</strong></summary>

### Objective

Analyse the retrieved material and investigate the further exposure described in the assignment.

The specific tasks were:

- Find the salaries of all hospital employees.
- Find the shareholder details of the hospital.
- Examine file properties and metadata for evidence of further exposure.

### Activities Performed

**1. Database examination**

Inspected the exposed SQL backup and identified the relevant staff and shareholder database structures.

**2. Staff salary analysis**

Reviewed the staff records and extracted the employee salary information required by the assignment.

**3. Shareholder analysis**

Reviewed the shareholder records and identified the associated shareholder information.

**4. Document metadata inspection**

Used ExifTool to examine the properties of the recovered PDF documents.

**5. Further exposure discovery**

Identified an internal metadata comment referring to a database backup location, together with an author field.

### Evidence

| Screenshot | Description |
|---|---|
| `24-m3-staff-salaries-extracted.png` | Staff salary data analysis |
| `25-m3-shareholders-extracted.png` | Shareholder data analysis |
| `26-m3-further-exposure-discovered.png` | Further exposure identified through PDF metadata |

**Milestone 3 result:** The required staff and shareholder information was identified in the exposed database material. PDF metadata inspection also revealed additional internal information.

> **Confidentiality:** Actual patient, employee and shareholder records are not reproduced in this README. Evidence containing identifiable or confidential information must be reviewed and appropriately redacted before any repository is made public.

</details>

---

# 9. Milestone 4 — Penetration Testing Report

The final milestone requires a detailed professional penetration testing report submitted to the instructor.

The report follows the five sections specified in the Week 4 project brief.

| Section | Required Content |
|---|---|
| 01 — Executive Summary | Concise overview of the engagement, key findings and overall risk to the client. |
| 02 — Scope and Methodology | Target, tools used, approach taken and limitations encountered. |
| 03 — Findings and Proof of Exploitation | Each vulnerability, with screenshots and evidence for every milestone. |
| 04 — Risk Rating | Critical, High, Medium or Low ratings with justification. |
| 05 — Recommendations and Remediation | Actionable steps the client should take to fix each identified issue. |

### Main Security Issues Documented

| Finding | Preliminary Risk Rating | Security Impact |
|---|---|---|
| SQL injection and authentication bypass | Critical | Potential unauthorized access to the patient portal |
| Publicly accessible database backup | Critical | Exposure of internal staff and shareholder information |
| Weak PDF password protection | High | Recovery of access to protected PDF documents |
| Internal information disclosed through PDF metadata | Medium | Disclosure of internal comments and author information |

*These are assessment ratings based on the observed lab evidence, not formal CVSS scores.*

### Remediation Priorities

- Use parameterized SQL queries and prepared statements.
- Remove database backups from publicly accessible directories.
- Enforce authentication and authorization on every sensitive file-download request.
- Apply strong document-protection controls.
- Sanitize document metadata before external distribution.
- Review access logs and investigate possible unauthorized access.
- Conduct a security retest after remediation.

---

# 10. Evidence and Screenshots

All practical screenshots are organized in the `screenshots/` directory.

```text
NetworkWalks-B084-Week-4-Mediroza-Penetration-Test/
│
├── README.md
│
└── screenshots/
    │
    ├── 00a-tool-inventory-network-dns.png
    ├── 00b-tool-inventory-web-enumeration.png
    ├── 00c-tool-inventory-security-analysis.png
    │
    ├── 01-whois-reconnaissance.png
    ├── 02a-dns-basic-records.png
    ├── 02b-dns-mail-and-text-records.png
    ├── 02c-dns-enumeration.png
    ├── 02d-dns-enumeration.png
    ├── 03-whois-key-details.png
    ├── 04-http-headers.png
    ├── 05-html-metadata.png
    ├── 06a-gobuster-scan.png
    ├── 06b-directory-discovery-summary.png
    ├── 07-login-forms-reconnaissance.png
    ├── 08-tls-and-http-security-analysis.png
    ├── 09-nmap-service-discovery.png
    │
    ├── 10-sql-injection-error.png
    ├── 11-portal-pdfs-browser-view.png
    ├── 12-portal-pdfs-curl-output.png
    ├── 13-kali-downloaded-pdfs.png
    ├── 14-exposed-backup-directory.png
    ├── 15-downloaded-database-backup.png
    │
    ├── 16-pdf-file-identification.png
    ├── 17-pdf-report1-hash-extraction.png
    ├── 18-pdf-report1-password-cracking.png
    ├── 19-pdf-report2-password-cracking.png
    ├── 20-pdf-report3-password-cracking.png
    ├── 21-pdf-report1-decryption-content-verification.png
    ├── 22-pdf-report2-decryption-content-verification.png
    ├── 23-pdf-report3-decryption-content-verification.png
    │
    ├── 24-m3-staff-salaries-extracted.png
    ├── 25-m3-shareholders-extracted.png
    └── 26-m3-further-exposure-discovered.png
```

---

# 11. Learning Outcomes

Through this project, I gained practical experience in:

- Performing website reconnaissance and DNS enumeration.
- Identifying exposed directories and web application entry points.
- Understanding authentication and SQL injection weaknesses.
- Investigating access to restricted application resources.
- Identifying and assessing PDF encryption.
- Using password-recovery tools in an authorized lab.
- Examining database structures and analysing extracted information.
- Inspecting document metadata for unintended information disclosure.
- Organizing technical evidence and preparing a structured penetration testing report.
- Understanding the importance of confidentiality when handling sensitive information.

---

# 12. Legal and Ethical Disclaimer

This repository documents work completed as part of the NetworkWalks Cybersecurity Internship and its authorized educational penetration testing exercise.

The target and activities described here are limited to the scope specified in the project brief.

All security testing must be conducted only with explicit authorization from the system owner. Unauthorized access, data extraction, password attacks or other security testing against third-party systems may violate applicable laws.

Sensitive information, credentials, session tokens and confidential records must not be disclosed or shared without permission.

---

<div align="center">

## NETWORKWALKS CYBERSECURITY INTERNSHIP

**WEEK 4 — MEDIROZA GENERAL HOSPITAL PENETRATION TESTING**

**Prepared by: Mutsiirwa Matembera Josué**

**Batch B084**

[GitHub](https://github.com/josuemutsiirwa) • [LinkedIn](https://www.linkedin.com/in/josue-matembera-37a269407/)

*Learn. Practise. Secure.*

</div>
