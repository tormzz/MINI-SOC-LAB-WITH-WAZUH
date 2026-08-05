# Investigating PAM Authentication Events

## Objective

The purpose of this exercise was to investigate user authentication events recorded by Wazuh and verify that login and logout activities were successfully monitored.

---

## Lab Environment

- Wazuh Manager: Ubuntu Server
- Wazuh Agent: Ubuntu Server
- Dashboard: Wazuh Dashboard

---

## Generating the Event

To generate PAM events, I logged into the monitored Ubuntu system and then logged out.

This created authentication events that were forwarded to the Wazuh Manager.

---

## Investigation

In the Wazuh Dashboard, I searched for PAM authentication events.

I observed the following alerts:

- PAM: Login session opened
- PAM: Login session closed

I opened the event details to confirm the alert information.

The event showed:

- The monitored endpoint
- The time the session started or ended
- The user session information
- The corresponding Wazuh rule

---

## Evidence

### Screenshot 1

**PAM login and logout events in the Wazuh Dashboard**

<img width="1440" height="900" alt="Screenshot 2026-08-05 at 10 21 05" src="https://github.com/user-attachments/assets/8bfba15a-dc77-44fb-96ed-1214053d5aef" />


---

### Screenshot 2

**Document Details for the PAM event**

<img width="1440" height="900" alt="Screenshot 2026-08-05 at 10 22 06" src="https://github.com/user-attachments/assets/ba2dc2c2-7922-4912-95e1-f58754c2d215" />

<img width="1440" height="900" alt="Screenshot 2026-08-05 at 10 22 13" src="https://github.com/user-attachments/assets/170dda7f-b2b3-4e86-a0bd-403e5d868392" />

---

## Result

The investigation confirmed that Wazuh successfully recorded authentication activity on the monitored endpoint. Login and logout events were visible in the dashboard and could be investigated through the event details.
