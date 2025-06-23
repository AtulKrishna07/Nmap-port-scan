# Task 1 - Network Port Scanning with Nmap

## Objective
To perform a network scan using Nmap and identify open ports and potential security risks on devices in the local network.

## Tools Used
- Nmap

## Command Used
nmap -sS 192.168.1.0/24 -oN scan_results.txt

SCAN SUMMARY

Nmap detected 9 active hosts with various open ports:

192.168.1.1 – local.airtelfiber.com
Open Ports: 53 (DNS), 80 (HTTP), 443 (HTTPS), 5555 (freeciv)

Risk: Port 5555 is sometimes associated with ADB or custom apps, may pose risk if exposed externally.

192.168.1.2 – Tuya Smart Device
Open Port: 6668 (IRC)

Risk: IoT devices with open IRC-like ports can be vulnerable to botnets if not secured.

192.168.1.5 – Tenda Router
Open Port: 80 (HTTP)

Risk: If not password protected, admin panel may be exposed.

192.168.1.6 – Amazon Device
Open Ports: 1080 (SOCKS), 8888, 10001

Risk: Uncommon ports could expose services; ensure access is limited.

192.168.1.9 – iPhone Device
Open Ports: 49152 (unknown), 62078 (iPhone sync)

Risk: Normal for iPhones, but high numbered open ports should be firewalled.

192.168.1.10
Open Ports: 135 (MSRPC), 445 (Microsoft-DS)

Risk: SMB (445) is vulnerable if not patched; often targeted by ransomware.

192.168.1.11
Open Ports: 135 (MSRPC), 139 (NetBIOS), 445 (Microsoft-DS)

Risk: Legacy NetBIOS and SMB services can allow unauthorized file access or exploitation.
