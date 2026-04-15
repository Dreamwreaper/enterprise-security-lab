
# Access Control Analysis

## Objective
Evaluate how the application enforces authorization and access restrictions.

## Observation
Application navigation and user functionality were tested to assess access control behavior.

## Risk
Improper access control can lead to:
- Unauthorized access to sensitive data
- Privilege escalation
- Exposure of restricted functionality

## RMF / NIST Mapping
- AC-2: Account Management
- AC-3: Access Enforcement

## Detection Perspective
Access control issues can be identified through:
- Unusual access patterns
- Requests to restricted endpoints
- Abnormal privilege usage

## Recommendation
- Enforce Role-Based Access Control (RBAC)
- Validate authorization on the server side
- Apply least privilege principles
- Monitor access patterns for anomalies

## Tools Used
- Burp Suite
- Splunk
