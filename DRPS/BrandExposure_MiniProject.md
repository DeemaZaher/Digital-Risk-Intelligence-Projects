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

<img width="683" height="752" alt="image" src="https://github.com/user-attachments/assets/e6622830-2973-4248-bca1-7349f74a2c52" />



<img width="702" height="746" alt="image" src="https://github.com/user-attachments/assets/2f8dca5f-0124-4b2c-bca9-350efca83bd5" />



**Scamadviser Results**

A reputation scan of 'examplebrand.net' showed the domain is offline but carries a high trust rating (85/100).
Even dormant domains can be repurposed by attackers for phishing or brand impersonation, emphasizing the importance of ongoing monitoring.

<img width="623" height="756" alt="image" src="https://github.com/user-attachments/assets/d57ceaaa-e18b-4bef-9b3d-5410fe346261" />  



**HIBP Results**

The email 'examplebrand@example.com' was checked for credential exposure.
No breaches were found, confirming strong hygiene at this time and reinforcing the value of proactive monitoring.


<img width="653" height="755" alt="image" src="https://github.com/user-attachments/assets/1672955f-2215-4f4b-a73f-697be64a4416" />



**URLVoid Results**

Reputation checks across multiple security engines returned no blacklists or active threats for 'examplebrand.net'.
Consistent clean results across vendors confirm the domain’s low current risk but highlight the need for continuous reputation tracking.

<img width="1029" height="735" alt="image" src="https://github.com/user-attachments/assets/de80731f-34e0-4307-8858-0da3bfcfe356" />

<img width="1104" height="721" alt="image" src="https://github.com/user-attachments/assets/1ee11d48-6626-48b9-ba6c-5ef967fe9b87" />

<img width="1004" height="727" alt="image" src="https://github.com/user-attachments/assets/23d7a877-52bd-4570-9fb9-65e3d35dca12" />

**VirusTotal Results**

VirusTotal scans verified no detections across 70+ engines and confirmed the domain’s inactive status through passive DNS records.
These results reinforce the findings from Scamadviser and URLVoid, validating the domain’s low-risk profile.

<img width="1012" height="815" alt="image" src="https://github.com/user-attachments/assets/e60fed12-0289-4e84-bc4f-7fe50dbb0164" />

<img width="1035" height="813" alt="image" src="https://github.com/user-attachments/assets/da88c3e7-0b4a-4193-8380-21c6a08c6a62" />


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
