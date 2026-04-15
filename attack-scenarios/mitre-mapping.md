# MITRE ATT&CK Mapping

## Overview
This lab simulates web application activity and maps observed behaviors to the MITRE ATT&CK framework to align detection with known adversary techniques.

---

## Technique Mapping

### Tactic: Initial Access
**Technique: T1190 – Exploit Public-Facing Application**

- Application: OWASP Juice Shop
- Activity: Injection testing via search input
- Example Input:
  ' OR 1=1 -- admin

**Description:**
Attackers attempt to exploit vulnerabilities in web applications exposed to the internet.

---

### Tactic: Credential Access
**Technique: T1110 – Brute Force**

- Activity: Repeated login attempts
- Detection Method:
  Splunk query monitoring login behavior

**Description:**
Adversaries attempt to gain access by trying multiple credential combinations.

---

### Tactic: Discovery
**Technique: T1046 – Network Service Discovery**

- Activity: Application exploration and navigation
- Behavior:
  Browsing endpoints and testing functionality

---

## Detection Strategy

### Injection Detection
```spl
index=main ("OR 1=1" OR "admin")

### Authentication Monitoring
index=main login OR password

### Traffic Analysis
index=main | stats count by host
