# 🔍 Nmap + Wireshark: TCP SYN Scan Explained

> **Privacy note:** All IP addresses in this report are anonymized (`10.10.10.x`) for security.  
> The lab was performed in an isolated VirtualBox environment.

## 📌 Overview
This project demonstrates how **Nmap results** map directly to **TCP/IP packets** captured with Wireshark.  
It shows how open, closed, and filtered ports respond differently at the packet level.

## 🖥️ Lab Setup
- **Attacker (Kali Linux):** `10.10.10.20`
- **Target (Ubuntu):** `10.10.10.19`
- **Virtualization:** VirtualBox (Bridged mode)
- **Sniffer:** Wireshark on Ubuntu (`enp0s3`)

## ⚡ Method
1. From Kali, run an Nmap SYN + version scan:
   ```bash
   sudo nmap -sS -sV 10.10.10.19
