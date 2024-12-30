# Lateral Movement Detection
**Use Case:** Identifies potential lateral movement by monitoring new administrative shares.

**Query:**
```splunk
index=wineventlog EventCode=5145 
| stats count by Account_Name, Computer_Name, Share_Name
| where count > 5
