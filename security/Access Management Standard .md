# Access Management Standard

Owner: Mikhail Kurzin
Area: InfoSec, Infra
Last edited time: June 11, 2025
Approvers: Mike Yan, Dmitry Kushnikov, Antony Gorin
Document ID:  STD-IS-03
Document Type: Standard
Document application: All Contractors, All Employees
Effective date: December 12, 2022
Reviewers: Ivan Toropitsin
Status: Published
Tag: ISO27001
Version: 3

<aside>

**Key points:**

- Authentication and Authorization
- User Accounts and Access Control
- Multi-factor Authentication
- Password Management
</aside>

<aside>

*Manychat is responsible for providing confidentiality, integrity, and availability of its systems. So access to Manychat resources and data must be controlled to ensure that authorized and approved users and partners have access to systems, data, and assets.*

</aside>

---

# Table of Contents

---

# **1. General**

## **1.1 Purpose**

This document describes access control principles, requirements, and the flow of the access request process. It contains information regarding data, which should be provided within each stage of the process.

## **1.2 Scope**

This standard applies to all divisions, teams, and services of Manychat and all personnel of Manychat. It also applies to external organizations and their personnel who have been granted access to the Manychat infrastructure and services.

The document is reviewed at least annually to ensure it meets the current business requirements of Manychat, partners, customers, and external organizations.

# **2. Access Management Standard**

## **2.1 Key requirements**

Manychat key principles that must be taken into account for effective access control are:

- Access to IT resources, systems, data, and assets owned and managed by Manychat must be given in accordance with the following principles:
    - **Need to know** – users or resources will be granted access to systems that are necessary to fulfill their roles and responsibilities.
    - **Least privilege** – users or resources will be provided with the minimum privileges necessary to fulfill their roles and responsibilities.
- Access to IT resources, business systems, data, and assets owned and managed by Manychat must be provided with a unique and personal user account (eg. **name.surname@manychat.com**) and a complex password.
- All main applications shall require multi-factor authentication (MFA) or/and login via corporate Okta SSO.
- Generic or group accounts should normally not be used, but may be provided under exceptional circumstances, if other cybersecurity controls are in place.
- All default accounts (such as user accounts pre-installed by the vendor) must be disabled or blocked. Temporary passwords must be changed on the first log-on.
- The access to business resources must be immediately revoked or actualized when an employee changes position or leaves the company.
- Business systems access rights and privileges must be provided based on user role and function rather than on the status.
- The creation of user accounts with special privileges such as administrator privilege must be rigorously controlled and restricted to only those users who are responsible for the management or maintenance of the business system.
- A formal access rights review process must be conducted at regular intervals.
- Business system access, if technically supported, must be configured to force mandatory use of corporate Okta SSO.
- Every personal identity must be linked to a digital identity/account (even for service or group accounts), which must have a unique and centrally registered user ID.

Additional Access control requirements for environments with Confidential data (eg. Production environment) are:

- Environments must be logically and technically separated depending on the purposes and confidentiality level (eg. Production and Development) to avoid unauthorized access and unauthorized data flows between environments.
- Controls must be in place to prohibit usage of and access to Customer data in development environments.
- Usage of group accounts with sensitive access to critical business systems is not allowed.
- Passwords may never be stored in plain text or using reversible encryption (obfuscation). Up-to-date hashing and salting techniques should be used for password protection.
- Passwords, API keys, access tokens,  must never be hardcoded as plain text in source code or scripts.

## **2.2 Access Control**

### 2.2.1 Initial system access (onboarding)

Manychat establishes default system access for all new hires on day one. By default, all Manychat full-time employees get base access to Google Workspace, Humaans, Okta, Pritunl VPN (all profile), Slack, Miro, Zoom, Zip, YouTrack and Notion. Access to other business systems shall be provided in accordance with the process described in the "Access Requests" section of this document.

There may be a list of team-specific systems for which access to newcomers is provided by default on day one. This information shall be updated by the HelpDesk and any changes shall be controlled by the responsible team.

Account naming must be clear with the possibility to identify the actual account owner. Account naming should be identical for all systems and should use the following pattern:

| **Type of account** | **Account naming rules** |
| --- | --- |
| Account for employees | **first_name.last_name@manychat.com** (eg. harry.tuttle@manychat.com) |
| Account for external users (eg. partners, contractors) | **first_name.last_name@partner.manychat.com** |
| Local system accounts | **first_name.last_name** (same as in email) |

Google Workspace is used as a reference source for all user accounts (eg. First name, Second name, Photo, Team, etc.).

ICAO Transliteration standard (Doc 9303: Machine Readable Travel Documents, [https://www.translit.site/en/type/icao](https://www.translit.site/en/type/icao)) should be used for naming transliteration.

In case of name and surname conflict with another user account, another transliteration standard may be used.

Mandatory fields in the Google Workspace profile must include department, manager, and job role. The user must ensure that his or her end-user profile is the same in all systems in case the user profile can be updated by the end-user.

Users are not allowed to access business systems under personal user accounts not associated with Manychat domains (including usage of personal email addresses).

### 2.2.2 Access Requests

Any access requests apart from default access must be reviewed, approved, and recorded.

Access requests are submitted via the [Manychat ServiceDesk](https://manychat.slack.com/apps/A037JEBA7BJ-manychat-servicedesk?tab=more_info) Slack application.

Access request form captures the following information for each request:

1. Requestor’s name;
2. Access to what resource is required;
3. Type of access level (read/write or specific role);
4. Duration of access (temporary/permanent);
5. Reason for access (must be explained by the requestor);
6. Line manager approval.

Once receiving the request, the assignee (System Owner, System Administrator or HelpDesk) shall check or request the approval of the requestor's Line manager ([source of mapping of end-users to line managers](https://contacts.google.com/directory)) and check or request the approval of the Security Team, if needed, in accordance with the following guidance.

| **Flags indicating additional approval** | **Yes/Not Sure** | **No** |
| --- | --- | --- |
| 1. Is it administrative access? | Security approval is required | Security approval is **not** required |
| 2. Does the business systems inventory require security approval for any access ([business systems inventory](https://www.notion.so/Systems-access-checklist-cf4b67638ca54ac8987de1967c0d4586?pvs=21) "Requires Security Approval" column)? | Security approval is required | Security approval is **not** required |
| 3. Does the system/resource process critical data (eg. security keys, customers’ personal data, contacts data, etc.)? | Security approval is required | Security approval is **not** required |
| 4. Is the access requested to the system owned by the department in which the requestor is operating? | Security approval is **not** required, the decision may be made by the line manager and the system owner | Security approval is required |

### 2.2.3 Privileged system access

Privileged access must be always approved by Security. Privileged access includes but is not limited to:

1. Administrative access to critical business systems;
2. Any access to the production environment;
3. VPN access to restricted segments with confidential data;
4. Access to group or service accounts with critical access (eg. Customer data processing).

Privileged access must require multi-factor authentication (MFA).

It is prohibited to register business system owners on a depersonalized or group account.

### 2.2.4 Service Accounts Management

**Service accounts must have an assigned owner, use system-generated credentials stored in approved secret managers, follow least privilege, prohibit interactive login, be reviewed every 90 days, and be created only inside Manychat-controlled infrastructure. Passwords, keys, or tokens may not be shared, hardcoded, or stored in plaintext.**

### 2.2.5 Access Revocation

Access must be revoked in the following cases:

1. Access request has expired.
2. Employees move to other functions or departments. In this case, if access is still necessary, the new access request must be created.
3. Employee leaves the company. All access requests must be revised by HelpDesk for accurate access revocation.
4. As a result of a security incident, access may be temporarily revoked for containment reasons in accordance with the incident response plan.
5. When a user or system account is no longer necessary.

In case a terminated user is a system owner, the HelpDesk shall initiate the ownership transfer before the user account is suspended or deleted.

### 2.2.5 Third-party access

Access provisioning for third parties (eg. partners, contractors) to Manychat resources must be controlled and monitored.

External access shall be provided under unique Manychat IDs in a dedicated domain (**@partner.manychat.com**).

Access requests must include the basis for relationship with this contractor (eg. Contract number, NDA number, legal entity name) in the description of the reason for access.

Access must be limited to the specific time-period required to perform the tasks. Access must be disabled immediately upon completion of any remote maintenance carried out by third parties.

No access should be granted for Third-party accounts by default except Google Gmail access.

For monitoring reasons, access to Manychat business systems via invite links to the external email address is **not** **recommended** and should be provided via accounts in **@partner.manychat.com** domain.

Manychat responsible member must be assigned as a manager of the external user account.

Security approval is required for all external access requests to Manychat business systems.

External Slack access is allowed only for documented business needs, must be provided as restricted Guest accounts, must include an expiration date and assigned manager, and must be limited to the minimum required channels. Sharing Confidential data with external Slack users is prohibited without Security approval.

### 2.2.6 Password management requirements

OktaSSO must be used, where technically possible, to access business systems. Built-in Okta SSO mechanisms already follow the industry practices on secure log-on procedures, such as token-based access, protection against brute-force attacks, detection of attempts of unauthorized access, captcha, etc.

Google Workspace resources (Gmail, Calendar, Drive) access must require MFA/2SV.

If a business system does not support Okta SSO or allow Okta SSO user-bypassing, reasonable additional security controls must be taken. Such actions may include but are not limited to:

1. Creation of technical system owner account for business system administration (system owner account) linked to email in @manychat.com domain;
2. System owner shall involve HelpDesk or Security to configure security settings of the system, e.g. enforce password complexity and MFA settings, if possible;
3. Require the system owner to perform regular user access reviews.

All business systems should mandate at least the following Password settings:

| **Password**
**Requirements** | **Personalized User accounts** | **Depersonalized (technical and service) accounts** |
| --- | --- | --- |
| Complexity | • Is not based on the account name;
• Contains at least 12 characters;
• Contains characters from all of the following categories:
    ◦ Uppercase alphabet characters (A-Z);
    ◦ Lowercase alphabet characters (a-z);
    ◦ Arabic numerals (0-9);
    ◦ Special characters (!"#$%&'()*+,-./:;<=>?@[\]^_`{|}~) | • Is not based on the account name;
• Requires the use of a password generator;
• Contains at least 14 characters;
• Contains characters from all of the following categories:
    ◦ Uppercase alphabet characters (A-Z);
    ◦ Lowercase alphabet characters (a-z);
    ◦ Arabic numerals (0-9);
    ◦ Special characters (!"#$%&'()*+,-./:;<=>?@[\]^_`{|}~) |
| Account lockout time | At least 30 minutes after 5 failed login attempts |  |
| Password age | The maximum password age for user accounts only applies when the password is not checked for breached passwords and/or dictionaries of known passwords (eg. google breached passwords or HaveIBeenPwned):
• password maximum age is 1 year;
User account passwords that are checked for breached passwords and/or dictionaries of known passwords have no maximum password age and shall be changed by the responsible person if needed. | Passwords have no maximum age and shall be changed by the responsible person if needed. |

Password disclosures of any kind are strictly prohibited and may lead to unauthorized actions on behalf of a legitimate user.

### 2.2.7 Review of access

The following types of privileged access must be reviewed frequently (at least every 12 months):

- VPN access
- Google Workspace
- AWS access
- Snowflake
- Facebook Business Manager
- GitHub
- Slack
- Notion

All accounts created for third-party user access to business systems must be reviewed every 6 months.

### 2.2.8 Logging and Monitoring

Monitoring events that help to control the effectiveness of access control processes include but are not limited to:

- Log-on and log-off events associated with the username, timestamp, and IP or location;
- Invalid login attempts with enabled alerting for multiple events from a single user (to prevent brute-force attacks).

# **3. Roles and Responsibilities**

The CEO has the overall responsibility for Information Security at the Company, including information security regarding personnel and IT security.

Process specific roles and responsibilities:

| **Role** | **Role description** |
| --- | --- |
| **All employees and contractors** | Take responsible actions to comply with the standard. |
| **Managers** | Responsible for ensuring their direct reports (whether those direct reports are permanent employees, contractors, sub-contractors, and agency personnel) are familiar with the requirements of this document. Managers also approve access requests initiated by direct reports. |
| **IT Ops** | Responsible for provisioning of default system access, keeping system inventory list up-to-date, managing access request workflow in terms of forwarding to a responsible system owner, obtaining approvals, and notifying Security in reasonable cases listed in this Standard. |
| **System administrators** | Responsible for defining appropriate access to the system using system built-in access control functionality (e.g. roles), maintaining system role matrix (if relevant), password settings, and conducting user access reviews including nominated system administrators following the least need-to-know access principle. There could be one or several administrators for each system appointed by system owners. |
| **System owners** | System owners (account owners) can undertake the same responsibilities as system administrators. In addition, system owners are responsible for account ownership and billing, supervision of system administrators, and timely interaction with HelpDesk in terms of configuration, system ownership updates, and transfers. There should be only one owner for each system. |
| **Security team** | Responsible for monitoring the effectiveness of the access control process, acting as an independent approver for comprehensive requests, initiating periodic reviews and mandatory actions defined within this Standard, collecting and reporting the summary results to the Leadership Team, and further initiatives on the process improvement. |

# **4. Compliance**

The proof of ISMS quality is the receipt and maintenance of the certificate of ISO/IEC 27001:2022 «Information Technology. Security techniques. Information security management systems. Requirements» compliance.

Manychat must comply with multiple state regulatory requirements of countries, Manychat operates in, such as:

- The General Data Protection Regulation (GDPR) (Regulation (EU) 2016/679);
- Personal data protection regulation in the countries or regions of operation (including CCPA and Law of Armenia on protection of personal data ( ЗR-49-N));
- Canada’s Anti-Spam Law (or “CASL”);
- The CAN-SPAM Act;
- other mandatory state regulatory acts including acts on commercial secrets and intellectual property.

## **4.1 Enforcement**

Implementation and enforcement of this policy is ultimately the responsibility of all employees at Manychat. Security team may conduct ad-hoc checks to ensure compliance with this document without notice. Any violation shall require immediate corrective action. Violations shall be noted in the Manychat applications and responsible employees shall be dispatched to remediate the issue.

For Manychat employees, breaches of this policy may result in disciplinary action being taken and will be dealt with under the disciplinary process in accordance with state laws and regulations of the residence country. Any serious breaches or repeated breaches of this policy may be deemed by Manychat as gross misconduct and may result in disciplinary sanctions, including a remark, reprimand, and dismissal from work.

## **4.2 Exceptions**

Exceptions to this standard must be processed in accordance with the deviation handling rules by the Security team. All exceptions must be maintained taking into account associated risks, exceptions, and recorded approvals. Continuously detected deviations may trigger the changes or improvements of the measures defined in this document.

# **Document History**

| **Version** | **Date of**
**Change** | **Author and Contributors** | **Changes to the previous version** |
| --- | --- | --- | --- |
| 0.1 | 10.12.2021 | **Author**: Mikhail Kurzin, Head of Security | Draft  version |
| 1.0 | 03.04.2022 | **Author**: Mikhail Kurzin, Head of Security
**Contributors**:
• [Antony Gorin](mailto:antony@manychat.com), Head of Infra
• [Anastasia Shchogoleva](mailto:ashchogoleva@manychat.com), Head of Operations
• [Nikolay Nestyurkin](mailto:nestyurkin@manychat.com) Workspace admin
• [Irina Solodkaya](mailto:irina.solodkaya@manychat.com), Internal HR lead. | Initial version |
| 2.0 | 12.12.2022 | **Author**: Mikhail Kurzin, Head of Security
**Approvers**:
• Sunny Manivannan, CEO Manychat Inc.
• Dmitry Kushnikov, Head of Technology | 1. Updated branding. |
| 2.1 | 16.07.2024 | **Author**: Mikhail Kurzin, Head of Security | Document review. No changes were made. |
| 3.0 | 11.06.2025 | **Author**: Mikhail Kurzin, Head of Security | 1. Switch to ISO/IEC 27001:2022
2. Document review |