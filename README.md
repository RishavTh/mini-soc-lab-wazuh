# 🛡️ Mini SOC Lab using Wazuh SIEM and Sysmon

This project demonstrates a **Mini Security Operations Center (SOC)** setup in a virtual environment using **Wazuh SIEM** on Ubuntu and **Sysmon** on Windows 10. It provides hands-on experience in threat detection, log analysis, custom rule creation, and attack simulation — ideal for cybersecurity learners and professionals.

---

## 📌 Project Overview

The goal of this lab is to build a basic SOC infrastructure to:

- Collect and analyze endpoint logs in real-time
- Detect suspicious activities and potential attacks
- Learn SIEM workflows and alerting mechanisms
- Simulate attack scenarios for detection validation

---

## 🧱 Lab Architecture

| VM Name       | OS                  | Role                                   |
|---------------|---------------------|--------------------------------------|
| `ubuntu-siem` | Ubuntu Desktop 22.04| Wazuh server (manager + dashboard)    |
| `win10-client`| Windows 10 Pro      | Endpoint with Sysmon + Wazuh agent    |

Network setup uses bridged mode with static IP assignments for stable communication.

---

## 🚀 Features Implemented

- Installation of Wazuh Manager and Dashboard on Ubuntu
- Deployment of Wazuh Agent on Windows 10 endpoint
- Sysmon installation with SwiftOnSecurity ruleset for detailed event monitoring
- Custom Wazuh detection rules for Nmap scans, Metasploit attacks, and port scanning
- Real-time alerting and log visualization via Wazuh dashboard

---

## 🔧 Setup Summary

### Ubuntu SIEM Server
```bash
curl -sO https://packages.wazuh.com/4.7/wazuh-install.sh
sudo bash wazuh-install.sh --wazuh-password wazuhadmin
