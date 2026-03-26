# Splunk SOC Analyst Query Reference

![Splunk](https://img.shields.io/badge/Splunk-SIEM-brightgreen?style=flat-square&logo=splunk)
![License](https://img.shields.io/badge/License-Apache%202.0-blue?style=flat-square)
![Queries](https://img.shields.io/badge/110-Detection%20Queries-orange?style=flat-square)
![SOC](https://img.shields.io/badge/SOC-Analyst%20Ready-red?style=flat-square)

> A curated library of **110 production-ready Splunk SPL queries** for Security Operations Center (SOC) analysts — covering threat detection, incident response, and proactive threat hunting.

---

## 📋 Table of Contents

- [Overview](#overview)
- [Categories Covered](#categories-covered)
- [How to Use](#how-to-use)
- [Requirements](#requirements)
- [Customisation Tips](#customisation-tips)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

This repository provides a structured, hands-on reference for SOC analysts using Splunk Enterprise or Splunk Cloud. Each file contains a single, focused SPL query targeting a specific threat scenario — from credential attacks and lateral movement to data exfiltration and ransomware detection.

Whether you are triaging alerts as a Tier 1 analyst, building detection rules as a Tier 2, or running threat hunts as a senior engineer, this library gives you a practical starting point for every major attack category.

---

## Categories Covered

| Category | Query Numbers |
|---|---|
| Authentication & Login Failures | 01, 04, 05, 17, 18, 19, 24 |
| Brute Force Attacks | 08, 26, 35, 38, 43, 47, 48, 60, 63, 71, 74, 78, 81, 84, 86, 88, 91, 92, 97, 100, 103, 105, 108 |
| Privilege Escalation | 03, 09, 25, 53, 64, 79, 85, 94, 104, 109 |
| Lateral Movement | 55, 66, 73, 77, 83, 87, 90, 93, 96, 99, 102, 107 |
| Data Exfiltration | 16, 40, 82, 89, 95, 98, 101, 106, 110 |
| Malware & Ransomware | 29, 32, 41, 62, 69 |
| Network Threats (DDoS, Port Scans, C2) | 06, 14, 23, 31, 39, 42, 50, 57, 61, 67, 70, 80 |
| PowerShell & Script-Based Attacks | 12, 58, 68, 85 |
| DNS Attacks & Tunneling | 11, 27, 45, 65, 95 |
| Web Application Attacks (SQLi, XSS, CSRF) | 02, 20, 46, 52, 54, 59, 71, 75, 76 |
| Email & Phishing | 15, 22, 28, 49, 75, 98 |
| Insider Threats | 10, 13, 33, 56, 72 |
| Reconnaissance | 51, 57 |
| Beaconing & C2 Communication | 67, 80 |

---

## How to Use

1. Clone or download this repository
2. Open any file in a text editor
3. Copy the SPL query into the **Splunk Search bar**
4. Adjust `sourcetype`, field names, and thresholds to match your environment
5. Schedule as an alert or add to a dashboard as needed

> **Tip:** Each file is numbered and titled for quick reference. Use the category table above to find the right query fast.

---

## Requirements

- Splunk Enterprise or Splunk Cloud
- Relevant data sources indexed (e.g. `linux_secure`, `WinEventLog`, `network_traffic`, `dns`, `access_*`)
- SOC analyst or security engineer role with search permissions

---

## Customisation Tips

- Replace `username` with actual usernames or tie to a lookup table
- Adjust count thresholds (e.g. `count >= 5`) to reflect your environment's baseline
- Scope queries with `index=your_index` for faster performance
- Chain multiple queries using `append` or `union` for correlation rules
- Use `| outputlookup` to export results for further analysis

---

## Contributing

Contributions are welcome. To add a query or improve an existing one:

1. Fork this repository
2. Create a branch: `git checkout -b feature/your-query-name`
3. Add your file following the naming convention: `111. Your query title`
4. Submit a pull request with a clear description of what it detects

---

## License

```
Copyright 2024 Splunk SOC Analyst Query Reference Contributors

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```

**Attribution:** This project is free to use under Apache 2.0. If you share or build upon it publicly — in blog posts, presentations, or other repositories — a credit or link back to this repository is appreciated.

---

## Disclaimer

These queries are provided for **defensive security and educational purposes only**. Always obtain proper authorisation before deploying detection rules in any environment. The contributors are not responsible for any misuse.

---

*Built for the SOC community. Open to all. Credit given where due.*
