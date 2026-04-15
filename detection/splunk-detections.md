## Detection Strategy

```spl
# Injection Detection
index=main ("OR 1=1" OR "admin")

# Authentication Monitoring
index=main login OR password

# Traffic Analysis
index=main | stats count by host
