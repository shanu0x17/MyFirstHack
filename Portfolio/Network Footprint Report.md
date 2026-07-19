# 🌐 Network Footprint Report

## Analyst Information

| Field | Details |
|-------|---------|
| **Analyst** | Shantanu Gayke |
| **Analysis Date** | 19 July 2026 |
| **Engagement Type** | Passive Reconnaissance |
| **Target** | https://shivchhatrapaticollege.org/ |
| **Methodology** | DNS → WHOIS → Certificate Transparency → Technology Fingerprinting |

> **Disclaimer:** This assessment was conducted using only publicly available information. No active scanning, exploitation, or interaction with the target infrastructure was performed.

---

# Target Summary

| Item | Details |
|------|---------|
| **Domain** | https://shivchhatrapaticollege.org/ |
| **Description** | Educational institution website located in Chhatrapati Sambhajinagar, Maharashtra |
| **Reason for Selection** | Medium-sized educational organization suitable for passive reconnaissance practice |
| **Scope** | Public OSINT only (DNS, WHOIS, Certificate Transparency and Technology Enumeration) |

---

# Executive Summary

A passive reconnaissance assessment was performed against **shivchhatrapaticollege.org** to identify publicly accessible infrastructure and technology information. The investigation indicates that the website is hosted on **Hostinger**, while DNS resolution utilizes **Cloudflare's DNS infrastructure**. Email services are also managed through Hostinger.

Certificate Transparency logs reveal several publicly visible service-related subdomains such as **cpanel**, **webmail**, and **webdisk**, which indicate the presence of administrative services. The technology stack is primarily based on **WordPress** with the **Eduma** theme and supporting PHP-based components. Overall, the domain appears to be an established educational website with a long operational history and no immediately critical findings from passive reconnaissance.

---

# DNS Records

| Record Type | Value |
|-------------|-------|
| **A Record** | `92.112.198.111` |
| **MX Records** | `mx1.hostinger.com`<br>`mx2.hostinger.com` |
| **NS Records** | `ns1.dns-parking.com`<br>`ns2.dns-parking.com` |
| **TXT Record** | `v=spf1 include:_spf.mail.hostinger.com ~all` |

### Key Findings

- Website resolves to **Hostinger International Limited (AS47583)**.
- Email services are configured through **Hostinger Mail**.
- Authoritative DNS servers (`dns-parking.com`) resolve through Cloudflare infrastructure, indicating Cloudflare is used for DNS resolution.
- SPF record is configured to authorize Hostinger mail servers.

---

# WHOIS Information

| Field | Value |
|-------|-------|
| **Registrar** | GoDaddy.com, LLC |
| **Registration Date** | 11 December 2010 |
| **Expiration Date** | 11 December 2026 |
| **Registrant** | Registration Private |
| **Registrant Country** | United States |
| **Contact** | https://www.godaddy.com/whois/results.aspx?domain=shivchhatrapaticollege.org&action=contactDomainOwner |
| **Domain Age** | Approximately 15 years |

---

# Certificate Transparency

| Field | Value |
|-------|-------|
| **Certificates Issued** | 123 |
| **Primary CA** | Let's Encrypt |

### Discovered Subdomains

- `mail.shivchhatrapati.org`
- `cpanel.shivchhatrapaticollege.org`
- `webdisk.shivchhatrapaticollege.org`
- `webmail.shivchhatrapaticollege.org`

### Notes

No suspicious or abandoned subdomains were identified through passive analysis. Most discovered entries appear to support hosting and administrative services.

---

# Technology Profile

| Category | Technology |
|----------|------------|
| **Hosting Provider** | Hostinger |
| **CMS** | WordPress |
| **Theme** | Eduma |
| **Vendor** | ThimPress |
| **Programming Language** | PHP |
| **Libraries** | jQuery, Lightbox |
| **Other Components** | H5P, Google Static (GStatic) |

---

# Observations

- The target has maintained an active internet presence for approximately **15 years**, indicating a well-established domain.
- Hosting and email infrastructure are consolidated under **Hostinger**, simplifying infrastructure management.
- Multiple administrative service subdomains (**cpanel**, **webmail**, and **webdisk**) are publicly visible through Certificate Transparency logs. While this is common for shared hosting environments, these services should be properly secured and exposed only when necessary.
- The website is built on **WordPress**, which requires regular updates to plugins, themes, and the core platform to minimize security risks.

---

# Recommendations

- Review whether administrative services such as **cpanel**, **webmail**, and **webdisk** need to remain publicly accessible. Restrict access where possible using IP allowlists, VPNs, or multi-factor authentication.
- Ensure the **WordPress core**, installed plugins, and the **Eduma** theme are updated regularly to reduce exposure to known vulnerabilities.
- Periodically review DNS records and remove any obsolete or unused entries to minimize the public attack surface.
- Continue monitoring Certificate Transparency logs to identify newly issued certificates or unexpected subdomains.
- Verify that email authentication mechanisms (**SPF**, and where applicable **DKIM** and **DMARC**) remain correctly configured to strengthen email security.
- Perform periodic vulnerability assessments and security reviews to ensure the infrastructure remains secure over time.

---

# Conclusion

This passive reconnaissance exercise identified the publicly exposed infrastructure, DNS configuration, certificate information, and technology stack of **shivchhatrapaticollege.org** without interacting with the target systems. No critical security issues were observed through publicly available information alone. However, the presence of administrative subdomains and the use of a WordPress-based platform emphasize the importance of continuous maintenance, secure configuration, and regular security monitoring.

---
**Analysis Type:** Passive Reconnaissance (OSINT Only)

**Tools Used:** nslookup, WHOIS, crt.sh, Netcraft, Wappalyzer, BuiltWith, SecurityTrails (where applicable)
