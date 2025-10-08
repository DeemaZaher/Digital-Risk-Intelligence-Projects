# External Attack Surface Mapping – scanme.nmap.org

**Objective:**  
Simulate attacker reconnaissance by mapping a safe, permissioned host and identifying exposed services.

**Tools Used:**  
- Shodan
- Censys

**Scope & Ethics:**  
Passive OSINT only. scanme.nmap.org is a legal, publicly authorized host for testing. No intrusive scanning performed.

---

## Findings

| Asset | Port/Service | Tool | Risk Note |
|-------|---------------|------|-----------|
| scanme.nmap.org (45.33.32.156) | 22/SSH (OpenSSH_6.6.1p1) | Shodan | Outdated SSH version visible; restrict access or update |
| scanme.nmap.org | 80/HTTP (Apache/2.4.7 Ubuntu) | Shodan | Web service responding with 400; ensure secure headers and disable detailed error messages |
| scanme.nmap.org | 123/NTP | Shodan | Time service exposed; restrict to internal access only |
| scanme.nmap.org |31337/Custom Port  | Shodan | Likely test/debug port; verify necessity and close if unused |
| scanme.nmap.org | 9929/Nmap Service | Shodan | Nmap test port; confirm safe exposure |
| scanme.nmap.org | 80/HTTP (Apache httpd) | Censys | Banner "Go ahead and ScanMe!" confirms public-facing web property; replace default banners in production |
| scanme.nmap.org | 443/HTTPS | Censys | TLS endpoint detected; validate certificate configuration and enforce modern cipher suites |


---

## Evidence

**Shodan Results**

![Shodan Results](https://github.com/DeemaZaher/Digital-Risk-Intelligence-Projects/blob/main/assets/Shodan_Results.png)


**Censys Results**

![Censys Results](https://github.com/DeemaZaher/Digital-Risk-Intelligence-Projects/blob/main/assets/Censys_Results.png)

---

## Insights
I looked at this target the way an attacker would. Shodan and Censys revealed open ports (SSH, HTTP, HTTPS, NTP) and detailed service banners, showing how much fingerprinting can happen from the outside. Even a harmless demo host exposed default messages like "Go ahead and ScanMe!" abd service versions that could guide exploitation if left unpatched. Seeing both HTTP and HTTPS confirmed that encryption alone doesn't hide exposure, TLS endpoints can still leak metadata if not configured properly. This assessment reinforced how visibility, patching, and monitoring work together to reduce external risk.

---

## Next Steps
- Restrict SSH access (port 22) to trusted IPs or VPN only
- Close unused ports (31337, 9929)
- Update Apache and SSH to latest stable versions
- Monitor TLS configurations and web headers for data exposure
- Integrate these findings into attack surface management workflows
