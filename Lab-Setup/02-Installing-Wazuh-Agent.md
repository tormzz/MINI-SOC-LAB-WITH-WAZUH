# Installing Wazuh Agent

## Objective

Install and configure the Wazuh agent on the Ubuntu virtual machine so it can communicate with the Wazuh Manager.

---

## Environment

- Ubuntu Server 26.04
- Wazuh Agent 4.14.6
- Wazuh Manager IP: 192.168.64.3

---

## Installation

1. Downloaded and installed the Wazuh agent.
2. Configured the Wazuh Manager IP address in the agent configuration file.
3. Enabled the Wazuh agent service.
4. Started the Wazuh agent.

```bash
sudo systemctl enable wazuh-agent
sudo systemctl start wazuh-agent
```

---

## Verification

Verified that the Wazuh agent service was running successfully.

```bash
sudo systemctl status wazuh-agent
```

**Result:** The Wazuh agent was active (running) and successfully connected to the Wazuh Manager.

---

## Screenshot

<img width="1440" height="900" alt="Screenshot 2026-08-03 at 19 42 19" src="https://github.com/user-attachments/assets/79589016-698c-46d7-a750-de52c637a07d" />
<img width="1440" height="900" alt="Screenshot 2026-08-03 at 20 17 07" src="https://github.com/user-attachments/assets/f71f2b94-0708-402e-9b67-41224b098c94" />
