Task 3: Vulnerability Scan on Local Machine

Objective

Perform a vulnerability scan on the local system using Nessus Essentials, identify possible vulnerabilities, and interpret the results.

---

Tools Used

- Nessus Essentials by Tenable (Free vulnerability scanner)

- Localhost (127.0.0.1 or machine IP: `10.223.131.99`) as target

- Web browser to access Nessus UI at `https://localhost:8834`

---

Scan Details

- Scanner Name: Nessus Essentials

- Target IP: 10.223.131.99

- Operating System Detected: Windows 10 (10.0.19041)

- Scan Duration: ~16 minutes

- Scan Profile: Basic Network Scan

---

 Vulnerabilities Found

1. SMB Signing Not Required (Medium)

- Port: TCP 445 (SMB/CIFS)

- Risk: Allows man-in-the-middle attacks

- Fix: Enforce message signing in group policies (`Microsoft network server: Digitally sign communications (always)`)

---

2. SSL Certificate Cannot Be Trusted (Medium)

- Port: TCP 8834

- Risk: Self-signed certificate not trusted by browsers

- Fix: Replace with a certificate from a recognized CA

---

Informational Findings

- SMB Versions Supported (SMBv2 and SMBv3 detected)

- DCERPC Services exposed on various dynamic ports

- Multiple Open Ports: Including 135, 139, 445, 5040, 7680, 8834, and many UDP services

- Device Type: General-purpose Windows device

-Web Servers Detected:

  - NessusWWW on port 8834

  - Microsoft HTTPAPI on port 50128

---

Screenshots Included

- `scan_dashboard.png` – Running scan UI

- `vuln_summary.png` – Severity breakdown

- `smb_signing_vuln.png` – SMB signing vulnerability details

---

Files Included

- `scan_report.pdf` – Full exported report from Nessus

- `screenshots/` – Proof of findings and scan activity

- `README.md` – This summary and documentation

---

Conclusion

This scan revealed several medium-level vulnerabilities, including insecure SMB configuration and untrusted certificates. Fixing these can greatly improve system security. No critical or high vulnerabilities were detected.

