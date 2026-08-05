# Detecting Nmap Scan

## Objective

The objective of this exercise was to generate network activity using Nmap and investigate how Suricata and Wazuh detected the scan.

---

## Test Environment

- Wazuh Manager: Ubuntu Server
- Wazuh Agent: Ubuntu
- Suricata IDS
- Wazuh Dashboard

---

## Scan Performed

I ran the following command against my monitored machine.

```bash
sudo nmap -sS -A 192.168.64.3
```

---

## Detection

After running the scan, I refreshed the Wazuh Dashboard.

Suricata generated multiple alerts, including:

- ET SCAN Possible Nmap User-Agent Observed

The alerts were successfully forwarded to Wazuh by the installed agent.

---

## Investigation

I opened one of the Suricata alerts in the Wazuh dashboard to review the event.

The alert showed **"ET SCAN Possible Nmap User-Agent Observed"**, confirming that Suricata detected the Nmap scan I performed during testing.

The event also included details such as the monitored agent, timestamp, alert level, and rule information.

This confirmed that the network scan was successfully detected by Suricata and forwarded to Wazuh for investigation.


---

## Evidence

### Nmap scan command

<img width="1440" height="900" alt="Screenshot 2026-08-05 at 01 51 51" src="https://github.com/user-attachments/assets/edaa8eab-f50a-410d-ac9b-5bfa6af3e340" />

<img width="1440" height="900" alt="Screenshot 2026-08-05 at 01 52 15" src="https://github.com/user-attachments/assets/b9dc4bb4-5fbc-4a3b-ab53-5c6b8b2e5359" />
---

### Wazuh alert generated

<img width="1440" height="900" alt="Screenshot 2026-08-05 at 01 55 14" src="https://github.com/user-attachments/assets/e9d6e39c-2f23-4375-a05d-a914ba452c34" />


---

### Alert investigation

<img width="1440" height="900" alt="Screenshot 2026-08-05 at 02 01 25" src="https://github.com/user-attachments/assets/e5564fce-c9ef-4232-92c2-20a1dba6fa27" />

<img width="1440" height="900" alt="Screenshot 2026-08-05 at 02 01 53" src="https://github.com/user-attachments/assets/8c30baaa-bd37-458f-bfed-0c553f4471bf" />
---

## Result

The Nmap scan generated network traffic that was detected by Suricata and successfully forwarded to Wazuh for analysis.

This demonstrates how network activity can be monitored, collected and investigated using a SIEM platform.
