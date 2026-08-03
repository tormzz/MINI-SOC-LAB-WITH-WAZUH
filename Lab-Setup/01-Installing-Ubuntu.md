# Installing Ubuntu 26.04

## Objective

To prepare an Ubuntu virtual machine that will host the SOC home lab.

---

## Environment

- Host OS: macOS
- Hypervisor: UTM
- Guest OS: Ubuntu Server 26.04

---

## Installation

1. Downloaded Ubuntu Server 26.04 ISO.
2. Created a new virtual machine in UTM.
3. Allocated RAM and CPU.
4. Installed Ubuntu.
5. Updated packages.

```bash
sudo apt update
sudo apt upgrade -y
```

## Verification

Verified internet connectivity.

```bash
ping google.com
```

Result: The VM successfully connected to the internet.

<img width="1440" height="900" alt="Screenshot 2026-08-03 at 19 32 48" src="https://github.com/user-attachments/assets/81f1a503-7449-467c-87cb-2ae895a160eb" />

