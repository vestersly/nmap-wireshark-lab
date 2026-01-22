# 🔍 Nmap + Wireshark: TCP SYN Scan Explained

> **Hands-on network security lab demonstrating how Nmap scan results map directly to real TCP/IP packets captured with Wireshark.**

---

## 🔐 Privacy & Environment Note
All IP addresses in this repository are anonymized (`10.10.10.x`) for security and privacy.  
This lab was conducted in an **isolated VirtualBox environment** for educational and ethical purposes only.

---

## 📌 Overview

This project demonstrates **how active network reconnaissance works at the packet level**.

By combining **Nmap** and **Wireshark**, the lab shows how:
- TCP SYN scans operate internally
- Open, closed, and filtered ports behave differently
- Scan results directly correlate with TCP flags and responses

Rather than treating Nmap as a “black box,” this project focuses on **understanding what actually happens on the wire**.

---

## 🎯 Why This Project Matters

Modern security roles often abstract networking behind tools, dashboards, and automation.  
However, **strong security engineers understand the fundamentals underneath**.

This lab demonstrates:
- Low-level TCP/IP knowledge
- Practical understanding of reconnaissance techniques
- Ability to validate tool output using packet analysis
- Security awareness at the network layer

These skills are directly applicable to:
- SOC & Blue Team analysis
- Firewall and IDS/IPS validation
- Cloud network security troubleshooting
- Incident response investigations

---

## 🧪 Lab Setup

- **Attacker:** Kali Linux (`10.10.10.20`)
- **Target:** Ubuntu Server (`10.10.10.19`)
- **Virtualization:** VirtualBox (Bridged networking)
- **Packet Capture:** Wireshark on Ubuntu (`enp0s3`)

---

## ⚙️ Methodology

### 1️⃣ TCP SYN Scan from Kali

```bash
sudo nmap -sS -sV 10.10.10.19
