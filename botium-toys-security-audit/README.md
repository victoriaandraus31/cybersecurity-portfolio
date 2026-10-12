# Botium Toys – Internal Security Audit

> Fictional scenario from the **Google Cybersecurity Professional Certificate** (Course 2: *Play It Safe: Manage Security Risks*).

## Scenario

Botium Toys is a small U.S. toy company with a single physical location (office, storefront and warehouse) and a growing online store serving customers in the U.S. and abroad, including the European Union. The IT manager requested an internal IT audit to identify risks, threats and vulnerabilities to critical assets and to check compliance with regulations related to online payments and doing business in the E.U.

The audit is based on the **NIST Cybersecurity Framework (CSF)**. I reviewed the scope, goals and risk assessment report, then completed a **controls and compliance checklist**.

## Scope

- Assets managed by the IT department: on-premises equipment, employee devices (desktops, laptops, smartphones), POS systems, storefront products, systems and software (accounting, telecommunications, database, security, e-commerce, inventory), internet access, internal network, data retention and storage, and legacy system maintenance.
- Current user permissions, implemented controls, procedures and protocols.
- Alignment with **PCI DSS**, **GDPR** and **SOC 1 / SOC 2** requirements.

## Goals

- Adhere to the NIST CSF.
- Establish a better process for systems to stay compliant.
- Fortify system controls.
- Apply the principle of least privilege to user credential management.
- Establish policies and procedures, including playbooks.
- Ensure the company meets compliance requirements.

## Key findings from the risk assessment

- Assets are managed by IT but are **not properly inventoried or classified**.
- **All employees** can access internally stored data, including cardholder data and customer PII/SPII.
- Customer credit card data is **not encrypted**.
- **Least privilege** and **separation of duties** are not implemented.
- A firewall with defined rules and regularly monitored antivirus software are in place.
- **No intrusion detection system (IDS)**.
- **No disaster recovery plan** and **no backups** of critical data.
- A plan exists to notify E.U. customers within **72 hours** of a breach; privacy policies are documented and enforced.
- The password policy is **weak** (below current complexity standards) and there is **no centralized password management system**.
- Legacy systems are monitored, but **without a regular schedule** or clear intervention methods.
- Physical security is adequate: locks, up-to-date CCTV, and fire detection/prevention.

**Risk score: 8/10 (high)** — mainly due to missing controls and non-compliance with regulations.

---

## Controls assessment checklist

Does Botium Toys currently have this control in place?

| Control | In place? | Type | Notes |
|---|:---:|---|---|
| Least privilege | ❌ No | Administrative / Preventive | All employees can access customer data. |
| Disaster recovery plans | ❌ No | Administrative / Corrective | No DRP exists. |
| Password policies | ❌ No | Administrative / Preventive | Policy exists but is below current complexity requirements. |
| Separation of duties | ❌ No | Administrative / Preventive | Not implemented. |
| Firewall | ✅ Yes | Technical / Preventive | Blocks traffic based on defined rules. |
| Intrusion detection system (IDS) | ❌ No | Technical / Detective | Not installed. |
| Backups | ❌ No | Technical / Corrective | No backups of critical data. |
| Antivirus software | ✅ Yes | Technical / Preventive & Corrective | Installed and monitored regularly. |
| Manual monitoring, maintenance and intervention for legacy systems | ❌ No | Technical / Preventive | Monitored, but no regular schedule or defined procedures. |
| Encryption | ❌ No | Technical / Deterrent | Credit card data is not encrypted. |
| Password management system | ❌ No | Technical / Corrective | No centralized system. |
| Locks (offices, storefront, warehouse) | ✅ Yes | Physical / Preventive | Sufficient locks in place. |
| Closed-circuit television (CCTV) surveillance | ✅ Yes | Physical / Preventive & Detective | Up to date. |
| Fire detection/prevention (alarm, sprinklers, etc.) | ✅ Yes | Physical / Detective & Preventive | Functioning systems in place. |

## Compliance checklist

### PCI DSS (Payment Card Industry Data Security Standard)

| Best practice | Adheres? |
|---|:---:|
| Only authorized users have access to customers' credit card information. | ❌ No |
| Credit card information is stored, accepted, processed and transmitted internally in a secure environment. | ❌ No |
| Implement data encryption procedures to better secure credit card transaction touchpoints and data. | ❌ No |
| Adopt secure password management policies. | ❌ No |

### GDPR (General Data Protection Regulation)

| Best practice | Adheres? |
|---|:---:|
| E.U. customers' data is kept private/secured. | ❌ No |
| There is a plan in place to notify E.U. customers within 72 hours if their data is compromised/there is a breach. | ✅ Yes |
| Ensure data is properly classified and inventoried. | ❌ No |
| Enforce privacy policies, procedures and processes to properly document and maintain data. | ✅ Yes |

### SOC type 1 / SOC type 2 (System and Organization Controls)

| Best practice | Adheres? |
|---|:---:|
| User access policies are established. | ❌ No |
| Sensitive data (PII/SPII) is confidential/private. | ❌ No |
| Data integrity ensures the data is consistent, complete, accurate and has been validated. | ✅ Yes |
| Data is available to individuals authorized to access it. | ✅ Yes |

---

## Recommendations for the IT manager

**Priority 1 – Protect cardholder and customer data (PCI DSS / GDPR / SOC)**
- Implement **least privilege** and **separation of duties**, with role-based access control so only authorized staff can reach cardholder data and PII/SPII.
- **Encrypt** credit card data at rest and in transit across all transaction touchpoints.
- **Inventory and classify** all assets and data to know what must be protected and how.

**Priority 2 – Business continuity**
- Create and test a **disaster recovery plan**.
- Implement regular, tested **backups** of critical data, kept off-site or in the cloud.

**Priority 3 – Identity and detection**
- Update the **password policy** to current standards (minimum length, complexity, no reuse) and enforce it through a centralized **password management system**, ideally with MFA.
- Deploy an **IDS** to detect suspicious activity on the network.
- Define a regular **maintenance schedule** and clear intervention procedures for legacy systems.

Implementing these controls would reduce the overall risk score and bring Botium Toys closer to compliance with PCI DSS, GDPR and SOC requirements.

## Skills demonstrated

`NIST CSF` · `Security auditing` · `Risk assessment` · `Control categories (administrative, technical, physical)` · `PCI DSS` · `GDPR` · `SOC 1/SOC 2` · `Security recommendations`
