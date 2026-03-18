# 05-Phase4-Policies-Controls — Security Policies & Controls

## Overview
Phase 4 develops and formalizes the complete security policy library and controls matrix for TechNova Financial Services. This phase delivered 14 approved security policies and a comprehensive controls mapping to NIST CSF 2.0, NIST SP 800-53, and applicable financial regulations. This phase ran **Weeks 17–26**.

## Key Deliverables

| File | Description |
|------|-------------|
| policy-01-information-security.md | Information Security Policy |
| policy-02-acceptable-use.md | Acceptable Use Policy |
| policy-03-access-control.md | Access Control Policy |
| policy-04-data-classification.md | Data Classification and Handling Policy |
| policy-05-incident-response.md | Incident Response Policy |
| policy-06-business-continuity.md | Business Continuity & Disaster Recovery Policy |
| policy-07-vulnerability-management.md | Vulnerability Management Policy |
| policy-08-change-management.md | Change Management Policy |
| policy-09-third-party-risk.md | Third-Party Risk Management Policy |
| policy-10-encryption.md | Encryption and Key Management Policy |
| policy-11-network-security.md | Network Security Policy |
| policy-12-physical-security.md | Physical Security Policy |
| policy-13-security-awareness.md | Security Awareness and Training Policy |
| policy-14-audit-logging.md | Audit Logging and Monitoring Policy |
| controls-matrix.md | Full controls matrix mapped to NIST CSF 2.0 and NIST 800-53 |
| policy-exception-process.md | Policy exception request and approval process |

## Security Policy Summary

| # | Policy Name | Owner | Approved | Review Cycle | NIST CSF Functions |
|---|-------------|-------|----------|-------------|-------------------|
| 1 | Information Security Policy | CISO | Week 22 | Annual | All |
| 2 | Acceptable Use Policy | CISO | Week 22 | Annual | PR, GV |
| 3 | Access Control Policy | IAM Lead | Week 22 | Annual | PR.AA |
| 4 | Data Classification Policy | Data Owner | Week 23 | Annual | PR.DS, ID.AM |
| 5 | Incident Response Policy | IR Lead | Week 23 | Annual | RS, DE |
| 6 | BCP/DR Policy | BCP Lead | Week 24 | Annual | RC |
| 7 | Vulnerability Management Policy | SecOps Lead | Week 24 | Annual | ID.RA, PR.PS |
| 8 | Change Management Policy | IT Operations | Week 24 | Annual | PR.PS |
| 9 | Third-Party Risk Policy | Vendor Mgmt | Week 25 | Annual | GV.SC, ID.AM |
| 10 | Encryption Policy | Data Owner | Week 25 | Annual | PR.DS |
| 11 | Network Security Policy | Network Lead | Week 25 | Annual | PR.IR |
| 12 | Physical Security Policy | Facilities | Week 26 | Annual | PR.AA |
| 13 | Security Awareness Policy | HR/CISO | Week 26 | Annual | PR.AT |
| 14 | Audit Logging Policy | SOC Lead | Week 26 | Annual | DE, PR.PS |

## Controls Matrix Summary

### NIST CSF 2.0 to NIST SP 800-53 Rev. 5 Mapping

| NIST CSF Category | Key Controls Implemented | NIST 800-53 Controls | Status |
|------------------|------------------------|---------------------|--------|
| PR.AA (Identity Mgmt) | MFA, PAM, RBAC, SSO | AC-2, AC-3, IA-2, IA-5, IA-8 | Implemented |
| PR.AT (Awareness) | KnowBe4 training, phishing sims | AT-2, AT-3 | Implemented |
| PR.DS (Data Security) | Encryption at rest/transit, DLP | SC-8, SC-28, SI-12 | Implemented |
| PR.IR (Network Security) | Firewall, IDS/IPS, segmentation | SC-7, CA-3, SI-3 | Implemented |
| PR.PS (Platform Security) | Patch mgmt, config baselines | SI-2, CM-2, CM-6 | Implemented |
| DE.AE (Anomaly Detection) | SIEM alerting, behavioral analytics | AU-6, SI-4 | Implemented |
| DE.CM (Monitoring) | SOC 24/7, SIEM, endpoint monitoring | AU-2, SI-4, CA-7 | Implemented |
| RS.MA (Incident Mgmt) | 12 IR playbooks, SOAR integration | IR-4, IR-5, IR-8 | Implemented |
| RS.CO (Communication) | Runbooks, escalation matrix | IR-6, CP-2 | Implemented |
| RC.RP (Recovery) | DR plan, backup testing | CP-10, CP-9 | Implemented |
| ID.AM (Asset Mgmt) | CMDB, software inventory | CM-8, SA-9 | Implemented |
| ID.RA (Risk Assessment) | Vulnerability scanning, threat intel | RA-3, RA-5 | Implemented |
| GV.RM (Risk Mgmt) | Risk committee, risk register | PM-9, RA-2 | Implemented |
| GV.SC (Supply Chain) | Vendor assessments, contract standards | SR-3, SR-5 | Implemented |

### Regulatory Compliance Mapping

| Policy / Control Area | SOC 2 | PCI DSS | GLBA | FFIEC | NY SHIELD |
|----------------------|-------|---------|------|-------|----------|
| Access Control | CC6.1–6.3 | Req 7, 8 | Yes | Yes | Yes |
| Data Encryption | CC6.7 | Req 3, 4 | Yes | Yes | Yes |
| Incident Response | CC7.3–7.5 | Req 12.10 | Yes | Yes | Yes |
| Change Management | CC8.1 | Req 6 | Yes | Yes | No |
| Vulnerability Mgmt | CC7.1 | Req 6.3 | No | Yes | Yes |
| Security Awareness | CC9.2 | Req 12.6 | Yes | Yes | Yes |
| Vendor Management | CC9.2 | Req 12.8 | Yes | Yes | Yes |
| Audit Logging | CC7.2 | Req 10 | Yes | Yes | Yes |

## Policy Governance

All policies follow this lifecycle:
1. **Draft** — Policy owner drafts based on framework requirements
2. **Review** — Legal, Compliance, IT Security review and comment
3. **Approval** — CISO approval required; Board approval for top 3 policies
4. **Publication** — Posted to intranet; mandatory employee acknowledgment
5. **Training** — Relevant training created and assigned in KnowBe4
6. **Review** — Annual review cycle with change management process

## Phase 4 Completion Criteria — All Met

- [x] 14 security policies drafted, reviewed, and approved
- [x] All policies published and employee acknowledgment collected (97% completion)
- [x] Controls matrix mapped to NIST CSF 2.0, NIST 800-53, and regulatory requirements
- [x] Policy training delivered via KnowBe4
- [x] Exception process documented and operationalized
- [x] Board-level policies approved by Board Security Committee

---
*TechNova Financial Services, Inc. | NIST CSF 2.0 GRC Project - Phase 4*
*Duration: Weeks 17-26 | Project Lead: Venkata Bharath Kasyap Devulapalli*
