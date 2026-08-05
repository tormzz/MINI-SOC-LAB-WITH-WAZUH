# Investigating Alerts

## Objective

The goal of this task was to look at the alerts generated in Wazuh and understand what they mean. I wanted to see why the alert was triggered and determine whether it was normal activity or something suspicious.

---

## Test Environment

- Wazuh Manager: Ubuntu Server 26.04
- Wazuh Agent: Ubuntu Server 26.04
- IDS: Suricata
- Dashboard: Wazuh Dashboard

---

## Alert Investigated

For this exercise, I investigated the **Successful sudo to ROOT executed** alert.

This alert appeared after I ran a `sudo` command on the monitored endpoint.

---

## Investigation

I opened the alert in the Wazuh Dashboard to view more details.

The alert showed:

- Rule ID: 5402
- Rule Level: 3
- Agent: agentt
- Hostname: waazuhagent
- MITRE ATT&CK: T1548.003 (Sudo and Sudo Caching)

I also checked the timestamp and confirmed it matched the time I executed the `sudo` command.

---

## Findings

After reviewing the alert, I confirmed that it was expected. I had intentionally run `sudo apt update` during testing, so Wazuh correctly detected the activity and created an alert.

Since I was the one who performed the action, I concluded that this was normal administrative activity and not a security threat.

---

## Conclusion

This investigation helped me understand how Wazuh records and displays security events. It also showed me how to review an alert and decide whether it is expected or requires further investigation.

---

## Evidence

### Figure 1 – Threat Hunting page

<img width="1440" height="900" alt="Screenshot 2026-08-05 at 00 58 30" src="https://github.com/user-attachments/assets/17ecb632-1356-475d-a481-524b5c71a552" />

## Viewing the generated alerts

The Wazuh Threat Hunting dashboard displays the alerts generated during testing, including Suricata events, PAM login activity, and successful sudo executions.

### Figure 2 – Alert Details


<img width="1440" height="900" alt="Screenshot 2026-08-05 at 01 04 16" src="https://github.com/user-attachments/assets/9e147015-ab3c-470b-b2e8-9a321126cfb4" />


---
<img width="1440" height="900" alt="Screenshot 2026-08-05 at 01 04 24" src="https://github.com/user-attachments/assets/ea7f7071-b920-4737-a604-4abd8b5c009a" />

## Investigating a sudo event

Selecting an alert opens the document details, showing the event timestamp, rule description, rule ID, MITRE ATT&CK mapping, log source, and additional metadata used during investigation.
