# Business Continuity and Disaster Recovery Policy

Owner: Mikhail Kurzin
Area: InfoSec, Infra
Last edited time: June 6, 2025
Approvers: Mike Yan, Dmitry Kushnikov
Document ID: POL-IS-05
Document Type: Policy
Document application: All Contractors, All Employees
Effective date: January 4, 2023
Status: Published
Tag: ISO27001
Version: 2

# Table of contents

---

# **1. General**

## **1.1 Purpose**

Manychat is responsible for confidentiality, integrity, and availability of its data and data of its customers stored in its systems.

This document sets out the basic principles to address business continuity and disaster recovery requirements in Manychat, including the following areas:

- Business Impact Analysis (BIA);
- Business Continuity Planning;
- Disaster Recovery;
- Back Up & Redundancy;
- BC/DR Plans Testing.

## **1.2 Scope**

This policy applies to all teams, divisions, sections and services of Manychat.

# **2. Business Continuity and Disaster Recovery Policy**

## **2.1 General requirements**

As a leading conversations marketing company, Manychat is required to be prepared to face several adverse conditions (i.e. “disasters”) that can seriously affect continuity of business and  services, and compromise information security and availability of the platform and customer data.

Manychat shall identify critical assets and design adequate Business Continuity and Disaster Recovery plans aimed to safeguards key business processes and its strategy.

## **2.2 Disasters**

Disasters are disruptive events that cause critical information resources and assets to be temporary (the disruption period could be a few minutes to several months) inoperative adversely affecting organizational operations and processes.

A disaster may be caused by natural calamities, such as earthquakes, floods, tornadoes and fire, or a disaster may be caused by events precipitated by humans such as terrorist attacks, hacker attacks, viruses or human errors.

Cybersecurity-related disasters may occur when a disruption in service is caused by loss, including temporary, of business critical and sensitive information availability and integrity (e.g. systems failures, accidental file deletions, untested application releases, loss of backup information, DoS attacks, hacker intrusions or viruses, etc.) executed by adverse actor.

Disasters require recovery efforts to restore operational status and business continuity and appropriate information protection levels, equivalent to the ones implemented during day-to-day operations, shall be ensured also in adverse conditions.

The purpose of business continuity planning (BCP) and disaster recovery planning (DRP) are to enable a business to continue offering Manychat platform services in the event of a disruption and to survive a disastrous interruption to activities.

Business Continuity and Disaster Recovery approach shall be driven by overall business strategy and objectives.

## **2.3 Business Impact Analysis (BIA)**

First step for Business Continuity and Disaster Recovery shall be Business Impact Analysis (BIA) - definition and identification of critical business processes and assets.

1. For each critical business processes and assets Business Impact Analysis (BIA) shall determine:
- information and information processing assets supporting key business processes and assets;
- evaluate risk and impact of:
    - potential loss of information involved in key business processes and assets;
    - downtime of each information processing asset supporting key business processes and services;
- сlassify information processing assets criticality using [Risk Management Procedure](https://docs.google.com/document/d/1Wy_RbmjElKCp6K6SYipBNSsVuLCyarcl/edit?usp=share_link&ouid=105608147576229526248&rtpof=true&sd=true);
- establishes the recovery point objective (RPO) and recovery time objective (RTO) for information processing assets, which respectively defines how much data can be lost in recovery operations and how quickly recovery must be executed.
1. BIA shall be performed regularly (at least yearly) or following main changes (new technologies implementation, new critical processes, major disasters, etc.).

## **2.4 Business Continuity Planning**

To ensure continued business operations during and following any critical incidents that result in a disruption to normal operational capabilities, Business Continuity (BC) plans must be developed  to address scenarios that may arise from the occurrence of disruptive events and incidents.

1. Business Continuity (BC) plans shall be defined for all **Highly critical** information processing assets.
2. BC plans shall at least include:
    - Critical actions and remediation necessary to the enforce business continuity;
    - The human/material resources supporting these critical actions;
    - Procedures for declaring a disaster (escalation procedures);
    - Circumstances under which a disaster should be declared (Note: Not all interruptions are disasters, but a small incident not addressed in a timely or proper manner may lead to a disaster. For example, a virus attack not recognized and contained in time may bring down the entire platform).
    - The clear identification of the responsibilities in the plan.
    - The clear identification of the persons responsible for each function in the plan.
    - The clear identification of contract information.
    - The step-by-step explanation of the recovery process.
    - The clear identification of the various resources required for recovery and continued operation of the organization.
3. BC plans must be documented and shared with respective teams and members. Procedures should include steps for notification of relevant team members and partners.
4. BC plans shall be validated and approved by the Executive team (aka Leadership team).

## **2.5 Backups and Availability of Data**

To ensure the ongoing availability of critical data, scheduled backups and data redundancy mechanisms must be established.

1. Backups shall be used as solution to recover critical information in case of temporary or definitive loss;
2. Backups frequency shall take into account criticality of information:
    - Production environment:
        - Backups of EC2 instances must be performed on a daily basis.
        - Backups of databases must be performed on an ongoing (transaction) basis.
        - Backups of databases and EC2 instances should be stored for at least 5 days.
    - Other environments:
        - Backups of EC2 instances must be performed on a daily basis.
        - Backups of databases must be performed on at least a daily basis.
        - Backups of databases and EC2 instances should be stored for at least 5 days.
3. Backups should be kept at an offsite location different from the main site (AWS Availability Zone);
4. Backups and replications should be monitored for failures. In the event of successive nightly or pervasive failures, the issue must be investigated and resolved in a timely manner;
5. Backup testing and Restore procedures shall be defined and implemented for either explicit data restore, system restore on same system or full system restore.

## **2.6 BC/DR Plans Testing**

Business continuity focuses on keeping business operational during a disaster, while disaster recovery focuses on restoring data and IT infrastructure access after a disaster. To ensure that the business continuity and disaster recovery plans are effective for meeting recovery time objectives, management must conduct an annual test of the plans.

1. All BC/DR plans shall be regularly reviewed and tested.
2. Roles and responsibilities for the annual testing of the BC/DR plans must be defined.
3. Scenarios tested must be documented and outcomes are evaluated against the existing plan.
4. The Head of Security should update the plans based on the test results.
5. The Executive team (aka Leadership team) must share relevant results and updates from the test with the Board of Directors.
6. In the event of an actual live event scenario that requires the plan to be used, no annual testing is required.

# **3. Roles and Responsibilities**

The CEO has the overall responsibility for Information Security at the Company, including information security regarding personnel and IT security.

Process specific roles and responsibilities:

| **Role** | **Role description** |
| --- | --- |
| **All employees** | Employees are responsible to comply with the Standard and report the violations to the Security team. |
| **Managers** | Line managers are responsible to ensure the awareness of this document across their teams. |
| **Security team** | Security team is responsible for regular review, overall awareness, monitoring and investigating violations, and deviations handling. |
| **Infrastructure team** | Infrastructure team is responsible for backups and availability of the production environment, including monitoring of failed backups. |

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
| 0.1 | 20.12.2022 | **Author**: Mikhail Kurzin, Head of Security | Draft  version |
| 1.0 | 04.01.2023 | **Author**: Mikhail Kurzin, Head of Security
**Approvers**:
• Sunny Manivannan, CEO Manychat Inc.
• Dmitry Kushnikov, Head of Technology
• Maria Eremenko, Head of People
• Dan McKelvey, Head of Finance
• Antony Gorin, Head of Infra | Initial version |
| 1.1 | 16.07.2024 | **Author**: Mikhail Kurzin, Head of Security | Document review. No changes were made |
| 2.0 | 06.06.2025 | **Author**: Mikhail Kurzin, Head of Security | 1. Switch to ISO/IEC 27001:2022
2. Document review |