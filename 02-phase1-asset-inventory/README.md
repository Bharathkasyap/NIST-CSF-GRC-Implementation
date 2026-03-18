# 02-Phase1-Asset-Inventory — Asset Inventory & Scoping

## Overview
Phase 1 establishes the complete asset inventory and scope boundary for the NIST CSF 2.0 assessment at TechNova Financial Services. This phase ran **Weeks 3–6** and produced the foundational data required for all subsequent phases.

## Key Deliverables

| File | Description |
|------|-------------|
| `asset-inventory.md` | Complete 275-system asset inventory with classification |
| `business-impact-analysis.md` | BIA for critical business processes and supporting systems |
| `vendor-third-party-register.md` | Third-party/vendor risk register with 47 vendors |
| `network-topology-summary.md` | High-level network segmentation and boundary diagram notes |
| `data-classification-matrix.md` | Data types, sensitivity levels, and handling requirements |
| `scope-statement.md` | Formal scope definition and exclusion rationale |

## Asset Summary

### By System Category

| Category | Count | Criticality |
|----------|-------|-------------|
| Core Banking Systems | 12 | Critical |
| Payment Processing | 8 | Critical |
| Customer Portal / Web | 15 | High |
| Internal Applications | 47 | High–Medium |
| Database Servers | 34 | Critical–High |
| Network Infrastructure | 61 | High |
| Endpoint Devices | 82 | Medium |
| Cloud Services (SaaS/IaaS) | 16 | High |
| **Total** | **275** | |

### By Data Classification

| Classification | Description | Systems Count |
|---------------|-------------|---------------|
| Restricted | PII, PCI-DSS data, credentials | 48 |
| Confidential | Internal business data, audit logs | 97 |
| Internal | General business operations data | 103 |
| Public | Marketing, public-facing content | 27 |

## Business Impact Analysis Summary

### Mission-Critical Processes

| Process | RTO | RPO | Supporting Systems |
|---------|-----|-----|--------------------|
| Core Banking Operations | 4 hours | 15 minutes | CBS-01 through CBS-12 |
| Payment Processing | 2 hours | 0 minutes | PAY-01 through PAY-08 |
| Customer Authentication | 1 hour | 30 minutes | IDM-01, IDM-02 |
| Fraud Detection | 30 minutes | 5 minutes | FRD-01 |
| Regulatory Reporting | 24 hours | 1 hour | RPT-01 through RPT-05 |

### High-Impact Processes

| Process | RTO | RPO |
|---------|-----|-----|
| Internal Banking Portal | 8 hours | 1 hour |
| HR / Payroll Systems | 24 hours | 4 hours |
| Email / Communications | 4 hours | 1 hour |

## Third-Party Vendor Summary

| Risk Tier | Vendor Count | Review Frequency |
|-----------|-------------|-----------------|
| Tier 1 (Critical) | 8 | Quarterly |
| Tier 2 (High) | 19 | Semi-annual |
| Tier 3 (Medium) | 20 | Annual |
| **Total** | **47** | |

**Top Tier 1 Vendors:** Core banking platform provider, payment network processor, cloud hosting (AWS/Azure), identity provider (Okta), SIEM provider (Microsoft Sentinel), cybersecurity monitoring (Managed SOC).

## Methodology

1. **Discovery** — Automated discovery via Nessus + Qualys scanning across all network segments
2. **Manual Enumeration** — IT asset management system (ServiceNow CMDB) reconciliation
3. **Business Owner Validation** — Interviews with 18 business unit owners to confirm criticality ratings
4. **BIA Workshops** — Four workshops with operations, IT, and risk teams
5. **Vendor Review** — Third-party contracts and security assessments reviewed

## Phase 1 Completion Criteria — All Met ✅

- [x] 100% of in-scope systems catalogued (275 systems)
- [x] Business impact analysis completed for all critical processes
- [x] Data classification applied to all asset categories
- [x] Network boundaries and segmentation documented
- [x] Vendor register populated with risk tier assignments
- [x] Scope statement approved by CISO and Steering Committee

---
*TechNova Financial Services, Inc. | NIST CSF 2.0 GRC Project — Phase 1*
*Duration: Weeks 3–6 | Project Lead: Venkata Bharath Kasyap Devulapalli*
