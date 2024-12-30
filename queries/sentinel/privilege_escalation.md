# Privilege Escalation Detection
**Use Case:** Detects new administrative account creations.

**Query:**
```kql
SecurityEvent
| where EventID == 4720
| summarize count() by Account, Computer
