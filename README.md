# Microsoft Sentinel Detection Lab
**Azure | KQL | MITRE ATT&CK | Real Attack Data**

A proof-of-concept Microsoft Sentinel SIEM detection lab built in Azure 
to demonstrate real-world threat detection and investigation capability.

## Lab Architecture
- Microsoft Sentinel on Log Analytics Workspace (sentinel-homelab-law)
- Windows Server 2022 VM as log source (sentinel-victim-vm)
- Windows Security Events via Azure Monitor Agent (AMA)
- Custom Scheduled Analytics Rules with MITRE ATT&CK mapping

## Detection Scenarios

| Scenario | MITRE Technique | Status |
|----------|----------------|--------|
| Brute Force RDP — Multiple Failed Logons | T1110.001 — Password Guessing | ✅ Live |
| Suspicious Local Admin Account Creation | T1136.001 — Create Local Account | ✅ Live |
| RDP Anomaly Detection | T1078.004 — Valid Accounts | ✅ Live |

## Evidence & Screenshots

### Scenario 1 — Brute Force RDP (T1110.001)
![Scenario 1](Scenario%201%20—%20Brute%20Force%20RDP%20(T1110.001).png)

### Scenario 2 — Local Admin Creation (T1136.001)
![Scenario 2](Scenario%202%20—%20Local%20Admin%20Creation%20(T1136.001).png)

### Scenario 3 — RDP Anomaly Detection (T1078.004)
![Scenario 3](Scenario%203%20—%20RDP%20Anomaly%20(T1078.004).png)

## Key Findings — Scenario 1
- Detected real brute force attack from IP 45.142.193.145 (Amsterdam, Netherlands)
- 29 failed logon attempts across 3 accounts in a 2-hour window
- Attacker infrastructure confirmed via AbuseIPDB — 405 reports, 100% abuse confidence
- Custom KQL analytics rule deployed and mapped to MITRE ATT&CK T1110.001
- Incident investigation documented following SOC Tier 1 triage methodology

## Tools Used
Microsoft Sentinel | KQL | Azure Monitor Agent | Log Analytics | 
MITRE ATT&CK | AbuseIPDB | Microsoft Defender XDR

## Certifications In Progress
- ISC² Certified in Cybersecurity (CC)
- SC-200: Microsoft Security Operations Analyst
