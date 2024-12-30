# Data Exfiltration Detection
**Use Case:** Detects abnormal data transfers to external IPs.

**Query:**
```lucene
network.bytes > 10000000 AND destination.ip NOT IN ["10.0.0.0/8", "192.168.0.0/16"]
