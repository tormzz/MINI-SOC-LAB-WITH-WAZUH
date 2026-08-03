# Installing Ubuntu 24.04

## Objective

To prepare an Ubuntu virtual machine that will host the SOC home lab.

---

## Environment

- Host OS: macOS
- Hypervisor: UTM
- Guest OS: Ubuntu Server 24.04

---

## Installation

1. Downloaded Ubuntu Server 24.04 ISO.
2. Created a new virtual machine in UTM.
3. Allocated RAM and CPU.
4. Installed Ubuntu.
5. Updated packages.

```bash
sudo apt update
sudo apt upgrade -y
