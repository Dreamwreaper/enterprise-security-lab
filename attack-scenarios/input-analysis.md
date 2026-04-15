
# Input Handling Analysis

## Objective
Evaluate how the application processes user-supplied input and identify potential security risks.

## Test Performed
Injected input into the search field:

' OR 1=1 -- admin

## Observation
The application returned no results, indicating that input was handled without exposing data. However, the payload was successfully transmitted to the backend.

## Security Insight
Even when injection attempts do not succeed, they generate identifiable patterns in HTTP traffic that can be monitored and analyzed.

## Detection Perspective
This type of input can be detected in a SIEM by identifying:
- SQL injection patterns (e.g., OR 1=1)
- Special characters and malformed queries
- Repeated abnormal input attempts

## Recommendation
- Implement strict server-side input validation
- Log all user input activity
- Monitor for known injection patterns
- Alert on repeated suspicious behavior

## Tools Used
- Burp Suite (traffic capture)
- Splunk (log analysis)
