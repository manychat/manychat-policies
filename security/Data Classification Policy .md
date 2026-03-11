# Data Classification Policy

Owner: Mikhail Kurzin
Area: InfoSec
Last edited time: January 26, 2026
Approvers: Mike Yan, Dmitry Kushnikov, Antony Gorin
Document ID: POL-IS-02
Document Type: Policy
Document application: All Contractors, All Employees
Effective date: December 12, 2022
Reviewers: Mikhail Kurzin, Xavier Gumara Rigol
Status: Published
Tag: ISO27001
Version: 4

# Table of Contents

---

# **1. General**

## **1.1 Purpose**

Information is critical to all we do at Manychat. Each of us plays an important role in managing  information and making sure that we handle it securely. That means taking into account both the sensitivity of the information and the business need to share information.

Therefore, Manychat classifies information into several categories depending on the harm that could result from a loss or unauthorized disclosure. On creation, all data and information must be assessed to determine the appropriate classification category.

This document defines the requirements for information classification and labeling to protect **confidentiality (including conditions of data processing depending on the sensitivity, privacy, and ownership)**, **integrity**, and **availability** of all data and information assets.

The labeling criteria based on the defined classification groups are essential in the definition of corporate business systems’ level. Integrity and availability criteria generally apply to the systems processing predefined types of data (confidentiality level, subject to specific regulations).

## **1.2 Scope**

This policy covers the classification and handling of Manychat information and information assets. This includes all paper documents, electronic documents, multimedia (photos, video, Zoom-recordings, Slack messages, Google Drive documents, etc.), verbal information (phone conversations/voicemail), as well as data and information held in systems, applications, or equipment that can store, process or transmit data.

This policy applies to all Manychat’s teams, services, and all personnel of Manychat. It also applies to external organizations and their personnel who have been granted access to Manychat infrastructure and services.

This policy also applies to data used in the design, configuration, operation, monitoring, and improvement of AI-enabled systems, to the extent such data is under Manychat’s control or influence.

The document is reviewed at least annually to ensure it meets the current business requirements of Manychat, partners, customers, and external organizations.

# **2. Data Classification Policy**

## **2.1 General requirements**

1. The Company shall classify the processed data in accordance with the pre-defined criteria. Information types shall be classified based on the following information security objectives: confidentiality, integrity, derived clients’ data, and regulatory requirements.
2. Classification of Information will take place at the following levels:
    - For paper and electronic documents, including output from systems, classification will apply to each individual document;
    - For business systems, classification will be done at the most sensitive dataset level (**for Google Drive classification should be done on a document level**);
    - For information in a database, the classification will normally apply to the entire database with a degree of the most sensitive type of data processed;
    - Laptops, USB sticks, and any other information carriers will be classified at the highest category of information carried.
3. Manychat business systems shall inherit the classification of the processed data. In case the business system aggregates data from multiple sources for processing, the final classification level for data shall be calculated by the highest value among all integrations.
4. A flag (or similar indicator) shall be created in the business systems inventory indicating if an application processes or allows access to confidential or mission-critical information. This flag shall be indicative and not be considered a full inheritance of the classification on the application level.
5. Reviews of the business system classification must be performed on an annual basis.
6. Review of classification schemas described in this policy shall be reviewed in an event of continuous deviations caused by the inability of the classification schema to achieve its goals.
7. Changes to classifications must be validated and approved by the Manychat Security and Legal supporting units.

## **2.2 Information Handling**

Associates, contractors, third parties (and anyone else with access to information and information systems of Manychat) shall be accountable to handle and process information in accordance with the information classification. The Information handling rules are described in [Office Security Standard](https://www.notion.so/Office-Security-Standard-2b7b12e9aa1a8005ab2edd693784d06f?pvs=21).

## **2.3 Information identification and ownership**

There shall be a process of identifying and listing information types in an information inventory. The Process Owner (it can be either a System Owner or a person who originated the information or record) is responsible for setting the classification level. An information type is defined as information grouped and categorized from the perspective of its content and business use rather than by the file, document, business system or other "container" that holds it. Its grouping should enable associates to identify and subsequently protect and manage it effectively.

## **2.4 Business systems identification**

There shall be a formal process of identifying and documenting IT systems in Manychat approved business systems inventory, that shall include in-house and SaaS applications.

System owners shall be identified and appointed both from an IT side as from a business side (for IT-owned applications the business side may also be someone from IT).

Relevant components that support IT applications (e.g. software, documentation, supporting databases, servers, etc.) shall also be identified and recorded in an inventory.

## **2.5 Classification**

### 2.5.1 Confidentiality

Confidentiality relates to the ability and authorization to read and share information. Each additional level of classification matches with security measures per corresponding confidentiality defined by Manychat.

The Manychat classification scheme has the following three categories:

| **Confidential** | Information disclosure would cause serious damage and significant harm to the interests or reputation of Manychat. 
Additional aspects: This is the type of information that, due to potential risk exposure, is to be restricted to a smaller group of people than the entire business unit. Such information includes customer-owned data, internal proprietary data related to technical configurations, source code, contract clauses with customers and suppliers, employee sensitive data. | Examples (not all-inclusive):
• Account  credentials and  any other  information used to  authenticate  identity such as passwords, PINS, and databases  containing  authenticating information
• Strategic business  plans (e.g., acquisition plans) 
• Forecasting  assumptions
• Treasury activities
• Sensitive Personal  Information of customers and employees 
• Security vulnerabilities 
• Security incidents 
• Hosted customer  data that includes  regulated or sensitive personal  information |
| --- | --- | --- |
| **Internal**
**[default value]** | Information disclosure could cause some harm to the interests or reputation of Manychat. 
Additional aspects: This classification reflects the risk of disclosure. As such, it does not imply that any information classified “internal” should be freely accessible to all Manychat employees. The need-to-know principle shall still apply.
This is the default level of classification, which shall be assumed for all information where the owner or context does not indicate another classification (e.g. for personal data the default classification assumed should always be Confidential unless otherwise determined).
Only if the information is truly more sensitive in terms of confidentiality shall it receive a higher classification. | Examples (not all-inclusive):
• Company-wide sendmails 
• Employee training materials 
• Employment  applications and  resumes (excl. Sensitive Personal  Information and payment data)
• Contracts and proposals from vendors 
• Product use cases and  requirements  
• Organization charts
 |
| **Public** | This classification includes information that is approved by the Manychat Marketing to be made available to the public. 
Additional aspects: In most cases, information must be cleared for public release through a specific process including formal approvals.
Examples:
Information published in blogs or any public websites, customer press releases, etc. | Examples (not all-inclusive):
• Published  Annual Reports 
• Press releases 
• Published  white papers,  product  announcement,  product  documentation,  Marketing  materials and social media content |

The default value for data originated and processed at Manychat is classified as **Internal** and is a subject of Confidentiality statement signed by all Manychat employees and third-parties. Data classified as Internal is allowed for disclosure between Manychat employees and contractors but is not allowed for disclosure to any untrusted third party.

**Confidential** data requires an additional protection level. Such may include access limitations to a defined list of employees per category even among Manychat. Disclosure of such information must be performed after explicit approval of the Process Owner even in case the NDA is in place.

Documents and paper records must be labeled in accordance with their Confidentiality class. It is optional to label all Internal records. However, Confidential data must always be labeled.

### 2.5.2 Integrity

Manychat shall classify information types on their required level of integrity, taking into account the risk impact it would have on the Company if the information involved were to be maliciously or accidentally altered.

Information integrity is expressed in one of two classifications: **Vital** and **Standard**.

| **Vital** | Information whose accidental or malicious alteration would cause serious damage to the point of endangering the existence of Manychat.
Additional aspects:
This is typically information that:
• is subject to high impact fraud (impact considered should combine financial, reputational, regulatory, and legal aspects)
• if accidentally or maliciously altered, could result in serious operational mistakes with a major impact on Manychat customers
• if accidentally or maliciously altered, could result in wrong strategic decisions by management resulting in serious penalties or harm to reputation |
| --- | --- |
| **Standard**
**[default value]** | Information whose accidental or malicious alteration would cause less than serious harm to the interests of Manychat.
Additional aspects:
This is the default level of classification, which shall be assumed for all information where the owner or context does not indicate another classification. |

### 2.5.3 Availability

All Manychat business systems shall be classified on their required level of availability, taking into account the risk impact it would have on Manychat if the application involved were to not be available when required.

Availability is determined by operational recovery requirements (in e.g. service level agreements or service descriptions), and/or disaster recovery requirements (as determined in disaster recovery planning) shall prevail over any availability classification. The latter shall be considered as an indicator only.

Information availability is expressed in one of the following classifications:

| **Mission Critical** | Corporate business systems whose unavailability (more than 24 hours) has a significant business impact.
Additional aspects:
Rule of thumb: maximum tolerable unavailability-time is less than a day. |
| --- | --- |
| **Business Critical**
**[default value]** | Corporate business systems whose unavailability (more than 24 hours) has no or very limited business impact.
Additional aspects:
Rule of thumb: maximum tolerable unavailability-time is more than 1 day, recovery shall be as per best effort. |
| **Business Support** | Corporate business systems with inessential availability requirements. |

### 2.5.4 Customer data

This classification shall be used for information types as well as to indicate if applications hold or provide access to customer data.

As privacy has a link to confidentiality, the confidentiality classification of information types shall take into account the privacy classification.

Customer data processed in Manychat business systems is classified as follows:

| **None** | Corporate business system is not used for processing customer data |
| --- | --- |
| **Lead/ Contract data** | Corporate business system contains a pool of customers or potential customers. Additional aspects: Such data is disclosed to parties mutually and includes basically contact information or direct messaging with customers. Applies for CRM-like systems and communication services. |
| **Customer- owned content** | Corporate business system which is used for storage and processing of customer-owned data. Additional aspects: Such data includes content, customer settings, logs and support track history (which might include customer owned content as well) and any other records made by the customer solely without intent to be accessed by Manychat |

### 2.5.5 Regulated data

Some information is subject to specific legal handling requirements and therefore is classified as Confidential by default, and must be treated in accordance  with this Policy, and any applicable processes adopted for the handling of such information. Examples are provided below.

Manychat in general does not process such information of its customers but may process some data related to its employees. Before starting to process the following data, the Legal support unit must be consulted first.

**Sensitive Personal information**

Sensitive Personal Information is Confidential Information and includes:

- social security number / national identifier;
- benefits choices and health information;
- union, political and religious affiliation;
- race;
- sexual orientation information;
- information about an individual’s dependents and beneficiaries;
- clearance level;
- criminal history; and
- results of credit checks.

**Other Industry or Regulatory Requirements**

Information that is subject to other industry or regulatory handling requirements is  Confidential information. Such information includes:

- Payment card data subject to the Payment Card Industry Data Security Standards (e.g., primary account number, cardholder name, and expiration date)
- Data subject to healthcare or research-related regulations.

### 2.5.6 AI-Specific Data Classification and Management

Data used in AI-enabled systems may include user-provided inputs, prompt configurations, system metadata, AI-generated outputs, and operational logs. Such data shall be classified and handled in accordance with the classification levels defined in this policy.

Manychat does not acquire, select, or manage training datasets for AI models. Training data and model development are the responsibility of third-party AI service providers.

Data quality requirements for AI-enabled systems include relevance to the intended use, suitability for processing, and integrity sufficient to support reliable AI operation. Controls are applied to detect malformed inputs, unexpected outputs, or abnormal behavior during AI system operation.

Data provenance for AI-enabled systems is recorded at a level proportionate to Manychat’s role and includes documentation of data source categories, purpose of use, and lifecycle context. Data provenance does not extend to training data managed by third-party AI service providers.

Criteria for selecting data preparation methods for AI-enabled systems include alignment with intended use, compatibility with third-party AI services, data minimization principles, and identified AI risks and impacts.

## **2.6 Disclosure**

Any disclosure of information must be lawful.

Prior to disclosure, information within Manychat control must be marked and controlled in accordance with the Data Classification Policy.

Contractors or temporary employees with access to Confidential material must be required to sign a non-disclosure agreement (NDA) detailing the terms of access and handling of the material concerned.

Information classified Confidential shall only be disclosed to named individuals and controls must be applied to defend against unauthorized or accidental disclosure.

Information that is classified Confidential must not be disclosed to a third party without the express permission of the Leadership team member who owns the information.

# **3. Roles and Responsibilities**

The CEO has the overall responsibility for Information Security at the Company, including information security regarding personnel and IT security.

Process specific roles and responsibilities:

| **Role** | **Role description** |
| --- | --- |
| **All employees** | Employees are responsible to comply with the Standard and report the violations to the Security team. |
| **Managers** | Line managers are responsible to ensure the awareness of this Standard across their teams. |
| **Security team** | Security team is responsible for monitoring overall awareness with this Standard, monitoring, and investigating the violations, and deviations handling. |

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
| 0.1 | 24.01.2022 | **Author**: Mikhail Kurzin, Head of Security | Draft  version |
| 1.0 | 01.03.2022 | **Author**: Mikhail Kurzin, Head of Security
**Approvers**:
• [Mike Yan](mailto:mike@manychat.com), CEO Manychat Inc. (US)
• [Dmitry Kushnikov](mailto:dmitry@manychat.com), CEO Manychat LLC (Armenia)
• [Maria Eremenko](mailto:eremenko@manychat.com), Head of People
• [Antony Gorin](mailto:antony@manychat.com), Head of Infra | Initial version |
| 2.0 | 12.12.2022 | **Author**: Mikhail Kurzin, Head of Security
**Approvers**:
• Sunny Manivannan, CEO Manychat Inc.
• Dmitry Kushnikov, Head of Technology | 1. Updated branding.
2. Added details on types of documents/information to be labeled (2.1.2). |
| 2.1 | 16.07.2024 | **Author**: Mikhail Kurzin, Head of Security | Document review. No changes were made. |
| 3.0 | 11.06.2025 | **Author**: Mikhail Kurzin, Head of Security | 1. Switch to ISO/IEC 27001:2022
2. Document review |
| 4.0 | 26.01.2025 | **Author**: Sergey Muslaev, GRC Lead | Updating document in accordance with ISO/IEC 42001:2023 |