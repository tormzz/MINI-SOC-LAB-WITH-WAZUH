# Generating Test Alerts

## Objective

The purpose of this exercise was to confirm that events generated on the monitored endpoint were successfully detected by Suricata, forwarded by the Wazuh agent, and displayed in the Wazuh dashboard.

---

## Test Environment

- Wazuh Manager: Ubuntu Server 26.04
- Wazuh Agent: Ubuntu Server 26.04
- IDS: Suricata
- Dashboard: Wazuh Dashboard

---

## Steps Performed

I generated activity on the monitored endpoint to verify that the logging pipeline was functioning correctly.

The activity included:

- Logging into the Ubuntu system
- Running commands with `sudo`
- Generating network traffic monitored by Suricata

These events were forwarded to the Wazuh manager and processed successfully.

---

## Verification

I confirmed that the alerts appeared in the Wazuh Dashboard.

The dashboard displayed alerts including:

- Suricata alerts
- PAM login events
- Successful sudo events

This confirmed that communication between the agent and manager was working correctly.

---

## Evidence

### Figure 1 – Generating a sudo event

<img width="1440" height="900" alt="Screenshot 2026-08-04 at 15 25 58" src="https://github.com/user-attachments/assets/6bf6bcfc-8010-45db-9d8f-f96b8c53b7b5" />


*Executed a privileged command on the monitored endpoint to generate a sudo security event.*

---

### Figure 2 – Generating authentication event

<img width="1440" height="900" alt="Screenshot 2026-08-04 at 15 34 50" src="https://github.com/user-attachments/assets/7eb4145b-ce27-4b7c-bbaf-0d8590495da0" />


*Logged out and back into the monitored endpoint to generate PAM authentication events.*

---

### Figure 3 – Wazuh Dashboard

<img width="1440" height="900" alt="Screenshot 2026-08-04 at 15 40 24" src="https://github.com/user-attachments/assets/a39c1b73-5da1-4c9f-b2de-0ae36881359b" />


*Wazuh Dashboard displaying the generated security events received from the monitored endpoint.*

---

### Figure 4 – Alert Details

<img width="1440" height="900" alt="Screenshot 2026-08-04 at 15 47 27" src="https://github.com/user-attachments/assets/506dd5fd-52c8-476b-b966-15c7e4bf5438" />


*Document Details showing the generated sudo event, rule information, severity level, and MITRE ATT&CK mapping.*



---

## Result

The alert generation process was successful and the events were visible in the Wazuh Dashboard.
