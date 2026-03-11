# [draft] Manychat Background Checks Policy

Owner: Sergey Muslaev
Area: InfoSec
Approvers: Mike Yan, Dmitry Kushnikov
Document ID: POL-xxx-xx
Document Type: Policy
Document application: All Employees
Reviewers: Mikhail Kurzin, Wesley Gilbert, Ilya Fedosov, Natasha Tolmacheva
Status: In review

## Table of Contents

## **Definitions**

| **Term** | **Definition** |
| --- | --- |
| **Background Check** | The process of verifying a candidate’s or employee’s identity, qualifications, and integrity before or during employment. |
| **Confidential Data** | Information disclosure would cause serious damage and significant harm to the interests or reputation of Manychat. More details: [2.5.1 Confidentiality](https://www.notion.so/2-5-1-Confidentiality-2bfb12e9aa1a805c99b8fb8c6ce6ce60?pvs=21)  |
| **Candidate** | An individual applying for employment, contract, or temporary work at Manychat. |
| **Partner** | External entities or platforms (e.g., Meta, TikTok) with which Manychat collaborates under data-sharing or operational agreements. |
| **Jurisdictional Adjustment** | Customization of background check processes to meet the legal and privacy requirements of specific regions or countries. |

---

# **1. Purpose, Scope, Objectives, Roles and Responsibilities**

## **1.1 Purpose**

The purpose of this policy is to outline Manychat’s approach to conducting pre-employment and ongoing background checks to maintain a trusted and secure work environment. These checks are designed to protect the company, its data, partners, and users by ensuring that individuals entrusted with access to sensitive information uphold the highest standards of integrity and reliability.

Background checks are implemented to strengthen **Manychat’s security and integrity**, including compliance with **ISO/IEC 27001** and **SOC 2 Type II** requirements. While these frameworks encourage employee screening as a security control, our background check program exists primarily to **protect the company, our users, and our partners**, rather than because it is explicitly prescribed within those standards.

## **1.2 Scope**

This policy applies to:

- All **candidates**, **employees** engaged by Manychat.
- All **departments and offices**, including remote employees and international subsidiaries.
- All **background check activities**, regardless of the vendor or region, provided they comply with applicable data protection and employment laws.

Manychat utilizes third-party background screening vendors to conduct most background checks. They operate under the **Data Processing Agreement (DPA)** and **confidentiality provisions** ensuring compliance with **GDPR**, **CCPA**, and equivalent data protection laws. Those vendors process personal data solely on behalf of Manychat and according to documented instructions. Vendor compliance is periodically reviewed by the Security department.

## **1.3 Objectives**

- Safeguard Manychat’s systems, data, and users from internal threats or reputational harm.
- Ensure compliance with internal security and integrity standards.
- Respect the principles of **proportionality** and **data minimization**, ensuring that checks are limited to what is necessary for legitimate hiring and access decisions.
- Meet local legislative obligations and partner-specific requirements (e.g., Meta, TikTok).
- Apply a **risk-based**, **jurisdiction-sensitive**, and **role-specific** approach to background screening.

## **1.4 Roles and Responsibilities**

| **Role** | **Responsibility** |
| --- | --- |
| **Talent Acquisition - Recruitment** | Manages initiation, coordination, and documentation of background checks; ensures candidate consent. |
| **Security** | Maintains alignment with partner and legal standards; verifies local legal compliance; checks that necessary notices are sent to the candidates and consent collection is integrated in the process, initiates DPIAs when required. Assign appropriate risk tier for each position. Ensures that no system, production environment, or access to confidential or sensitive data is granted prior to satisfactory background check completion, including during probationary or pre-boarding periods. Provides notifications on the background checks progress.  |
| **Hiring Managers** | Communicate role requirements to TA. |
| **Legal Counsels** | Advise on country-specific regulations, privacy, and labor laws. |
| **Finance - HRA & Payroll** | Control termination of the contract if background check is failed. |

---

# **2. Policy Reasoning**

The reasoning for implementing Manychat’s background check program directly aligns with the company’s commitment to maintaining **security and integrity** across all operations. This section echoes the rationale outlined in the Purpose, emphasizing that background checks are intended to protect Manychat, its users, and partners — not because external standards prescribe them, but because they are essential for ensuring trustworthy and compliant operations.

Manychat’s approach reflects the intent of international best practices such as ISO 27001 and SOC 2, while adapting to legislative realities, cyber risks and partner expectations. This means that background checks are structured to uphold our internal integrity requirements, comply with regional laws, and maintain the trust and partnership of global platforms such as Meta and TikTok.

## **2.1 Security and Integrity**

Manychat treats background checks as a proactive security control — an essential part of its broader information security and risk management strategy. These checks are designed to prevent potential insider threats, protect company and partner assets, and preserve user trust. They are not performed merely as a compliance formality but as a preventative safeguard that supports Manychat’s long-term resilience, reputation, and alignment with partner expectations.

Manychat stores and processes large volumes of data about its users and Customer Content, including personal and confidential information. The loss, unauthorized disclosure, or misuse of such data could cause significant harm to a large number of individuals and adversely impact Manychat’s operations and reputation. Therefore, ensuring the integrity and reliability of individuals with access to these data assets is a critical preventive control within our security program.

## **2.2 Legislative Compliance**

Manychat’s legislative reasoning for background checks centers on complying with diverse regional data-protection and labor laws. The company customizes its background check practices per jurisdiction rather than applying a single global model (see section [**3. Jurisdictional Adjustment** ](https://www.notion.so/3-Jurisdictional-Adjustment-2a3b12e9aa1a809cb812df057800d4f9?pvs=21)). This ensures each background check process respects local legal frameworks, privacy standards, and employment requirements while maintaining the integrity of the company’s vetting process.

Where background checks involve sensitive data categories, such as criminal history or sanctions list screening, Manychat conducts a **Data Protection Impact Assessment (DPIA)** to evaluate and mitigate potential privacy risks, as required under Article 35 of the GDPR.

## **2.3 Partner Requirements (Meta and TikTok)**

Manychat’s partnerships with Meta and TikTok require adherence to their employee vetting standards. For example, **TikTok mandates** that individuals with access to its data undergo:

1. Social Security trace or identity confirmation.
2. Criminal background check (covering all jurisdictions lived or worked in over the past 7 years).
3. Consolidated Government Screening List review (Terrorist Watchlist).

---

# **3. Jurisdictional Adjustment**

- **Spain and Serbia:** Criminal checks are **prohibited** unless mandated by law. Only identity verification and reference checks are permitted.
- **Netherlands:** This process requires request of the **VOG Certificate** (Verklaring Omtrent het Gedrag) by the candidate before the employment. **In the Netherlands, the failure to obtain a Certificate of Conduct (VOG) may serve as a condition for withdrawing a conditional offer.**
- Where background checks involve international data transfers, Manychat ensures compliance with cross-border safeguards, such as **Standard Contractual Clauses (SCCs)** or adequacy decisions under relevant data protection regulations.

# **4. Check Descriptions**

## **4.1 Description of Check Types**

Manychat defines categories of background checks in a vendor-agnostic way. Individual screening providers (e.g., Checkr, Zinc, or others) may label or bundle their products differently, but the services used by Manychat must map to one or more of the categories below.

| **Check Type** | **Description** |
| --- | --- |
| **Criminal records checks** | Searches criminal records (where lawfully available) for a legally permitted look-back period to identify relevant convictions or pending cases. |
| **Sanctions, watchlist, and restricted-party screening** | Screens against relevant government, law-enforcement, regulatory, and international sanctions or watchlists (for example, export-control, anti-terrorism, or anti-money-laundering lists). |
| **Identity verification** | Validates the authenticity of government-issued identity documents (such as passports or national IDs), including document security features and, where available, database checks. |
| **Right to work check** | A right to work check confirms that an individual has the legal right to work in the country of the employment. |
| **Employment history verification** | Confirms prior roles, dates of employment, and, where appropriate, reasons for leaving for employers relevant to the role. |
| **Adverse media / open-source checks** | Searches reputable media sources and public records to identify serious adverse information relevant to the candidate’s suitability for the role (e.g., credible reports of fraud or professional misconduct), subject to local law. |
| **Professional reference checks** | Obtains feedback from former managers, colleagues, or other professional referees regarding work performance, reliability, and integrity, without collecting unnecessary sensitive personal information. |
| **Education verification** | Confirms the authenticity of the candidate’s highest or otherwise relevant academic degrees, certifications, or other formal education credentials. |
| **Professional reference checks** | References requested from the former colleagues of the candidate |

---

## **4.2 Identity Verification Process**

Due to Manychat’s **remote and globally distributed hiring model**, identity verification is a critical control to prevent impersonation, document fraud, and unauthorized access risks.

Verification is performed by an **external identity verification provider**, which temporarily processes a copy of the candidate’s government-issued ID to confirm authenticity.

## **4.3 Reference Checks**

Reference checks are performed to verify the candidate’s professional conduct and performance through references obtained from former colleagues or supervisors. The process is conducted by the **Talent Acquisition team** after the candidate’s consent, focusing only on job-related aspects such as reliability, teamwork, and professional integrity. No sensitive personal data or private information is collected during this process.

# **5. Risk-Based Screening Model**

## **5.1 General requirements**

Access to **confidential data (**More details: [2.5.1 Confidentiality](https://www.notion.so/2-5-1-Confidentiality-2bfb12e9aa1a805c99b8fb8c6ce6ce60?pvs=21)) includes any direct or indirect access to **user personal data**, **customer information**, **sensitive business data**, or **production systems**.

Such access must not be granted to any employee or contractor until all required background checks applicable to the role have been successfully completed.

Each department is classified according to the Department Risk Mapping described in [Annex 1](https://www.notion.so/draft-Manychat-Background-Checks-Policy-28cb12e9aa1a80aca6a3e88b1c078811?pvs=21) of this policy.

## **5.2 Tier 1 — High Risk Roles**

**Includes:** Leadership team members and employees with access to production systems, infrastructure or data engineering admin tools, customer content, sensitive financial data and other confidential data.

These checks are reserved for roles involving the highest degree of access or responsibility and must therefore be **strictly justified** by the nature of the position.

The number of Tier-1 screenings should be **minimized** and limited to functions where enhanced verification is demonstrably necessary to mitigate substantial security or compliance risks.

**For Tier 1 candidates Manychat will typically request an equivalent combination of:**

- identity and address verification;
- right to work check;
- criminal records checks, where lawfully permitted;
- sanctions, watchlist, and restricted-party screening;
- open-source checks, where appropriate and lawful;
- qualification verification;
- employment history verification; and
- professional reference checks.

The exact combination of checks may vary by jurisdiction, by the risk profile of the role, and by the capabilities of the engaged screening provider, but it must provide coverage equivalent to the categories above and remain compliant with local law.

## **5.3 Tier 2 – General Risk Roles**

**Includes:** positions that do **not have direct access** to production environment and other confidential information but may have access to **user and customer contact information**, **internal business information or partner-related aggregated analytics** considered sensitive.

These roles typically involve **customer success, coordination, or analytical functions t**hat handle company data of moderate sensitivity but do not pose a high systemic or compliance risk.

**For U.S.-based Tier 2 candidates, Manychat will typically request a reduced set of checks focused on:**

- identity and address verification (for example, via SSN or other government-identifier-based traces and address history tools);
- right to work check;
- appropriate local / state / national criminal records checks;
- sanctions, watchlist, and restricted-party screening;
- professional reference checks, where appropriate.

**For Tier 2 candidates based outside the U.S., Manychat will typically request:**

- identity document validation;
- sanctions, watchlist, and restricted-party screening;
- right to work check;
- professional reference checks, where appropriate.

The scope of Tier 2 checks may be further tailored by jurisdiction, role profile, and provider capabilities, provided that the resulting package remains consistent with the moderate-risk nature of these roles and the principles of proportionality and data minimization.

## **5.4 Tier 3 – Low-Risk Roles**

**Includes**: positions with **no access** to customer content or personal data of the users, production systems, financial or confidential business information, and that perform **non-sensitive or administrative functions**.

Examples may include:

- Interns or short-term contractors performing non-technical assignments;
- Marketing or design staff without access to customer or user data;
- Administrative or support roles limited to internal coordination or public materials.

For Tier 3 roles, **no formal background checks are required** beyond **identity verification,** right to work check and standard onboarding documentation.

Any additional verification must be **specifically justified** by a documented business or regulatory requirement and approved by the Talent Acquisition and Security & Compliance teams.

---

# **6. Procedures and Candidate Communication**

## **6.1 Timing of Background Checks**

Background checks may only be initiated after a candidate has been selected for hire (offer stage) and may not be conducted before the interview or during the early screening stages of recruitment.

Employment offers and employment agreements may be issued and signed prior to completion of background checks, where permitted by applicable law, provided that such offers or agreements are expressly conditional upon satisfactory completion of the required background checks.

Offer letters and employment agreements must contain explicit provisions stating that:

- employment and continued employment are conditional upon satisfactory completion of applicable background checks;
- failure to complete or pass required background checks may result in withdrawal of the offer or termination of employment, in accordance with applicable law;
- no access to confidential information, systems, or sensitive data will be granted prior to completion of such checks.

## **6.2 Candidate Communication and Consent**

- Candidates must receive written notice describing the purpose, scope, and type of background checks.
- Written **informed consent** must be obtained before processing begins.
- Candidates may exercise their **data subject rights** (access, rectification, erasure, restriction, objection) by sending an email to **[privacy@manychat.com](mailto:privacy@manychat.com)**.
- Candidates have the right to **review and dispute** inaccurate information.

## **6.3 Data Protection and Retention**

Background check data will be **securely stored, encrypted, and limited to authorized personnel**.

If **no employment occurs**, personal data must be deleted once the recruitment process ends, unless there is a valid legal basis to retain it — typically, the candidate’s **informed consent** for future vacancies or, in limited cases, a **legitimate interest**. Retention for such purposes should not exceed **twelve (12) months**, after which consent must be renewed or the data deleted.

If **employment occurs**, documents proving compliance with hiring, social security, and payroll obligations shall be retained for at least **four (4) years**, in line with statutory requirements.

Data may be **blocked** where retention is necessary for legal defense and will be **securely deleted or anonymized** once the relevant limitation periods expire.

International transfers of data are safeguarded by **Standard Contractual Clauses (SCCs)** or equivalent mechanisms.

Processing complies with **GDPR**, **LGPD**, **CCPA**, and other applicable data-protection regulations.

Manychat conducts background checks primarily through **third-party service providers** acting as **data processors** under Manychat’s documented instructions. Those vendors adhere to strict data-protection, confidentiality, and security standards and process personal data only as necessary for verification purposes.

## **6.4 Internal Transfers and Additional Checks**

When an employee transfers from one position to another with a higher risk tier, Manychat may conduct additional background checks corresponding to the new tier’s requirements.

This applies, in particular, to movements from **Tier 3 → Tier 2** or **Tier 2 → Tier 1**, where access to more confidential data, systems, or customer content is introduced.

Such checks must follow the same principles of proportionality, data minimization, and candidate notification as initial pre-employment checks.

---

# **7. Compliance, Audits, and Review**

This policy will be reviewed annually or upon major legal, operational, or partner requirement changes. Internal audits and third-party reviews may be conducted to ensure ongoing compliance. The **Security team** ensures that this policy remains accurate and effective.

Non-compliance may result in disciplinary action, including employment termination, and may expose the company to contractual penalties or partner suspension.

---

# **8. Privacy Notice Reference**

Background check data is processed in accordance with the [**Manychat Candidate Privacy Statement**](https://manychat.com/legal/candidate-privacy-statement), which provides detailed information about:

- The categories of personal data processed during background checks.
- The purposes and legal bases for processing.
- Data retention periods and deletion practices.
- The rights of candidates and employees regarding their personal data.

Candidates are encouraged to review this Privacy Statement prior to consenting to any background check.

---

# Annex 1 - Department List Mapping

[Untitled](%5Bdraft%5D%20Manychat%20Background%20Checks%20Policy/Untitled%20293b12e9aa1a809b868bc57cf436638e.csv)