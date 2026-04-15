
# Lab Setup Guide – Enterprise Security Lab

## Overview
This guide walks through how to recreate the web application security lab using OWASP Juice Shop, Burp Suite, and Splunk.

---

## Requirements

- Docker Desktop (WSL2 enabled)
- Splunk Enterprise (Free Trial)
- Burp Suite Community Edition
- Web browser (Chrome/Edge)

---

## Step 1 – Run OWASP Juice Shop

Run the following command:
docker run --rm -p 3000:3000 bkimminich/juice-shop

Open:
http://localhost:3000

---

## Step 2 – Generate Traffic

Perform the following actions:

- Browse the application
- Attempt logins
- Use search input: ' OR 1=1 -- admin
- - Navigate through pages

---

## Step 3 – Capture Traffic (Burp Suite)

1. Open Burp Suite
2. Go to Proxy → HTTP History
3. Configure browser proxy (127.0.0.1:8080)
4. Capture requests
5. Export traffic:
 - Right-click → Save items → XML

---

## Step 4 – Import into Splunk

1. Go to http://localhost:8000
2. Settings → Add Data → Upload
3. Upload exported Burp file
4. Set index = main
5. Start Searching

---

## Step 5 – Run Detection Queries

Example queries:
index=main

index=main ("OR 1=1" OR "admin")

index=main | stats count by host

---

## Outcome

This lab demonstrates:

- Web traffic analysis
- Attack simulation
- SIEM detection using Splunk
- Security monitoring techniques

---

## Disclaimer
This lab is for educational purposes only. Do not use these techniques against unauthorized systems.
