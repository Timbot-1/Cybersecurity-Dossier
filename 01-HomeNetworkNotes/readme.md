# Incident Investigation Summary: [Incident Name / Ticket ID]

**Date of Report:** November 5, 2026  
**Lead Investigator:** [Your Name/Title]  
**Severity Level:** [Critical / High / Medium / Low]  
**Status:** [Contained / Resolved / Under Investigation]  

---

## 🚨 Executive Summary
Provide a brief, non-technical overview of the incident. State exactly what happened, the systems affected, whether data was compromised, and the current operational status in 3–4 sentences.

## 🕒 Incident Timeline
A chronological breakdown of the event. Use a table to map out key milestones from initial entry to resolution.

| Timestamp (UTC) | Phase | Event Description & Evidence |
| :--- | :--- | :--- |
| YYYY-MM-DD HH:MM | **Detection** | Initial alert triggered by [SIEM/EDR tool] indicating [anomaly]. |
| YYYY-MM-DD HH:MM | **Analysis** | Confirmed unauthorized access via [compromised credentials/vulnerability]. |
| YYYY-MM-DD HH:MM | **Containment** | Affected host `[Hostname/IP]` isolated from the network. |
| YYYY-MM-DD HH:MM | **Eradication** | Malicious artifacts, accounts, and web shells removed. |
| YYYY-MM-DD HH:MM | **Recovery** | System restored from verified backup; credentials rotated. |

## 🔍 Technical Analysis & Findings
Detail how the incident occurred and what the adversary did while inside the environment.

* **Root Cause / Vector:** Identify how the attacker gained initial entry (e.g., phishing link, unpatched public-facing server, VPN credential stuffing).
* **Indicators of Compromise (IoCs):** 
  * **IP Addresses:** `192.0.2.1` (Attacker C2)
  * **File Hashes (SHA-256):** `e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855`
  * **Malicious Accounts:** `domain\test_admin`
* **Impacted Assets:** List servers, databases, endpoints, or user accounts compromised during the incident.

## 💾 Data & Privacy Impact
* **Exfiltration Status:** [Confirmed / Suspected / None Profiled]
* **Data Types Involved:** (e.g., Personally Identifiable Information (PII), proprietary source code, internal emails).
* **Regulatory Trigger:** State if this breach requires legal notification (e.g., GDPR, CCPA, HIPAA).

## 🛡️ Remediation & Preventative Actions
Actionable steps taken or planned to ensure this specific vulnerability cannot be exploited again.

### Completed Actions
- [x] Isolated compromised endpoints from the production VLAN.
- [x] Forced a global password reset for all affected domain accounts.
- [x] Blocked known malicious IP addresses at the perimeter firewall.

### Planned Long-Term Actions
- [ ] Implement Multi-Factor Authentication (MFA) across all external access vectors.
- [ ] Schedule an external vulnerability scan and penetration test for the affected subnet.
- [ ] Update SIEM correlation rules to flag anomalous lateral movement patterns.

