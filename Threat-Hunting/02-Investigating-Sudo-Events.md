# Investigating Sudo Events

## Objective

The goal of this exercise was to investigate a sudo event detected by Wazuh and verify that privileged commands executed on the monitored endpoint were successfully logged.

---

## Lab Environment

- Wazuh Manager: Ubuntu Server
- Wazuh Agent: Ubuntu Server
- IDS: Suricata
- Dashboard: Wazuh Dashboard

---

## Generating the Event

To create a sudo event, I ran a command with elevated privileges on the monitored endpoint.

```bash
sudo apt update
```

Wazuh detected the activity and generated a security event.

---

## Investigation

In the Wazuh Dashboard, I searched for:

```
Successful sudo to ROOT executed.
```

I opened the alert and reviewed the event details.

The alert confirmed:

- The monitored endpoint generated the event.
- A command was executed using sudo.
- Wazuh successfully logged the activity.
- The timestamp matched the time the command was executed.

---

## Evidence

### Screenshot 1

**Sudo event detected in the Wazuh Dashboard**

<img width="1440" height="900" alt="Screenshot 2026-08-05 at 10 11 04" src="https://github.com/user-attachments/assets/be0bcf31-4a4f-44aa-ac09-89db7c5eebe0" />


---

### Screenshot 2

<img width="1440" height="900" alt="Screenshot 2026-08-05 at 10 13 17" src="https://github.com/user-attachments/assets/57c4bdab-436f-43ab-bbb2-aa00790c86ad" />

<img width="1440" height="900" alt="Screenshot 2026-08-05 at 10 13 26" src="https://github.com/user-attachments/assets/512dac35-120e-4ef2-b7dc-9191803ca51b" />



---

## Result

The investigation confirmed that Wazuh successfully detected and recorded privileged activity performed with sudo. This demonstrates that administrative actions on the monitored endpoint can be tracked and reviewed from the Wazuh Dashboard.
