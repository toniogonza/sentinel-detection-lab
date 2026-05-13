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
|---|---|---|
| Brute Force RDP — Multiple Failed Logons | T1110.001 — Password Guessing | ✅ Live |
| Suspicious Local Admin Account Creation | T1136.001 — Create Local Account | 🔄 In Progress |
| Azure AD Sign-In Anomaly Detection | T1078.004 — Cloud Accounts | 🔄 In Progress |

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
