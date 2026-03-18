# 03-Phase2-Risk-Assessment — Risk Assessment

## Overview
Phase 2 delivers a comprehensive risk assessment for TechNova Financial Services using the NIST SP 800-30 methodology, supplemented with FAIR (Factor Analysis of Information Risk) quantitative analysis. This phase ran **Weeks 7–11**.

## Key Deliverables

| File | Description |
|------|-------------|
| risk-register.md | Full risk register — 47 identified risks |
| nist-800-30-risk-assessment-report.md | Formal NIST SP 800-30 risk assessment report |
| fair-quantitative-analysis.md | FAIR analysis for top 10 critical risks |
| threat-catalog.md | Threat source and event catalog |
| vulnerability-summary.md | Nessus/Qualys scan findings — 106 critical/high CVEs |
| risk-scoring-methodology.md | Likelihood x Impact scoring guide |

## Risk Register Summary

### Risk Distribution by Category

| Risk Category | Count | Critical | High | Medium | Low |
|---------------|-------|----------|------|--------|-----|
| Access Control | 8 | 3 | 4 | 1 | 0 |
| Data Protection | 7 | 2 | 3 | 2 | 0 |
| Third-Party / Supply Chain | 6 | 1 | 3 | 2 | 0 |
| Network Security | 9 | 2 | 5 | 2 | 0 |
| Incident Response | 5 | 2 | 2 | 1 | 0 |
| Application Security | 7 | 1 | 4 | 2 | 0 |
| Physical Security | 3 | 0 | 1 | 1 | 1 |
| Compliance / Regulatory | 2 | 0 | 2 | 0 | 0 |
| **Total** | **47** | **11** | **24** | **11** | **1** |

### Top 10 Critical Risks

| Risk ID | Risk Description | Likelihood | Impact | Risk Score | Owner |
|---------|-----------------|------------|--------|-----------|-------|
| RSK-001 | Privileged account compromise via weak MFA | High | Critical | 20 | IAM Team |
| RSK-002 | Ransomware attack on core banking systems | Medium | Critical | 18 | SOC Team |
| RSK-003 | SQL injection in customer portal | High | High | 16 | AppSec Team |
| RSK-004 | Unpatched critical CVEs (106 open) | High | High | 16 | Patching Team |
| RSK-005 | Third-party data breach (Tier 1 vendor) | Medium | Critical | 18 | Vendor Mgmt |
| RSK-006 | Insider threat data exfiltration | Medium | High | 14 | DLP / HR |
| RSK-007 | Phishing leading to credential theft | High | High | 16 | Security Awareness |
| RSK-008 | Missing encryption on data at rest | Medium | High | 14 | Data Protection |
| RSK-009 | No documented IR playbooks for ransomware | High | Critical | 20 | IR Team |
| RSK-010 | Lack of network segmentation in legacy systems | Medium | High | 14 | Network Team |

## FAIR Quantitative Analysis Summary

| Risk | Annualized Loss Expectancy (ALE) | Confidence Interval |
|------|----------------------------------|---------------------|
| RSK-001: Privileged account compromise | $4.2M - $8.7M | 90% |
| RSK-002: Ransomware attack | $6.8M - $22.4M | 85% |
| RSK-005: Third-party breach | $3.1M - $9.6M | 80% |
| RSK-003: SQL injection breach | $1.8M - $5.2M | 85% |
| RSK-007: Phishing/credential theft | $2.2M - $6.1M | 90% |

**Total estimated annual cyber risk exposure: $18.1M - $52.0M**

## Vulnerability Assessment Summary

| Severity | Count (Baseline) | Systems Affected | CVSS Score Range |
|----------|-----------------|-----------------|-----------------|
| Critical | 31 | 47 systems | 9.0-10.0 |
| High | 75 | 89 systems | 7.0-8.9 |
| Medium | 142 | 124 systems | 4.0-6.9 |
| Low | 214 | 163 systems | 0.1-3.9 |

**Tools Used:** Nessus Professional, Qualys VMDR, manual penetration testing (external)

## Risk Treatment Decisions

| Treatment | Risk Count | Description |
|-----------|------------|-------------|
| Mitigate | 38 | Implement controls to reduce likelihood/impact |
| Accept | 4 | Risk within tolerance; documented and monitored |
| Transfer | 3 | Cyber insurance / contractual transfer |
| Avoid | 2 | Eliminate risky business process/technology |

## Phase 2 Completion Criteria - All Met

- [x] Risk register with 47 risks documented and rated
- [x] NIST SP 800-30 formal assessment report completed
- [x] FAIR quantitative analysis for top 10 risks
- [x] Vulnerability scan results integrated into risk register
- [x] Risk treatment decisions made by Risk Committee
- [x] Report approved by CISO and Risk Committee

---
*TechNova Financial Services, Inc. | NIST CSF 2.0 GRC Project - Phase 2*
*Duration: Weeks 7-11 | Project Lead: Venkata Bharath Kasyap Devulapalli*
