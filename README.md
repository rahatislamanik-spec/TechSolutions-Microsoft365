# TechSolutions Inc. — Microsoft 365 Enterprise Deployment

### One Tenant. Every Layer. Built End to End in a Live M365 Environment.

**Md Rahat Islam Anik · Self-Directed Case Study · 2025**

[![Live Case Study](https://img.shields.io/badge/Live%20Case%20Study-View%20Now-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)](https://rahatislamanik-spec.github.io/TechSolutions-Microsoft365/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-rahatislamanik-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/rahatislamanik)
[![GitHub](https://img.shields.io/badge/GitHub-rahatislamanik--spec-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/rahatislamanik-spec)

---

| 300 Employees Onboarded | 3 Departments Configured | M365 E5 Deployed | 4 Phases | 0 Data Breaches Undetected |
|:---:|:---:|:---:|:---:|:---:|

---

## The Brief

TechSolutions Inc. was moving 300 employees to Microsoft 365 and needed it done right — not just functional, but secure, compliant, and built to scale. This is the complete deployment story: identity, security, collaboration, and monitoring, configured end to end inside a **live Microsoft 365 tenant**.

Every configuration in this case study was applied to a real tenant. Every screenshot is live verification. This is not a simulation.

---

## Tech Stack

`Microsoft Entra ID` · `Exchange Online` · `SharePoint Online` · `OneDrive for Business` · `Microsoft Defender for Office 365` · `Microsoft Purview` · `DLP` · `Insider Risk Management` · `Adaptive Protection` · `Viva Engage` · `Power Automate` · `Microsoft Graph API` · `Microsoft Secure Score` · `Service Health`

---

## Phase 01 — Identity & Onboarding

> **Building the Foundation** · Bulk onboarding · E5 licensing · M365 Groups · SharePoint permissions

Before a single email is sent or a document shared, the right people need to be in the right places with the right access. Phase 01 established TechSolutions' identity layer from the ground up.

**Bulk User Onboarding via CSV**
300 employees across three departments — IT, HR, and Marketing — were onboarded via structured CSV import through the Microsoft 365 Admin Center. Each account was provisioned with correct UPN, display name, department, and country metadata in a single operation. At scale, manual account creation isn't an option. Bulk CSV import is how enterprise IT teams handle real onboarding — repeatable, auditable, and error-resistant.

**Microsoft 365 E5 Licensing**
Every account was assigned an M365 E5 license — the highest tier, unlocking Defender, Purview, Power Automate, and the full compliance stack. Profile pictures were standardized with the TechSolutions company logo across Admin Center, Teams, and Outlook. Department fields, job titles, and contact information were populated tenant-wide.

**Microsoft 365 Groups — Department Structure + Master Group**
Four M365 Groups were created and configured:

```
TechSolutions-IT        → IT department members
TechSolutions-HR        → HR department members
TechSolutions-Marketing → Marketing department members
TechSolutions-All       → All 300 users, tenant-wide communications
```

Each group creation automatically provisions a shared mailbox, SharePoint site, Teams workspace, and Planner — one action, five connected services.

**SharePoint Permissions & Teams Access**
Permissions were configured at group level. The HR group received Full Control on the HR SharePoint site (with Edit-level access for members), and access denial was verified for unauthorized users. The Marketing group was granted rights to create and manage Teams workspaces — confirmed by provisioning a Marketing team and adding all Marketing members.

---

## Phase 02 — Security & Data Protection

> **Locking the Perimeter** · Defender · OME Encryption · DLP · Insider Risk · Adaptive Protection

An M365 tenant without hardened security is an open door. Phase 02 covered every threat surface: email-borne attacks, phishing, malware, unauthorized data exfiltration, and internal data leaks.

**Microsoft Defender for Office 365 — Safe Links & Safe Attachments**
Safe Links and Safe Attachments were enabled under Preset Security Policies (Standard and Strict), applied to all inbound email. Safe Links rewrites every URL at time-of-click against Microsoft's threat intelligence database in real time. Safe Attachments detonates suspicious files in a sandbox before delivery. Extended protection was configured across Teams and Office 365 Apps with click-tracking enabled.

**Anti-Phishing — Mailbox Intelligence & Spoof Protection**
Anti-phishing was configured through Defender's Threat Policies. Mailbox intelligence and spoof intelligence were both enabled, allowing Defender to learn normal sending patterns and flag anomalies. Phishing threshold set to Standard. Zero impersonated domains or users detected in the 7-day post-configuration window — confirming a clean baseline.

**Microsoft 365 Message Encryption — Automatic Internal Email Encryption**
A mail flow rule was configured in the Exchange Admin Center to automatically apply Microsoft 365 Message Encryption (OME) to all internal-to-internal emails. The rule — *"Encrypt All Internal Emails"* — was enabled and confirmed active. Every communication between TechSolutions employees is encrypted in transit with no action required from the sender.

**Data Loss Prevention — Canadian PII & Financial Data**
Two DLP policies were created in Microsoft Purview targeting the highest-risk data types for a Canadian organization:

- **Canadian PII policy** — Social insurance numbers, health card numbers, and personal identifiers
- **Financial data policy** — Credit card numbers and banking data

Both policies were set to active and live-tested. An email containing test credit card data immediately triggered a high-severity DLP alert in Microsoft Purview, with a `DlpRuleMatch` event logged in the audit trail — real-time detection confirmed.

**Insider Risk Management & Adaptive Protection**
A Data Leaks quick policy was deployed in Microsoft Purview covering all active users, with DLP policies integrated as policy indicators. Adaptive Protection was enabled to dynamically tighten Conditional Access controls based on user risk score — automatically restricting Office app access for elevated-risk users without manual admin intervention. This is risk-based security that responds to behaviour, not just policy.

**Microsoft Secure Score — Baseline Review**
The Secure Score dashboard was reviewed post-configuration to assess TechSolutions' overall security posture. The score reflected the cumulative effect of all protections deployed across identity, data, and collaboration — with recommended improvement actions flagged for ongoing hardening.

---

## Phase 03 — Collaboration & Governance

> **Building the Workspace** · SharePoint · OneDrive · Viva Engage · Document Lifecycle

Productivity without structure creates chaos. Phase 03 stood up the full collaboration infrastructure with the right permissions, retention rules, and governance controls across every service.

**SharePoint Online — Departmental Sites & Permission Tiers**
Three dedicated SharePoint team sites were provisioned — TechSolutions IT, HR, and Marketing. Each site has its own permission structure:

| Site | Owners | Members | External |
|---|---|---|---|
| IT | Full Control | Edit | Locked |
| HR | Full Control | Edit only | Locked |
| Marketing | Full Control | Edit | Locked |

The HR site is the most restrictive — access denied response verified for any user outside the HR group attempting to browse.

**HR Document Library — Versioning & Content Approval**
A dedicated HR Documents Library was configured with two critical governance controls:

- **Document versioning** — full edit history preserved for every HR document
- **Content approval** — HR owners must approve any new or modified document before it becomes visible to members
- **Draft item security** — draft visibility restricted to authors and approvers only

**OneDrive for Business — External Sharing Restriction & Retention Policies**
Organization-wide OneDrive external sharing was locked to *"Only people in your organization"* — no file can leave the tenant without admin authorization. Two retention policies were applied:

- **5-year retention policy** — all OneDrive files retained for long-term compliance
- **1-year deletion policy** — stale files automatically moved to Recycle Bin after 12 months of inactivity

**Viva Engage — Internal-Only Communities**
Viva Engage was configured as TechSolutions' enterprise social network with a strict internal-only policy — all activity restricted to authenticated tenant users only. Four communities were created and confirmed:

```
Company-Wide Announcements  → All 300 users
TechSolutions-IT            → IT department
TechSolutions-HR            → HR department
TechSolutions-Marketing     → Marketing department
```

Internal-only policy saved and verified with confirmation banner.

---

## Phase 04 — Monitoring & Automation

> **Keeping the Lights On** · Audit Logs · Alert Policies · Service Health · Power Automate

A deployed environment without visibility is a liability. Phase 04 instrumented the entire TechSolutions tenant so IT administrators can see everything that matters without having to look for it.

**Audit Logging — Custom Search in Microsoft Purview**
Audit logging was enabled across the tenant. A custom audit log search was configured to track SharePoint file activity — access, uploads, edits, and deletions — for specific users within defined date ranges. This gives IT administrators the ability to reconstruct any user action in SharePoint and meet the forensic requirements of a compliance investigation.

**Alert Policies — Suspicious Activity & DLP Breach Notifications**
A Suspicious File Activity alert policy was created to notify administrators when anomalous file access patterns are detected. Separate DLP breach notifications were configured to fire on every DLP policy match. Alert coverage configured:

- Multiple failed login attempts
- Mass file deletion
- DLP policy breaches
- High-severity insider risk events
- Unresolved policy warnings

Severity, threshold, and recipient list configured and policy confirmed active.

**Power Automate — Automated Monthly Usage Reports via Microsoft Graph API**
A scheduled Power Automate cloud flow was built and deployed to automatically generate and deliver monthly M365 usage reports to IT administrators and department heads. The flow:

1. Runs on monthly recurrence
2. Retrieves the previous 30 days of activity via **Microsoft Graph API**
3. Formats the data as CSV
4. Emails the report to the distribution list

Coverage: email activity, SharePoint usage, and security events. Flow tested and confirmed active.

**Service Health Monitoring**
Service Health email alerts were enabled to automatically notify administrators of any M365 service incidents, advisories, or degradations. All services confirmed healthy post-deployment: Exchange Online, OneDrive, SharePoint, Teams, and Viva Engage. IT department team members were added as additional notification recipients alongside the global admin — no incident goes unnoticed.

**Final Secure Score Review**
With all four phases complete, the Secure Score dashboard was reviewed as the final validation checkpoint. The score reflects the cumulative effect of every security configuration applied across identity, data, email, and collaboration — confirming TechSolutions' tenant is hardened against the most common threat categories facing a mid-sized Canadian organization.

---

## Skills Demonstrated

| Domain | What Was Configured |
|---|---|
| **Identity & Access** | Bulk user onboarding, M365 Groups, RBAC, SharePoint permission tiers, Entra ID |
| **Email Security** | Safe Links, Safe Attachments, Anti-Phishing, OME encryption, Exchange mail flow rules |
| **Data Loss Prevention** | Canadian PII policies, credit card detection, live alert verification, DLP-IRM integration |
| **Compliance & Governance** | Retention policies, content approval, document versioning, audit log search, Purview |
| **Insider Risk** | Data leaks policy, Adaptive Protection, Conditional Access integration, risk-based controls |
| **Collaboration Tools** | SharePoint Online, OneDrive governance, Viva Engage communities, Microsoft Teams |
| **Automation** | Power Automate scheduled flows, Microsoft Graph API, automated reporting pipelines |
| **Monitoring** | Custom audit searches, alert policies, service health monitoring, Secure Score tracking |

---

## What's Next — Phase 05 Roadmap

The foundation is in place. These are the logical next steps to complete TechSolutions' information protection framework:

**Sensitivity Labels** — Apply Public, Internal, Confidential, and Highly Confidential labels across documents and emails. Auto-labelling policies to classify HR and financial data without user action.

**Microsoft Entra PIM** — Privileged Identity Management for just-in-time admin role activation. Global Administrator access time-bound and approval-gated — least privilege enforced at the highest level.

**Microsoft Intune** — Enroll TechSolutions endpoints into Intune. Deploy compliance policies, app protection policies, and Defender for Endpoint across all managed devices.

---

## Live Case Study

The full interactive case study — with phase-by-phase documentation and live-tenant screenshots — is published at:

**[rahatislamanik-spec.github.io/TechSolutions-Microsoft365](https://rahatislamanik-spec.github.io/TechSolutions-Microsoft365/)**

---

> *Every screenshot in this case study was taken from a real Microsoft 365 tenant with real configurations applied. TechSolutions' environment was designed, deployed, secured, and instrumented — end to end — by one administrator.*

---

## Author

**Md Rahat Islam Anik**
Cloud Computing & Network Administration · George Brown College · May 2026

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat&logo=linkedin)](https://linkedin.com/in/rahatislamanik)
[![GitHub](https://img.shields.io/badge/GitHub-Portfolio-181717?style=flat&logo=github)](https://github.com/rahatislamanik-spec)
