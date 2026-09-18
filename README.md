# NETWORKWALKS-B083-WK2-PM1-PM5-REPORT
# 🔐 CYBERSECURITY & PENETRATION TESTING INTERNSHIP — WEEK 2

## FOOTPRINTING & NETWORK SCANNING

This report documents two connected exercises: gathering publicly available intelligence on a live, authorized domain (passive footprinting), and running a host-discovery scan against my own local network using Kali Linux and the Nmap/Zenmap toolset.

---

## ⚖️ Disclaimer

This work is intended purely for learning and authorized security research. Accessing systems without permission is illegal in most places, regardless of intent or outcome. Every task below was carried out only on infrastructure I own, have written authorization to test, or my own machine's local network.

---

## ⚙️ PROJECT OVERVIEW

| Field         | Detail                                     |
| ------------- | ------------------------------------------- |
| Intern        | Anas Qureshi                                  |
| Program/Batch | B083                                  |
| Report date   | 17.09.2026                                 |
| Targets       | networkwalks.com, own local network         |
| Phase covered | PM1 —  footprinting            |
|               | PM5 — Zenmap/Nmap ping scan & topology   |

⚠️ **Authorization Notice:** Every action recorded here was limited to systems I either own or have explicit written permission to test, done solely for training purposes. At no point was any exploit, intrusion, or unauthorized access attempted.

---
## 👜 ToolUsed

| Tool               | Stage        | What it's for                                             |
| ------------------ | ------------ | ----------------------------------------------------------- |
| whois               | Footprinting | Pulls domain registration records                          |
| nslookup            | Footprinting | Resolves DNS entries — IPs, mail servers, name servers      |
| whatweb             | Footprinting | Identifies the technologies powering a site                |
| wafw00f             | Footprinting | Flags whether a WAF is protecting the target                |
| curl -I             | Footprinting | Grabs just the HTTP response headers                        |
| dnsrecon            | Footprinting | Enumerates the full DNS record set                          |
| Kali Linux          | OS           | Platform used for the recon work                            |
| Windows + ipconfig  | OS           | Used to confirm the local host's IP                          |
| Zenmap (Nmap GUI)   | Scanning     | Ping scan, host discovery, and topology mapping             |

---
## 4. Activities Performed
## 4.1 Footprinting & Reconnaissance

I performed reconnaissance against the networkwalks.com domain using six Kali Linux tools: WHOIS, WhatWeb, Nslookup, Curl, Wafw00f and DNSRecon. Each tool was used to collect a different type of information about the target.
First, I used WHOIS to obtain publicly available domain registration information and identify the domain’s name servers. The results provided information about the domain registration and hosting infrastructure.
I then used WhatWeb to identify technologies used by the website. The results identified WordPress 7.0.4 and WP Download Manager 3.3.58, along with other information exposed by the website.
Using Nslookup, I resolved the domain name to its IP address. The provided result identified 192.232.216.135.
I used Curl with the -I option to inspect the HTTP response headers. This provided additional information about the web application and exposed the WordPress REST API endpoint /wp-json/.
Next, I used Wafw00f to determine whether a Web Application Firewall was protecting the website. The result identified ModSecurity (SpiderLabs).
Finally, I used DNSRecon to enumerate DNS records. The results provided information relating to name servers, mail servers, SPF/TXT records, service records and DNS software information.

## 4.2 Network Scanning with Zenmap
For the second activity, I used Zenmap to perform network discovery on my local network. The practical required me to identify my local IP address and subnet, discover live hosts, identify their IP and MAC addresses, and generate a network topology.
I first used the Windows ipconfig command to identify my local IP address and LAN subnet. I then entered the subnet into Zenmap and selected Ping Scan to identify active hosts.
The example results provided in the practical identified ten live hosts:
•	192.168.68.1
•	192.168.68.100
•	192.168.68.101
•	192.168.68.104
•	192.168.68.105
•	192.168.68.107
•	192.168.68.111
•	192.168.68.249
•	192.168.68.250
•	192.168.68.124
    The example results also included nine MAC addresses.
After completing the scan, I opened the Topology section in Zenmap, enabled the legend and saved the network topology in PDF format as required by the practical task.
Note: The actual subnet, number of hosts and addresses should be replaced with the results from my own network when submitting the report.
## Conclusion
During Week 2 of my Cybersecurity & Ethical Hacking internship, I completed practical activities covering footprinting, reconnaissance and network scanning.
In the footprinting activity, I used six Kali Linux tools to collect information about the target domain. I learned how WHOIS can provide domain information, WhatWeb can identify web technologies, Nslookup can resolve domain names, Curl can inspect HTTP headers, Wafw00f can identify a WAF, and DNSRecon can provide additional DNS information.
In the network scanning activity, I used Zenmap to identify my local network configuration and discover active hosts. I also collected IP and MAC address information and created a network topology.
The exercises showed me that information gathering is an important part of cybersecurity. Even before attempting to exploit a system, a security professional can learn a significant amount about an environment by carefully analyzing publicly available information and network responses.
I also learned that technical findings should be documented clearly. A good cybersecurity report should explain what was performed, what was discovered, what the observation means, what risk it may create, and what can be done to reduce that risk.
Finally, I learned that reconnaissance and scanning must always be performed within an authorized scope. These activities were completed as part of the assigned educational cybersecurity lab.
## Evidence Collected
<img width="1920" height="1037" alt="whois network" src="https://github.com/user-attachments/assets/ba6c8319-1d8d-4501-9fb4-89aaa3ca94ba" />
<img width="1920" height="1040" alt="whatweb" src="https://github.com/user-attachments/assets/f41af5bc-6cb9-4210-b0a8-cd7869e8e7d4" />
<img width="1920" height="1037" alt="curl" src="https://github.com/user-attachments/assets/db02f8af-a485-45f2-9736-23f1df18bd61" />

<img width="1917" height="1032" alt="wafwoof" src="https://github.com/user-attachments/assets/901461b0-2870-4853-a1d1-15e2c465fa46" />
<img width="1920" height="1040" alt="nslookup" src="https://github.com/user-attachments/assets/09ef0d49-83fe-42fd-b8ce-1219ce912980" />
<img width="1920" height="1038" alt="dns recon" src="https://github.com/user-attachments/assets/cffe23b8-7038-43c9-8415-52de19293794" />

<img width="1920" height="1080" alt="ping scan " src="https://github.com/user-attachments/assets/8ebc80c2-41e1-4a04-bb46-00196c76a9e3" />
<img width="1920" height="1080" alt="topology" src="https://github.com/user-attachments/assets/7fe95b82-1698-4f87-a191-38fc6f3f1495" />



