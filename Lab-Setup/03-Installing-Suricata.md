# Installing Suricata

## Objective

Install and configure Suricata on the Ubuntu virtual machine to monitor network traffic and generate security alerts.

---

## Environment

- Ubuntu Server 26.04
- Suricata IDS
- Wazuh Agent 4.14.6
1234
---

## Installation

1. Updated the system packages.
2. Installed Suricata.
3. Verified the installation.
4. Enabled the Suricata service.
5. Started the Suricata service.
6. Updated the Suricata rules.

```bash
sudo apt update
sudo apt install suricata -y
sudo systemctl enable suricata
sudo systemctl start suricata
sudo suricata-update
```

---

## Verification

Verified that the Suricata service was running successfully.

```bash
sudo systemctl status suricata
```

**Result:** The Suricata service was active (running), confirming that the installation was successful.

Verified the installed version.

```bash
suricata --build-info
```

**Result:** The installed version of Suricata and its build information were displayed successfully.

---

## Screenshot

<img width="1440" height="900" alt="Screenshot 2026-08-03 at 19 50 37" src="https://github.com/user-attachments/assets/3c57651d-539c-4b24-b5be-899c61afd73f" />


