# Dark Web Monitoring – Leak & Exposure Detection

**Objective:**

Simulate dark web monitoring workflows to detect exposed credentials, leaked data, and brand mentions using publicly available, ethical OSINT sources.

**Tools Used:**  
- DeHashed
- Leak-Lookup
- SOCRadar
- DarkFeed.io

**Scope & Ethics:**  

All searches were performed using demo identifiers such as 'examplebrand' and 'examplebrand@example.com'. 
No Tor access, intrusive actions, or unauthorized data collection occurred.
Only passive feeds, sanitized breach data, and public intelligence reports were referenced.
All screenshots were redacted to remove sensitive data, ensuring full compliance with OSINT ethics.

---

## Findings

| Type | Example | Source | Risk Note |
|------|----------|--------|-----------|
| Credential exposure | examplebrand@example.com | DeHashed | No breaches found; confirms clean record at time of check; continue periodic monitoring. |
| Dataset appearance | examplebrand@example.com | Leak-Lookup | No results found; reinforces clean status; continue periodic checks for new breach feeds. |
| Brand mention | examplebrand.net | SOCRadar Labs Dark Web Report | No stealer logs; credential leaks, or dark web mentions detected; reinforces brand's clean status at time of scan. |
| Ransomware activity | Global ransomware ecosystem | DarkFeed.io | Over 2,000 attacks tracked in 2025; LockBit, Play, and Akira remain dominant actors. Organizations in finance and healthcare face ongoing risk from active groups. |
| Sector exposure | Government, financial, healthcare | Darkfeed.io | Intelligence confirms continued targeting of public sector and healthcare entities. Reinforces need for proactive monitoring and ransomware defense readiness. |
---

## Evidence

### DeHashed Results

The email 'examplebrand@example.com' returns no results, confirming the demo email was not present in any known breach datasets. 

This reinforces strong credential hygiene and shows no current exposure in historical breach archives.

![Dehashed Results](https://github.com/DeemaZaher/Digital-Risk-Intelligence-Projects/blob/main/assets/dehashed_result.png?raw=true)

---

### Leak-Lookup Results

The email 'examplebrand@example.com' returned no matches across Leak-Lookup's breach archives.

This reinforces earlier DeHashed findings, confirming no known exposure across public or aggregated datasets.

![Leak-Lookup Results](https://github.com/DeemaZaher/Digital-Risk-Intelligence-Projects/blob/main/assets/leaklookup_result.png?raw=true)

---

### SOCRadar Labs Dark Web Report

The SOCRadar Labs Dark Web Report for 'examplebrand.net' showed **no stealer logs, credential leaks, or hacker mentions** across monitored sources.  

This confirms the brand’s clean posture and highlights how DRPS workflows provide enterprise-style visibility into dark web exposure.


![SOCRadar Results](https://github.com/DeemaZaher/Digital-Risk-Intelligence-Projects/blob/main/assets/socradar_result.png)

---

### DarkFeed.io Ransomware Groups Overview

Darkfeed.io visualizes ransomware ecosystem trends across active and inactive groups.
2025 metrics indicate a **rise in Q1 attacks**, with **LockBit (2,935 attacks)** leading, followed by **Play (981)**, **Akira (841)**, and **Qilin (812)**.

Healthcare and financial sectors remain **high-risk**, while **over 8,800 U.S. incidents** highlight geographic concentration.
Inactive groups such as **El Dorado** and **Silent** show lifecycle turnover, reflecting takedowns or regrouping.

![DarkFeed Results Ransomware Groups](https://github.com/DeemaZaher/Digital-Risk-Intelligence-Projects/blob/main/assets/darkfeed_ransomwaregroups.png)


![DarkFeed Results Ransomware Teams](https://github.com/DeemaZaher/Digital-Risk-Intelligence-Projects/blob/main/assets/darkfeed_ransomwareteamgroups.png)


---

## Insights

This assessment demonstrates **how dark web intelligence supports DRP and exposure management**.
By cross-referencing multiple open-source intelligence tools (DeHashed, Leak-Lookup, SOCRadar, Darkfeed.io), analysts gain a **multi-layered view** of exposure, reputation, and threat landscape.

Even when no exposures are found, verifying across distinct datasets confirms **sound brand hygiene**.
Monitoring ransomware trends offers forward-looking insight into **actor TTPs**, **target sectors**, and **campaign volumes**, supporting better prioritization in defensive roadmaps.

## Next Steps

- Maintain **continuous credential monitoring** through DeHashed and Leak-Lookup

- Schedule **monthly SOCRadar scans** to detect emerging stealer logs or credentials

- Subscribe to **Darkfeed.io** or **Styx Intelligence** for ransomware and dark web trend tracking

- Integrate findings into SIEM or EASM tooling for contextual alerting

- Conduct **quarterly exposure audits** to adapt to evolving underground marketplaces
