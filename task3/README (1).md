# Task 3: Perform a Basic Vulnerability Scan on Your PC

## Objective
Use free tools to identify common vulnerabilities on your computer and understand their impact and mitigations.

## Tools
- OpenVAS Community Edition (GVM)
- Nessus Essentials

## Steps to Perform

### 1. Install Vulnerability Scanner

**OpenVAS (GVM):**
```bash
sudo apt update
sudo apt install openvas
sudo gvm-setup
sudo gvm-check-setup
```
Fix any setup errors until the installation is complete.

**Nessus Essentials:**

- Download the Debian package from [Tenable Website](https://www.tenable.com/products/nessus/nessus-essentials)

- Install and start Nessus:
```bash
sudo dpkg -i Nessus-*.deb
sudo systemctl start nessusd
```

- Access the Nessus Web GUI at `https://localhost:8834`

### 2. Setup the Scan
- Open the scanner dashboard (OpenVAS or Nessus).
- Create a new scan.
- Set the target as your local machine IP or `127.0.0.1`.
- Choose a full or basic system/network scan.

### 3. Run the Scan
- Start the scan.
- Wait for the scan to complete (may take 30-60 minutes).

### 4. Review Results
- View the report.
- Focus on vulnerabilities categorized by severity: Critical, High, Medium, Low.

### 5. Analyze & Document
- Identify critical vulnerabilities.
- Note vulnerability name, CVSS score, affected service, and suggested fixes.

### 6. Research Mitigations
- Look up CVE or plugin IDs for patches or configuration fixes.

### 7. Take Screenshots
- Capture dashboard, vulnerability summaries, and critical findings.

### 8. Export Report
- Save the full report in PDF or HTML format.

## Deliverables
- Vulnerability scan report.
- Screenshots of scan and results.
- Summary of critical vulnerabilities and mitigations.

## Outcome
- Basic experience with vulnerability scanning.
- Understanding of common PC security risks.
- Knowledge of how to remediate vulnerabilities.
