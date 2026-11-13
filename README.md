# Week 2 – Footprinting & Reconnaissance

**Cybersecurity Internship | Networkwalks**  
**Participant:** Labeeba Manzoor  
**Batch:** B084

This repository contains the Week 2 practical work on footprinting, reconnaissance and local network discovery.

## Project Overview

The practical exercises involved collecting publicly available domain information, checking DNS and HTTP details, identifying website technologies, attempting WAF fingerprinting, and scanning the local subnet for active hosts.

**Target domain:** `networkwalks.com`

## Tools Used

- WHOIS – domain registration information
- Nslookup – DNS lookup
- WhatWeb – website technology identification
- cURL – HTTP response/header inspection
- DNSRecon – DNS enumeration
- WAFW00F – web application firewall fingerprinting
- Zenmap/Nmap – local network host discovery

## Repository Structure

```text
Week-2-Footprinting-Reconnaissance/
├── Screenshots/
│   ├── PM1_01_WHOIS.jpeg
│   ├── PM1_02_NSLOOKUP.jpeg
│   ├── PM1_03_WHATWEB.jpeg
│   ├── PM1_04_CURL_HEADERS.jpeg
│   ├── PM1_05_WAFW00F.jpeg
│   ├── PM1_06_DNSRECON.jpeg
│   ├── PM5_01_ZENMAP_PING_SCAN.png
│   └── PM5_02_ZENMAP_NETWORK_TOPOLOGY.pdf
├── Outputs/
│   ├── whois_summary.txt
│   ├── nslookup.txt
│   ├── whatweb.txt
│   ├── curl_headers.txt
│   ├── wafw00f.txt
│   ├── dnsrecon.txt
│   ├── zenmap_ping_scan.txt
│   └── findings_summary.txt
├── Reports/
│   └── Labeeba_Manzoor_B084_Penetration_Testing_Report.pdf
└── README.md
```

## Key Observations

- WHOIS showed registrar GoDaddy.com, LLC, name servers NS6135.HOSTGATOR.COM and NS6136.HOSTGATOR.COM, creation date 2019-11-06 and expiry date 2027-11-06.
- The target domain resolved to `192.232.216.135`.
- WhatWeb identified Apache, WordPress 7.1.4, WP Download Manager 3.3.76 and jQuery 3.7.1.
- The cURL header request returned `HTTP 200 OK` and identified Apache.
- DNSRecon reported 8 records, including SOA, NS, MX, A, TXT and SRV categories.
- WAFW00F timed out, so WAF identification remained inconclusive.
- The local adapter used IPv4 address `172.20.10.2`, subnet mask `255.255.255.240` and gateway `172.20.10.1`.
- The subnet `172.20.10.0/28` was scanned using `nmap -sn`. The scan covered 16 IP addresses and reported 2 hosts up in 7.12 seconds.

## Outputs and Evidence

The `Screenshots` folder contains the captured practical evidence. The `Outputs` folder contains readable summaries of the observed command results. These text files are summaries, not verbatim terminal logs; refer to the screenshots for the original captured output.

The `Reports` folder contains the detailed PDF report.

## Disclaimer

This repository is intended for educational purposes as part of the Networkwalks cybersecurity internship. Scanning and reconnaissance should only be performed on systems and networks for which appropriate authorization has been obtained.
