# Enterprise Web Application Security Lab

## Overview
This project demonstrates hands-on web application security testing, traffic analysis, and SIEM-based detection using a controlled lab environment.

The lab was built using OWASP Juice Shop, with traffic captured via Burp Suite and analyzed in Splunk to simulate real-world security monitoring.

---

## Objectives
- Deploy a vulnerable web application locally
- Capture and analyze HTTP traffic
- Identify suspicious patterns and behaviors
- Develop detection strategies using SIEM tools
- Map findings to security best practices

---

## Tools Used
- OWASP Juice Shop
- Burp Suite Community Edition
- Splunk Enterprise
- Docker / WSL2

---

## Lab Workflow
1. Deploy application locally  
2. Generate traffic and simulate attack scenarios  
3. Capture HTTP requests using Burp Suite  
4. Export logs and ingest into Splunk  
5. Develop detection queries  

---

## Key Scenario (Injection Test)

Test input:
' OR 1=1 -- admin

This demonstrates how malicious patterns appear in web traffic and how they can be detected in logs.

---

## SIEM Detection Example

```spl
index=main "' OR 1=1"

---

## Then scroll down and click:

👉 **Commit new file**

---

# ✅ AFTER THAT

You will now see:
👉 `README.md` on your repo homepage

---

# 🔥 NEXT STEP

After you create it, tell me:

👉 **“README created”**

Then we’ll:

- Build your folders (attack-scenarios, detection, etc.)
- Upload your screenshots
- Move into **Splunk ingestion (this is where you stand out HARD)**

You’re doing this exactly right—this is how you build real portfolio value.
---

## Disclaimer
This project was conducted in a controlled lab environment for educational purposes only. No unauthorized systems or data were targeted.
## Screenshots

### Splunk Detection
![Detection](screenshots/splunk-detection-results.png)

### Raw Logs
![Logs](screenshots/splunk-raw-logs.png)

### Traffic Analysis
![Traffic](screenshots/splunk-traffic-analysis.png)

```md
## MITRE ATT&CK Mapping

This project includes mapping of simulated attack activity to the MITRE ATT&CK framework to align detection strategies with real-world adversary techniques.
