# ISMS Context and Scope

Owner: Mikhail Kurzin
Area: InfoSec
Approvers: Mike Yan, Dmitry Kushnikov
Document ID: POL-IS-03
Document Type: Policy
Document application: All Contractors, All Employees
Effective date: April 24, 2023
Status: Published
Tag: ISO27001
Version: 5

# Table of contents

---

# **1. General**

## 1.1 Purpose

This document describes the scope and boundaries of the Information Security Management System (“ISMS”) implemented in Manychat ("the Company"). The ISMS scope and boundaries are described in consideration of the Company’s context, including the requirements of relevant interested parties as well as dependencies between activities performed by the Company and by other organizations.

This document confirms the declaration of the Company’s Leadership team expectations that the ISMS complies with the requirements of ISO/IEC 27001:2022.

All references made in this document are to the latest versions of the ISMS documented information including that of external origin.

## 1.2 Company Context

Manychat is a chat marketing platform with a mission to help businesses grow by building meaningful relationships with their customers.

Manychat is committed to provide a safe and secure environment to customers that use Manychat services.

The Company has millions of accounts globally and put particular importance for privacy considering the large quantities of personal data it processes through Facebook, Instagram, WhatsApp and other integrations.

Manychat would like to provide assurance to its key stakeholders and key partners that confidentiality, integrity and availability of data is adequately maintained.

The Company believes that establishing, implementing, maintaining and continually improving an ISMS helps to combat cyber threats it faces.

The Company’s context is defined in terms of the following internal and external issues that are relevant to the Company’s mission. The context affects its ability to achieve the intended outcomes of the ISMS.

External factors:

- Economic market factors: limited budget for information security;
- Competitive environment: high confidentiality, integrity, and availability requirements of information, significant damage from leaks or disclosures;
- Compliance: the need to comply with different local laws in countries where Company operates;
- Fraud: sms, email and chat fraud increase.

Internal factors:

- IT sustainability: high requirements regarding the availability of Manychat platform;
- High volumes of data processing and data storage: large volume of customer data, including personal data;
- Third-party applications and components: vulnerabilities and bugs in open-source and third-party components used in Manychat platform can lead to serious financial and reputation losses for the Company;
- Resilience of IT infrastructure: high requirements regarding the service continuity;
- High dependencies on cloud infrastructure and third-party integrations: dependency of Manychat platform hosted in cloud provider and connected to several key service providers (SMS, email, CRM, etc.);
- Roles within the Company: international team located in several countries.

When analyzing the Company's information security risks, the impact of the internal and external factors listed above must be considered.

## 1.3 Requirements of stakeholders

The company considers stakeholder relations as the most important condition for sustainable development. Creating effective relationships between the Company and its stakeholders ensures continuous development and business continuity, reduction of investment risks, compliance with legislation in operating countries, as well as the good reputation of the Company.

The list of stakeholders is outlined in Table 1 and is taken into account for ISMS scope selection and further review.

***Table 1. List of requirements of stakeholders.***

| **#** | **Stakeholders** | **Requirements** |
| --- | --- | --- |
|  | **External Stakeholders** |  |
| 1 | **Legislation and regulatory** | Compliance with legislation and regulatory requirements which applicable to Company in accordance with territories, activities and processing data, including:
• CCPA;
• GDPR;
• Privacy Legislation around the World;
• Anti-Spam legislation around the World (CAN-SPAM, etc.). |
| 2 | **End customers - individuals, enterprise clients, government and non-profit organizations** | • Protection of sensitive data (including confidential and  personal data, ensuring compliance with legal requirements and contractual obligation);
• Meeting contractual requirements relating to information security and data ownership;
• Ensuring the availability and integrity of the information services provided, continuous support and knowledge transfer;
• Acquisition of products and services of high quality that are robust to IT industry flaws and vulnerabilities;
• Transparent communication;
• Building stable long-term business relationships. |
| 3 | **Partners and marketing agencies** | • Protection of business sensitive and confidential information, including personal data;
• Meeting contractual requirements relating to information security and data ownership;
• Increase in market share by selling products and services of high quality that are robust to bugs, cyber threats and vulnerabilities;
• Products and services high quality support and continuous knowledge transfer;
• Transparent communication;
• Building stable long-term business relationships. |
| 4 | **Competitors** | • None. |
| 5 | **Service providers:** |  |
|  | IT infrastructure (AWS) | • Implementation of contractual requirements in matters of information security and continuity. |
|  | Platform integrations (Facebook, SendGrid, Twilio, Intercom, Telegram, Shopify, et.) | • Implementation of contractual requirements in matters of information security. |
|  | Business cloud systems (HR, Accounting, etc.) | • Implementation of contractual requirements in matters of information security. |
|  | **Internal Stakeholders** |  |
| 6 | **Leadership team** | • Information Security Risk Management;
• Protection of confidential information, ensuring compliance with requirements;
• Company of information security management processes;
• Requirements for local regulatory and administrative documentation for ISMS. |
| 7 | **Employees** | • Protection of confidential information, including personal information of employees; 
• Compliance with requirements;
• Ensuring the availability and integrity of IP. |
| 8 | **Internal divisions of the Company** | • Asset protection;
• Protection of confidential information, ensuring compliance with requirements;
• Ensuring the availability of business systems and services;
• Training and raising the awareness of personnel in the field of information security;
• Investigation of IS incidents;
• Business Continuity. |

The ISMS extends to the business-process below:

- Control;
- Technical design;
- Maintenance;
- Security and availability;
- Customer support;
- Development;
- Provisioning of Manychat products and services.

Products and services covered by ISMS:

- Manychat web application;
- Manychat applications for mobile devices (iOS, Android);
- Manychat application programming interfaces (APIs).

The process of implementation of the ISMS related activities are reflected in the internal documents of the Company such as organizational structure, job descriptions and supporting documentation.

Key Teams:

The ISMS in the Company extends to the teams, which perform main business process activities in accordance with Table 2. Other teams may be involved in ISMS processes, however, they are not relevant to the execution of the ISMS business-process. These units are not included in the ISMS risk assessment scope.

***Table 2. Main ISMS supporting teams***

| **Team** | **ISMS type (Main\Core\Supporting)** | **Entity Name** | **Location** |
| --- | --- | --- | --- |
| Leadership team | Main | Manychat Inc.
OctoHub LLC
Manychat S.L.
Manychat NL B.V. | US, Austin
Armenia, Yerevan
Spain, Barcelona
Netherlands, Amsterdam |
| Product management and design | Core | Manychat Inc.
OctoHub LLC
Manychat S.L.
Manychat NL B.V. | US, Austin
Armenia, Yerevan
Spain, Barcelona
Netherlands, Amsterdam |
| IT infrastructure maintenance | Core | OctoHub LLC
Manychat S.L. | Armenia, Yerevan
Spain, Barcelona |
| Customer support | Core | Manychat Inc.
OctoHub LLC
Manychat Brazil LTDA | US, Austin
Armenia, Yerevan
Brazil, São Paulo |
| Product Development | Core | OctoHub LLC
Manychat S.L. | Armenia, Yerevan
Spain, Barcelona |
| Office internal IT | Supporting | OctoHub LLC | Armenia, Yerevan |
| Information security and compliance | Supporting | OctoHub LLC
Manychat S.L. | Armenia, Yerevan
Spain, Barcelona |
| Finance & Accounting | Supporting | Manychat Inc. 
OctoHub LLC | US, Austin
Armenia, Yerevan |
| Legal | Supporting | Manychat Inc. 
OctoHub LLC | US, Austin
Armenia, Yerevan |
| Human Resource | Supporting | Manychat Inc.
OctoHub LLC
Manychat S.L.
Manychat NL B.V. | US, Austin
Armenia, Yerevan
Spain, Barcelona
Netherlands, Amsterdam |
| Marketing & Sales | Supporting | Manychat Inc. | US, Austin |

## 1.4 Information Assets and Technology Infrastructure

The ISMS key information types include:

- Customer data (user data);
- Subscribers data (customers of Manychat customers);
- Personal Data;
- Company’s confidential information;
- Data related to employees and managers;
- Data related to IT infrastructure, hardware, software, proprietary source code security measures;
- Contracts information.

The Company utilizes cloud-based infrastructure (IaaS, PaaS, SaaS), provided by Amazon Web Services, to run its core platform.

Information assets covered by the ISMS scope are identified and their inventory is maintained in the Risk Management Report.

The scope of the ISMS includes the Manychat platform and its supporting business systems, which constitutes of the following assets and technologies:

- information and business processes,
- employees,
- information assets, including databases, files, documentation,
- cloud services, programs, and data storage system,
- software assets, including system and application software,
- physical assets, including networking equipment, communications channels, workstations, servers and storage systems,
- facilities, including buildings,
- services and integrations.

The list of information assets, software assets, systems, services and other technical means are regularly reviewed and updated in the process of Information security risk management.

The main interfaces used for interaction between the scope of the Company's ISMS and the other Companys' activities and dependencies between activities performed by the Company and those that are performed by other organizations are listed below:

***Table 3. Interfaces and dependencies***

| **Interface/dependency** | **Description** |
| --- | --- |
| Data transmission network | Network equipment and communication channels |
| Business processes support cloud systems (HR, Accounting, etc.) | Manychat teams interact with business systems that support their business processes |
| Internal teams | Interaction according to job responsibilities |
| Platform integrations (Facebook, SendGrid, Twilio, Intercom, Telegram, Shopify, et.) | Manychat platform interacts with information systems of third-party organizations |
| IT infrastructure platform (AWS) | The Manychat system is hosted on a third-party cloud computing platform |
| Other   services provided by external organizations | • lease of office premises,
• equipment transportation and delivery,
• wired communications, etc. |
| Manychat system users | Entities and persons with access to the Manychat system |

## 1.5 Physical boundaries

| **Location** | **Type** | **Activities / Functions / interfaces** |
| --- | --- | --- |
| Manychat Inc. (US), Austin | HQ,
Physical office (co-working), Remote | • Product management and design
• Risk management and strategy 
• Corporate functions 
• Legal, governance and compliance 
• Marketing
• Sales
• Customer Success
• HR |
| OctoHub LLC (Armenia), Yerevan | Operations, Physical office, Remote | • Product management and design
• IT and Cyber security Operations 
• Software Engineering 
• Software Development
• Risk management and strategy 
• Corporate functions 
• Product support
• Legal, governance and compliance 
• HR |
| Manychat S.L.
(Spain), Barcelona | Operations, Physical office (co-working), Remote | • Product management and design
• IT and Cyber security Operations 
• Software Engineering 
• Software Development
• Corporate functions 
• Legal, governance and compliance 
• HR |
| Manychat NL B.V.
(Netherlands), Amsterdam | Operations, Physical office (co-working), Remote | • Product management and design
• IT and Cyber security Operations 
• Software Engineering 
• Software Development
• Corporate functions 
• Legal, governance and compliance 
• HR |
| Manychat Brazil LTDA
(Brazil), São Paulo | Operations, Physical office (co-working), Remote | • Product management and design
• IT and Cyber security Operations 
• Corporate functions 
• Product support
• Legal, governance and compliance 
• HR |

# **2. Definition of ISMS scope**

Manychat operates an Information Security Management System, which complies with the requirements of ISO/IEC 27001:2022 in accordance with the following scope statement:

Development, control, technical design, maintenance, customer support and provisioning of Manychat platform services including:

- Manychat web application,
- Manychat applications for mobile devices (iOS, Android),
- Manychat application programming interfaces (APIs).

This in accordance with the Statement of Applicability.

# **3. Rationale of scope decision**

The choice of the listed process and applications as the area of implementation and certification of ISMS is based on the requirements of customers and partners to ensure information security in the production environment.

Leakage of customer data can lead to irreparable damage to the reputation and finances of the Company.

The implementation and certification of ISMS in the above area are designed to ensure the selection of adequate and proportionate security management measures that will protect information assets and provide the necessary assurance of compliance with contractual requirements for all stakeholders.

The ISMS is embedded in the Company’s processes and overall management structure, so information security is considered within the design of processes, business systems, and controls.

# **4. Exceptions**

All sales, marketing, data analytics, and source code development activities are excluded from the ISMS scope.

# **Document History**

| **Version** | **Date of**
**Change** | **Author, Contributors and Approvers** | **Changes to the previous version** |
| --- | --- | --- | --- |
| 0.1 | 16.09.2021 | **Author**: Mikhail Kurzin, Head of Security | Draft  version |
| 1.0 | 17.01.2022 | **Author**: Mikhail Kurzin, Head of Security | Initial version |
| 2.0 | 14.04.2022 | **Author**: Mikhail Kurzin, Head of Security
**Approvers**:
• [Mike Yan](mailto:mike@manychat.com), CEO (US)
• [Dmitry Kushnikov](mailto:dmitry@manychat.com), Head of Technology, CEO (Armenia)
• [Anastasia Shchogoleva](mailto:ashchogoleva@manychat.com), Head of Operations
• [Irina Solodkaya](mailto:irina.solodkaya@manychat.com), Internal HR lead. | Yerevan Virtual office update |
| 3.0 | 02.06.2023 | **Author**: Mikhail Kurzin, Head of Security
**Approvers**:
• [Mike Yan](mailto:mike@manychat.com), CEO | - Added “development” to ISMS scope
-  Added Spain office
- Changed legal name of Armenia office
- Added Sales and Product development functions to Table 2. |
| 4.0 | 24.04.2024 | **Author**: Mikhail Kurzin, Head of Security
**Approvers**:
• [Mike Yan](mailto:mike@manychat.com), CEO | - Added “fraud” to external factors.
-  Changed the US, NY office to US, Austin.
- Added marketing to the Functions section. |
| 5.0 | 11.06.2025 | **Author**: Mikhail Kurzin, Head of Security
**Approvers**:
• [Mike Yan](mailto:mike@manychat.com), CEO | -Switched to ISO/IEC 27001:2022
-Added Brazil and Amsterdam offices to the Physical boundaries |