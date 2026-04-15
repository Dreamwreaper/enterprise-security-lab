
# Enterprise Web Application Security Lab Report

## Executive Summary
This project demonstrates a hands-on approach to web application security testing and detection using OWASP Juice Shop, Burp Suite, and Splunk.

The objective was to simulate real-world attack scenarios, capture HTTP traffic, and develop detection strategies using SIEM tools.

---

## Methodology
1. Deployed OWASP Juice Shop locally using Docker
2. Generated web traffic and simulated attack scenarios
3. Captured HTTP requests using Burp Suite
4. Exported traffic logs and ingested them into Splunk
5. Developed detection queries to identify suspicious activity

---

## Key Findings

### Input Handling
Injection patterns were successfully transmitted through the application, demonstrating how malicious input appears in traffic logs.

### Authentication
Login activity can be monitored to detect abnormal authentication patterns and potential credential abuse.

### Access Control
Application behavior highlights the importance of enforcing proper authorization mechanisms.

---

## SIEM Detection (Splunk)

Splunk was used to analyze ingested traffic and identify suspicious patterns.

### Example Detection Queries

Injection Detection:
```spl
index=main ("OR 1=1" OR "admin")
