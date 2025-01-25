# Phishing Email Defensive Measures

This repository serves as a continuation of the project `Phishing Email Analysis and Defensive Measures`. The focus here is to implement and document defensive measures to mitigate phishing attacks, utilizing real-world examples and analysis.

## Key Sections

### 1. Defensive Measures Taken
This section elaborates on the actions performed to block malicious artifacts observed during phishing analysis. Defensive measures include:
- **Email Artifact Blocking:** Subject lines, sending addresses, and server IPs.
- **Web Artifact Blocking:** URLs, domains, and IPs.
- **File Artifact Blocking:** File names and hashes.

### 2. Phishing Analysis Demo
Includes demonstrations of phishing attacks, the observed artifacts, and the appropriate defensive measures taken to neutralize the threat.

---

## Example: Defensive Measures in Action

### Scenario: DHL Credential Harvester
**Details:**
- Sender: `contact@dhl.com`
- Sending Server IP: `209.85.167.42`
- Reverse DNS: `mail-lf1-f42.google.com`
- Subject: `Failed Delivery DHL RESPOND NOW – URGENT!!`
- URL: `hxxps://dhl-faileddelivery.shanepppalkkbc.com`

### Report Section:

1. **Email Analysis:**
    - The sending address (`contact@dhl.com`) was spoofed.
    - The sending server IP (`209.85.167.42`) belongs to Gmail, indicating a legitimate platform used maliciously.

2. **Actions Taken:**
    - **Blocked Subject Line:**
      - Action: Blocked the subject line `Failed Delivery DHL RESPOND NOW – URGENT!!` on the email gateway.
      - Justification: Highly unlikely for legitimate DHL emails to use this subject line. No negative business impact.
      - Timestamp: `22nd December, 12:03 PM`
    
    - **Blocked Domain:**
      - Action: Blocked the domain `shanepppalkkbc[.]com` via web proxy.
      - Justification: Domain was created for malicious purposes. Blocking prevents access to all links hosted on this domain.
      - Timestamp: `22nd December, 12:07 PM`

### Recap:
- Summarized phishing email attributes and their analysis.
- Justified the measures taken to ensure no adverse effects on business operations.
- Documented actions, timestamps, and accountability clearly.

---

## Structure of the Repository
1. **`DefensiveMeasures.md`:**
   - Comprehensive documentation of defensive measures implemented.
   
2. **`PhishingScenarios/`:**
   - Contains examples and demos of phishing emails analyzed and corresponding actions taken.

3. **`Scripts/`:**
   - Scripts to automate the analysis and blocking of artifacts.

4. **`Reports/`:**
   - Sample reports showcasing defensive measures and justifications.

---

## Contributions
Contributions are welcome to expand on defensive measures, analysis tools, or examples. Please submit a pull request with your proposed additions.

---

## License
This project is licensed under the MIT License. See `LICENSE` for more information.
