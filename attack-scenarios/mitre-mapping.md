# MITRE ATT&CK Mapping

## Overview
This lab simulates web application activity and maps observed behaviors to the MITRE ATT&CK framework to align detection with real-world adversary techniques.

---

## Technique Mapping

### T1190 – Exploit Public-Facing Application (Initial Access)

**Activity:**
Injection testing using OWASP Juice Shop

**Example Input:**
' OR 1=1 -- admin

**Description:**
Attackers attempt to exploit vulnerabilities in publicly accessible web applications.

**Evidence:**
![Injection](screenshots/mitre-t1190-injection.png)

---

### T1110 – Brute Force (Credential Access)

**Activity:**
Repeated login attempts and authentication-related traffic

**Detection Method:**
```spl
index=main login OR password
