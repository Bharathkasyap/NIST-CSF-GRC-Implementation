# Risk Register — TechNova Financial Services

**Organization:** TechNova Financial Services, Inc.
**Framework:** NIST SP 800-30 Rev. 1 / NIST CSF 2.0
**Assessment Date:** Week 7–11
**Last Updated:** Week 11
**Version:** 1.0
**Owner:** Venkata Bharath Kasyap Devulapalli, GRC Analyst & Project Lead

---

## Risk Scoring Methodology

### Likelihood Scale

| Score | Level | Description |
|-------|-------|-------------|
| 5 | Very High | Near certain to occur (>80% in 12 months) |
| 4 | High | Likely to occur (60-80% in 12 months) |
| 3 | Medium | Possible (40-60% in 12 months) |
| 2 | Low | Unlikely (20-40% in 12 months) |
| 1 | Very Low | Rare (<20% in 12 months) |

### Impact Scale

| Score | Level | Business Impact Description |
|-------|-------|---------------------------|
| 5 | Critical | Catastrophic — regulatory action, >$10M loss, operations halted |
| 4 | High | Major — significant regulatory risk, $1M-$10M loss, major disruption |
| 3 | Medium | Moderate — manageable regulatory risk, $100K-$1M loss |
| 2 | Low | Minor — minimal regulatory impact, <$100K loss |
| 1 | Very Low | Negligible — no significant business impact |

### Risk Score = Likelihood x Impact (Range: 1–25)

| Risk Score | Rating | Action Required |
|-----------|--------|----------------|
| 20–25 | Critical | Immediate action required; Executive escalation |
| 15–19 | High | Action required within 30 days; assigned to senior owner |
| 8–14 | Medium | Action required within 90 days; tracked in risk register |
| 1–7 | Low | Monitor; accept or address in standard operations |

---

## Risk Register

### ACCESS CONTROL RISKS

| Risk ID | Risk Title | Threat Source | Vulnerability | Likelihood | Impact | Score | Rating | Treatment | Owner | Target Date | Status |
|---------|-----------|--------------|--------------|-----------|--------|-------|--------|-----------|-------|-------------|--------|
| RSK-001 | Privileged account compromise via weak/absent MFA | External attacker, Insider | 847 privileged accounts lack MFA enforcement | 4 | 5 | 20 | Critical | Mitigate — Deploy CyberArk PAM + MFA enforcement | IAM Team | Week 29 | CLOSED |
| RSK-002 | Excessive privileged access — least privilege violations | Insider | RBAC not enforced; 312 users with admin rights not requiring admin | 3 | 4 | 12 | Medium | Mitigate — RBAC review and Okta IGA deployment | IAM Team | Week 33 | CLOSED |
| RSK-006 | Insider threat — unauthorized data exfiltration | Malicious insider | No DLP controls; outbound traffic not monitored | 3 | 4 | 12 | Medium | Mitigate — Deploy Microsoft Purview DLP | DLP/HR | Week 31 | CLOSED |
| RSK-014 | Shared/generic credentials in use | External attacker, Insider | 47 shared service accounts identified in scan | 3 | 3 | 9 | Medium | Mitigate — Password vault for shared accounts | IAM Team | Week 29 | CLOSED |
| RSK-023 | Terminated employee access not revoked | Insider | IGA review found 23 active accounts for terminated employees | 2 | 4 | 8 | Medium | Mitigate — Automated provisioning/deprovisioning | IAM Team | Week 33 | CLOSED |
| RSK-031 | Remote access (VPN) without device compliance check | External attacker | VPN allows connections from unmanaged personal devices | 3 | 3 | 9 | Medium | Mitigate — Conditional access policies in Okta | IAM Team | Week 28 | CLOSED |
| RSK-038 | No privileged access session recording | Internal audit, Insider | Privileged sessions not logged or recorded | 2 | 3 | 6 | Low | Mitigate — CyberArk session management | IAM Team | Week 30 | CLOSED |
| RSK-045 | Default credentials on network devices | External attacker | 12 network devices using vendor defaults | 4 | 3 | 12 | Medium | Mitigate — Credential audit and rotation | Network Team | Week 28 | CLOSED |

### NETWORK SECURITY RISKS

| Risk ID | Risk Title | Threat Source | Vulnerability | Likelihood | Impact | Score | Rating | Treatment | Owner | Target Date | Status |
|---------|-----------|--------------|--------------|-----------|--------|-------|--------|-----------|-------|-------------|--------|
| RSK-003 | SQL injection on customer portal | External attacker | DAST scan found 3 SQLi vulnerabilities on public-facing portal | 4 | 4 | 16 | High | Mitigate — WAF + application fix | AppSec Team | Week 34 | CLOSED |
| RSK-010 | Insufficient network segmentation — legacy systems | External attacker | Legacy systems on flat network; breach could spread laterally | 3 | 4 | 12 | Medium | Mitigate — Implement microsegmentation (Cisco Firepower) | Network Team | Week 32 | CLOSED |
| RSK-019 | Unpatched network infrastructure CVEs | External attacker | Nessus scan: 31 critical CVEs on network devices | 4 | 4 | 16 | High | Mitigate — Emergency patching sprint; patch 100% in 30 days | Network Team | Week 28 | CLOSED |
| RSK-028 | No intrusion detection on east-west traffic | External attacker | IDS only on perimeter; lateral movement not monitored | 3 | 4 | 12 | Medium | Mitigate — Deploy Cisco StealthWatch for east-west | Network Team | Week 33 | CLOSED |
| RSK-035 | Unencrypted internal network traffic (sensitive data) | Insider, External | TLS not enforced on all internal DB connections | 3 | 3 | 9 | Medium | Mitigate — TLS enforcement policy + implementation | Network Team | Week 35 | CLOSED |
| RSK-042 | DNS security gap | External attacker | No DNSSEC or DNS filtering in place | 3 | 3 | 9 | Medium | Mitigate — Deploy Cisco Umbrella for DNS security | Network Team | Week 31 | CLOSED |
| RSK-047 | Open firewall rules — over-permissive | External attacker | Firewall review found 89 rules with ANY/ANY or overly broad rules | 4 | 3 | 12 | Medium | Mitigate — Firewall rule review and cleanup | Network Team | Week 30 | CLOSED |
| RSK-011 | No DDoS protection on customer-facing systems | External attacker | Customer portal exposed without DDoS mitigation | 2 | 4 | 8 | Medium | Transfer — Cloudflare DDoS protection (vendor) | Network Team | Week 30 | CLOSED |
| RSK-040 | Wireless network insufficient segmentation | External attacker | Guest WiFi bridges to corporate network in 3 offices | 2 | 3 | 6 | Low | Mitigate — VLAN separation for guest network | Network Team | Week 29 | CLOSED |

### DATA PROTECTION RISKS

| Risk ID | Risk Title | Threat Source | Vulnerability | Likelihood | Impact | Score | Rating | Treatment | Owner | Target Date | Status |
|---------|-----------|--------------|--------------|-----------|--------|-------|--------|-----------|-------|-------------|--------|
| RSK-008 | Sensitive data at rest not encrypted | External attacker, Insider | 23 databases with PII/PCI data lack at-rest encryption | 3 | 4 | 12 | Medium | Mitigate — BitLocker/TDE encryption deployment | Data Protection | Week 35 | CLOSED |
| RSK-016 | PCI-DSS data stored beyond retention requirements | Compliance | Data retention policy not enforced; 4-year-old PAN data found | 2 | 4 | 8 | Medium | Mitigate — Data retention enforcement + disposal | Compliance | Week 36 | CLOSED |
| RSK-024 | No DLP controls on email | Insider, External | Sensitive data can be emailed externally without restriction | 3 | 3 | 9 | Medium | Mitigate — Microsoft Purview email DLP policies | DLP Team | Week 31 | CLOSED |
| RSK-032 | Cloud storage with public access misconfiguration | External attacker | 3 Azure Blob storage containers set to public access | 4 | 4 | 16 | High | Mitigate — Immediate remediation + policy | Cloud Team | Week 27 | CLOSED |
| RSK-043 | Backup data not encrypted | External attacker | Backup tapes stored offsite without encryption | 2 | 4 | 8 | Medium | Mitigate — Implement backup encryption | IT Ops | Week 35 | CLOSED |
| RSK-046 | No data classification labels on documents | Insider | Document classification policy not implemented | 2 | 3 | 6 | Low | Mitigate — Microsoft Purview sensitivity labels | Data Protection | Week 36 | CLOSED |
| RSK-015 | Credit card data in non-PCI-compliant systems | Compliance | PAN data found in 2 systems outside PCI scope | 3 | 5 | 15 | High | Mitigate — Scope remediation; data moved or tokenized | Compliance | Week 30 | CLOSED |

### INCIDENT RESPONSE RISKS

| Risk ID | Risk Title | Threat Source | Vulnerability | Likelihood | Impact | Score | Rating | Treatment | Owner | Target Date | Status |
|---------|-----------|--------------|--------------|-----------|--------|-------|--------|-----------|-------|-------------|--------|
| RSK-009 | No documented IR playbooks for major threat scenarios | External attacker | Zero IR playbooks in existence; response is ad hoc | 4 | 5 | 20 | Critical | Mitigate — Develop 12 playbooks by Week 35 | IR Team | Week 35 | CLOSED |
| RSK-017 | No SIEM — limited visibility into security events | External attacker | No centralized log management or SIEM platform | 4 | 5 | 20 | Critical | Mitigate — Deploy Microsoft Sentinel; tuned by Week 33 | SOC Team | Week 33 | CLOSED |
| RSK-025 | No 24/7 SOC coverage | External attacker | After-hours security events go undetected | 4 | 4 | 16 | High | Mitigate — SOC expansion to 24/7 + Managed SOC for gaps | SOC Team | Week 30 | CLOSED |
| RSK-033 | IR escalation matrix not defined | External attacker | No documented escalation path for security incidents | 3 | 4 | 12 | Medium | Mitigate — Document escalation matrix in playbooks | IR Team | Week 35 | CLOSED |
| RSK-041 | No post-incident review process | Internal | Incidents closed without lessons-learned documentation | 2 | 3 | 6 | Low | Mitigate — PIR template and process | IR Team | Week 36 | CLOSED |

### THIRD-PARTY / SUPPLY CHAIN RISKS

| Risk ID | Risk Title | Threat Source | Vulnerability | Likelihood | Impact | Score | Rating | Treatment | Owner | Target Date | Status |
|---------|-----------|--------------|--------------|-----------|--------|-------|--------|-----------|-------|-------------|--------|
| RSK-005 | Third-party data breach — Tier 1 vendor | Third-party | No contractual security requirements for Tier 1 vendors | 3 | 5 | 15 | High | Mitigate — Vendor security assessments + contract standards | Vendor Mgmt | Week 25 | CLOSED |
| RSK-013 | No vendor security assessment process | Compliance | 47 vendors with data access; 0 have been formally assessed | 3 | 4 | 12 | Medium | Mitigate — TPRM program with tiered assessment process | Vendor Mgmt | Week 25 | CLOSED |
| RSK-021 | Vendor with excessive data access | Vendor, Insider | 3 Tier 1 vendors have broader data access than required | 2 | 4 | 8 | Medium | Mitigate — Contractual access scoping and monitoring | Vendor Mgmt | Week 26 | CLOSED |
| RSK-029 | Software supply chain — open source vulnerabilities | External attacker | No SCA tooling; open source dependencies not inventoried | 3 | 3 | 9 | Medium | Mitigate — Deploy Snyk or Dependabot for SCA | AppSec Team | Week 34 | CLOSED |
| RSK-037 | No fourth-party (sub-processor) visibility | Third-party | Core banking vendor has 12 sub-processors; 0 assessed | 2 | 3 | 6 | Low | Accept — Monitor; review in annual vendor assessment | Vendor Mgmt | Ongoing | ACCEPTED |
| RSK-044 | Vendor access not monitored | Third-party, Insider | Vendor remote access sessions not logged or reviewed | 3 | 3 | 9 | Medium | Mitigate — Vendor access through CyberArk EPM | IAM Team | Week 32 | CLOSED |

### APPLICATION SECURITY RISKS

| Risk ID | Risk Title | Threat Source | Vulnerability | Likelihood | Impact | Score | Rating | Treatment | Owner | Target Date | Status |
|---------|-----------|--------------|--------------|-----------|--------|-------|--------|-----------|-------|-------------|--------|
| RSK-004 | Unpatched critical application vulnerabilities (106 CVEs) | External attacker | 106 critical + high CVEs identified across 136 systems | 4 | 4 | 16 | High | Mitigate — Emergency patch sprint; 100% critical in 30 days | Patching Team | Week 30 | CLOSED |
| RSK-012 | No SAST/DAST in CI/CD pipeline | External attacker | Applications deployed without security testing | 3 | 3 | 9 | Medium | Mitigate — Integrate Veracode SAST/DAST in pipeline | AppSec Team | Week 34 | CLOSED |
| RSK-020 | Cross-site scripting (XSS) vulnerabilities | External attacker | DAST scan: 7 XSS findings on customer portal | 4 | 3 | 12 | Medium | Mitigate — Application fix + WAF rules | AppSec Team | Week 34 | CLOSED |
| RSK-027 | Insecure API endpoints | External attacker | 4 API endpoints lack authentication | 3 | 4 | 12 | Medium | Mitigate — API gateway + authentication enforcement | AppSec Team | Week 34 | CLOSED |
| RSK-036 | No mobile application security testing | External attacker | Mobile banking app not tested for security | 2 | 4 | 8 | Medium | Mitigate — Mobile DAST (quarterly) | AppSec Team | Week 40 | CLOSED |
| RSK-039 | Hardcoded credentials in application code | External attacker | Code scan found 8 instances of hardcoded credentials | 4 | 4 | 16 | High | Mitigate — Code remediation + secrets management | AppSec Team | Week 28 | CLOSED |
| RSK-048 | Security headers missing on web applications | External attacker | Missing HSTS, CSP, X-Frame-Options on 6 web apps | 3 | 2 | 6 | Low | Mitigate — Security headers implementation | AppSec Team | Week 34 | CLOSED |

### PEOPLE / AWARENESS RISKS

| Risk ID | Risk Title | Threat Source | Vulnerability | Likelihood | Impact | Score | Rating | Treatment | Owner | Target Date | Status |
|---------|-----------|--------------|--------------|-----------|--------|-------|--------|-----------|-------|-------------|--------|
| RSK-007 | Phishing attack leading to credential theft | External attacker | Phishing simulation: 32% click rate; no security awareness training | 4 | 4 | 16 | High | Mitigate — KnowBe4 training + monthly phishing sims | HR/CISO | Week 27 | CLOSED |
| RSK-018 | No security awareness training program | External attacker | Only 22% of employees completed any security training | 4 | 3 | 12 | Medium | Mitigate — Mandatory KnowBe4 training for all 850 FTE | HR/CISO | Week 27 | CLOSED |
| RSK-026 | Social engineering — vishing susceptibility | External attacker | No vishing testing or awareness conducted | 2 | 3 | 6 | Low | Mitigate — Include vishing in awareness program | HR/CISO | Week 36 | CLOSED |
| RSK-034 | Developers lack secure coding training | External attacker | No secure development lifecycle (SDLC) training | 3 | 3 | 9 | Medium | Mitigate — Secure coding training via KnowBe4 + vendor | AppSec Team | Week 30 | CLOSED |

### PHYSICAL SECURITY RISKS

| Risk ID | Risk Title | Threat Source | Vulnerability | Likelihood | Impact | Score | Rating | Treatment | Owner | Target Date | Status |
|---------|-----------|--------------|--------------|-----------|--------|-------|--------|-----------|-------|-------------|--------|
| RSK-022 | Data center physical access control gaps | Physical threat, Insider | Badge reader log review found 3 unauthorized entries | 2 | 4 | 8 | Medium | Mitigate — Access review + biometric upgrade | Facilities | Week 32 | CLOSED |
| RSK-030 | Server room clean desk policy not enforced | Insider | Post-it notes with credentials found during audit | 2 | 3 | 6 | Low | Mitigate — Clean desk policy + awareness training | Facilities/HR | Week 26 | CLOSED |
| RSK-049 | No CCTV in server rooms | Physical threat | Server rooms lack video surveillance | 1 | 4 | 4 | Low | Accept — Cost-benefit: budget for Year 2 | Facilities | Year 2 | ACCEPTED |

### COMPLIANCE / REGULATORY RISKS

| Risk ID | Risk Title | Threat Source | Vulnerability | Likelihood | Impact | Score | Rating | Treatment | Owner | Target Date | Status |
|---------|-----------|--------------|--------------|-----------|--------|-------|--------|-----------|-------|-------------|--------|
| RSK-050 | FFIEC examination findings — inadequate maturity | Regulatory | FFIEC CAT Baseline maturity; exam scheduled Q3 | 4 | 4 | 16 | High | Mitigate — Full GRC program (this project) | CISO/Compliance | Week 52 | CLOSED |
| RSK-047b | GLBA Safeguards Rule non-compliance elements | Regulatory | 3 GLBA required elements not fully implemented | 3 | 4 | 12 | Medium | Mitigate — Policies + controls addressing GLBA gaps | Compliance | Week 26 | CLOSED |

---

## Risk Register Summary

| Rating | Total Risks | Closed | Open | Accepted |
|--------|------------|--------|------|---------|
| Critical | 3 | 3 | 0 | 0 |
| High | 11 | 11 | 0 | 0 |
| Medium | 27 | 27 | 0 | 0 |
| Low | 6 | 4 | 0 | 2 |
| **Total** | **47** | **45** | **0** | **2** |

*2 accepted risks: RSK-037 (fourth-party visibility) and RSK-049 (CCTV in server rooms) — both documented and tracked.*

---

*TechNova Financial Services, Inc. | NIST CSF 2.0 GRC Project — Risk Register v1.0*
*Project Lead: Venkata Bharath Kasyap Devulapalli*
*Risk Committee Approved: Week 11*
