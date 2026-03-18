# Templates — Reusable GRC Templates

## Overview
This folder contains reusable templates for all major GRC artifact types used throughout the NIST CSF 2.0 implementation project at TechNova Financial Services. These templates are designed to be adapted for other organizations implementing NIST CSF.

## Available Templates

### Project Management

| Template | Description | Use Case |
|----------|-------------|----------|
| project-charter-template.md | Project charter with all standard sections | New GRC projects |
| raci-matrix-template.md | RACI responsibility assignment matrix | Project initiation |
| communication-plan-template.md | Stakeholder communication plan | Project initiation |
| meeting-notes-template.md | Standard meeting notes format | All meetings |
| phase-gate-review-template.md | Phase gate review checklist | Phase completion |

### Risk Management

| Template | Description | Use Case |
|----------|-------------|----------|
| risk-register-template.md | Risk register with scoring fields | Risk tracking |
| risk-assessment-template.md | NIST 800-30 risk assessment template | Risk assessments |
| fair-analysis-template.md | FAIR quantitative risk analysis template | Risk quantification |
| risk-treatment-plan-template.md | Risk treatment plan with action tracking | Risk remediation |

### Asset Management

| Template | Description | Use Case |
|----------|-------------|----------|
| asset-inventory-template.md | Asset inventory with classification fields | Asset management |
| bia-template.md | Business impact analysis template | BIA workshops |
| vendor-register-template.md | Third-party vendor risk register | Vendor management |
| data-classification-template.md | Data classification decision matrix | Data governance |

### Gap Analysis & Controls

| Template | Description | Use Case |
|----------|-------------|----------|
| nist-csf-gap-analysis-template.md | 106-subcategory gap analysis spreadsheet | CSF assessments |
| controls-matrix-template.md | Controls-to-framework mapping template | Control documentation |
| remediation-roadmap-template.md | Prioritized remediation roadmap | Control gap remediation |
| maturity-scoring-guide.md | NIST CSF maturity scoring guidance | Maturity assessments |

### Policy & Procedure

| Template | Description | Use Case |
|----------|-------------|----------|
| security-policy-template.md | Standard security policy format | Policy development |
| policy-exception-template.md | Policy exception request form | Exception management |
| procedure-template.md | Standard operating procedure template | Procedure documentation |
| standard-template.md | Technical security standard template | Standards development |

### Incident Response

| Template | Description | Use Case |
|----------|-------------|----------|
| ir-playbook-template.md | Incident response playbook template | Playbook development |
| incident-report-template.md | Post-incident report template | Incident documentation |
| tabletop-exercise-template.md | Tabletop exercise scenario template | IR testing |
| lessons-learned-template.md | Lessons learned capture template | Continuous improvement |

### Reporting

| Template | Description | Use Case |
|----------|-------------|----------|
| executive-dashboard-template.md | Executive security dashboard | Board/C-suite reporting |
| board-report-template.md | Board security committee report | Quarterly board updates |
| kpi-metrics-template.md | Security KPI tracking template | Ongoing metrics |
| audit-report-template.md | Security audit report template | Audit findings |
| vendor-assessment-template.md | Third-party security assessment | Vendor reviews |

## Template Usage Guidelines

### How to Use These Templates

1. **Select the appropriate template** for your use case from the table above
2. **Copy the template file** to the relevant phase folder
3. **Rename the file** to reflect the specific artifact (e.g., `risk-register-2026.md`)
4. **Replace placeholder text** — all placeholder text is marked with `[BRACKETS]`
5. **Adapt the template** to your organization's specific requirements
6. **Remove template notes** (marked with `<!-- TEMPLATE NOTE: -->`) before finalizing

### Template Variables Reference

When adapting templates, replace these common variables:

| Variable | Replace With |
|----------|-------------|
| [ORGANIZATION] | Your organization name |
| [DATE] | Current date |
| [OWNER] | Document owner name/role |
| [REVIEWER] | Reviewer name/role |
| [APPROVER] | Approver name/role |
| [VERSION] | Document version number |
| [FRAMEWORK] | Applicable framework (e.g., NIST CSF 2.0) |

### Template Versioning

All templates follow semantic versioning (MAJOR.MINOR.PATCH):
- **MAJOR** — Breaking change to template structure
- **MINOR** — New sections added, backward compatible
- **PATCH** — Minor corrections or clarifications

Current template version: **1.0.0**
Last reviewed: March 2026

## NIST CSF 2.0 Quick Reference

| CSF Function | Core Categories | Key Subcategories |
|-------------|----------------|-------------------|
| **GOVERN (GV)** | Organizational Context, Risk Strategy, Roles, Policy, Oversight, Supply Chain | GV.OC, GV.RM, GV.RR, GV.PO, GV.OV, GV.SC |
| **IDENTIFY (ID)** | Asset Mgmt, Risk Assessment, Improvement | ID.AM, ID.RA, ID.IM |
| **PROTECT (PR)** | Identity Mgmt, Awareness, Data Security, Platform Security, Infrastructure | PR.AA, PR.AT, PR.DS, PR.PS, PR.IR |
| **DETECT (DE)** | Monitoring, Adverse Events | DE.CM, DE.AE |
| **RESPOND (RS)** | Incident Mgmt, Incident Analysis, Reporting, Mitigation | RS.MA, RS.AN, RS.CO, RS.MI |
| **RECOVER (RC)** | Recovery Planning, Communication | RC.RP, RC.CO |

## Contributing

To contribute a new template or improve an existing one:
1. Create the template in this folder following the naming convention `[type]-template.md`
2. Add an entry in this README's template table
3. Include the template version and date in the file header
4. Submit via pull request with a description of the template purpose

---
*TechNova Financial Services, Inc. | NIST CSF 2.0 GRC Project*
*Template Library Version: 1.0.0 | Maintained by: Venkata Bharath Kasyap Devulapalli*
