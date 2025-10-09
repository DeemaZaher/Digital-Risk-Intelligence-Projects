# Digital Risk Protection – Brand & Credential Exposure

**Objective:**  
Simulate DRP workflows to identify impersonation risks, domain lookalikes, and credential exposures using passive OSINT tools.

**Tools Used:**  
Namechk, Scamadviser, HaveIBeenPwned, URLVoid, VirusTotal

**Scope & Ethics:**  
All analysis was conducted using publicly available, passive OSINT sources.  
No intrusive scanning, exploitation, or unauthorized access was performed.  
The brand name 'examplebrand' and associated domains were selected for demonstration purposes only.  
All screenshots were redacted to remove personal or sensitive data.  
This project adheres to responsible disclosure and ethical intelligence-gathering practices in alignment with industry standards.

**Ethical Summary**

All domains analyzed were publicly available or RFC-approved examples. Only passive lookups and reputation checks were conducted; no intrusive scanning was performed.

---

## Findings

| Type | Example | Source | Risk Note |
|------|----------|--------|-----------|
| Handle squat | examplebrand taken on select platforms | Namechk | Could be used for impersonation |
| Lookalike domain | examplebrand.net | Scamadviser | Offline but high trust; monitor for reactivation |
| Credential exposure | examplebrand@example.com | HIBP | No breaches found; continue proactive monitoring |
| Domain reputation | examplebrand.net | URLVoid | Clean reputation across major blacklists; no active malicious indicators detected. Continued monitoring recommended in case of future re-registration or misuse |
| Threat intelligence correlation | examplebrand.net | VirusTotal | No detections reported across 70+ engines; passive DNS history confirms domain currently inactive but safe. Suggest re-check during future brand sweeps |

---

## Evidence

**Namechk Results**

The handle 'examplebrand' was checked across major social platforms and domains to identify potential impersonation risks.
Some platforms show the handle as taken, illustrating how easily threat actors can pose as the brand if accounts remain unclaimed.

![Namechk Result 1](https://github.com/DeemaZaher/Digital-Risk-Intelligence-Projects/blob/main/assets/Namecheckdomain.png)

![Namechk Result 2](https://github.com/DeemaZaher/Digital-Risk-Intelligence-Projects/blob/main/assets/NameCheckUsersSocials.png)


**Scamadviser Results**

A reputation scan of 'examplebrand.net' showed the domain is offline but carries a high trust rating (85/100).
Even dormant domains can be repurposed by attackers for phishing or brand impersonation, emphasizing the importance of ongoing monitoring.

![Scamadviser Result](https://github.com/DeemaZaher/Digital-Risk-Intelligence-Projects/blob/main/assets/ScamAdviser_Results.png)


**HIBP Results**

The email 'examplebrand@example.com' was checked for credential exposure.
No breaches were found, confirming strong hygiene at this time and reinforcing the value of proactive monitoring.


![HIBP Result](https://github.com/DeemaZaher/Digital-Risk-Intelligence-Projects/blob/main/assets/HIBP_Results.png)


**URLVoid Results**

Reputation checks across multiple security engines returned no blacklists or active threats for 'examplebrand.net'.
Consistent clean results across vendors confirm the domain’s low current risk but highlight the need for continuous reputation tracking.

![URLVoid 1](https://github.com/DeemaZaher/Digital-Risk-Intelligence-Projects/blob/main/assets/URLVoid_Results.png)


![URLVoid 2](https://github.com/DeemaZaher/Digital-Risk-Intelligence-Projects/blob/main/assets/URLVoidInfo.png)


![URLVoid 3](https://github.com/DeemaZaher/Digital-Risk-Intelligence-Projects/blob/main/assets/URLVoidScanning.png)


**VirusTotal Results**

VirusTotal scans verified no detections across 70+ engines and confirmed the domain’s inactive status through passive DNS records.
These results reinforce the findings from Scamadviser and URLVoid, validating the domain’s low-risk profile.

![VirusTotal 1](https://github.com/DeemaZaher/Digital-Risk-Intelligence-Projects/blob/main/assets/VirusTotal_Results1.png)


![VirusTotal 2](https://github.com/DeemaZaher/Digital-Risk-Intelligence-Projects/blob/main/assets/VirusTotal_Results2.png)


---

## Insights

This assessment simulated how attackers could impersonate a brand, register lookalike domains, or exploit leaked credentials across public platforms.
Checking handle availability showed how easily threat actors can create spoofed accounts to mislead users or damage brand reputation.
Lookalike domains, even those offline, demonstrate latent risk, as dormant assets can be reactivated for phishing or fraud campaigns.
Credential exposure checks highlighted why brands should rotate passwords regularly, enable MFA, and monitor breaches across multiple datasets.

Cross-verifying findings across Namechk, Scamadviser, HaveIBeenPwned, URLVoid, VirusTotal, and crt.sh provided a layered view of potential risks.  
Even clean results are valuable, they confirm strong hygiene today but reinforce the need for continuous monitoring, as reputation scores and threat landscapes shift over time.  
Combining these sources mirrors real-world DRPS workflows, where multiple intelligence feeds are used to validate, correlate, and prioritize alerts with context.

---

## Next Steps

- Register brand handles across major social platforms to prevent impersonation
- Monitor domain registrations for lookalikes using Scamadviser, crt.sh, and passive DNS feeds
- Reset exposed credentials and enforce MFA on all accounts
- Set up automated alrets via HIBP or DeHashed for future credential exposures
- Integrate URLVoid and VirusTotal checks into regular brand sweeps for updated reputation scores
- Establish a recurring quarterly DRPS review to ensure evolving risks are captured early
- Consider onboarding an enterprise DRP/EASM platform (e.g., Styx Intelligence) for centralized visibility and alerting
