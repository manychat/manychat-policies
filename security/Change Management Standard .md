# Change Management Standard

Owner: Mikhail Kurzin
Area: AI, InfoSec, Infra
Last edited time: January 22, 2026
Approvers: Mike Yan, Dmitry Kushnikov, Antony Gorin
Document ID: STD-IS-09
Document Type: Standard
Document application: All Contractors, All Employees
Effective date: December 14, 2022
Reviewers: Mikhail Kurzin, Anastasia Shchogoleva
Status: Published
Tag: ISO27001, ISO42001
Version: 3

<aside>

**Key points:**

- Infra configuration changes
- Secrets changes
- Firewall changes
- Change testing and rollback procedure
</aside>

<aside>

*Manychat is responsible for confidentiality, integrity and availability of customers data, as well as for high availability of the product. Changes made by employees in the configuration of the production environment can directly affect the security and availability of the product and therefore should be made in accordance with the basic principles described in this document.*

</aside>

---

# Table of contents

---

# **1. General**

## **1.1 Overview**

Manychat processes its proprietary data, as well as clients’ data, in information systems.

For successful work, it is vitally important to maintain continuity of provided services, and confidentiality, integrity and availability of data.

In order to achieve best quality of provided services to customers, Manychat has a strong focus on compliance to best industry standards and practices, and state regulations of countries in which Manychat operates.

## **1.2 Purpose**

The purpose of this standard is to describe the responsibilities, requirements, and procedures to be followed when any changes to the Manychat production environments are to be made.

This policy is designed to provide a managed and orderly method in which changes to the information technology environment are requested, tested and approved prior to installation or implementation.

The purpose is not to question the rationale of a change, but to ensure that all elements are in place, there is no negative impact on the infrastructure, all the necessary parties are notified in advance and the schedule for implementation is coordinated with all other activities.

## **1.3 Scope**

This standard applies to all divisions, teams, and services of Manychat and all personnel of Manychat. It also applies to external organizations and their personnel who have been granted access to the Manychat infrastructure and services.

**AI-enabled application changes**, including the introduction of new AI-enabled features, material changes to existing AI functionality, or changes affecting the behaviour, configuration, or integration of AI-enabled systems.

The document is reviewed at least annually to ensure it meets the current business requirements of Manychat, partners, customers, and external organizations.

### **In Scope**

The intended scope of the Change Management Policy is to cover all of the company’s computing systems and platforms in the **production** environment.

The primary functional components covered in the Change Management policy include:

- **AWS infrastructure** – Deployment of EC2 virtual machines, RDS databases, and other IaaS components.
- **Hardware** – Installation, modification, removal or relocation of computing equipment.
- **Software** – Installation, patching, upgrade or removal of software products.
- **Database** – Changes to databases or files such as additions, reorganizations and major maintenance.
- **Application** - Manychat application changes being promoted to production as well as the integration of new application systems and the removal of obsolete elements.

### **Out of Scope**

There are many tasks performed at the company, either by the Infra team or by the end users that do not fall under the policies and procedures of Change Management. Tasks that require an operational process, but are outside the initial scope of the company’s Change Management process includes:

- Contingency/Disaster Recovery;
- Changes to non-production elements or resources;
- Changes made within the daily administrative process;
- Application deployment process.

# **2. Change Management Standard**

Change Management is the process of requesting, analyzing, approving, developing, implementing, and reviewing a planned or unplanned change within the IT infrastructure. The Change Management process begins with the creation of a **Change Request** (or **Request for Change**) in the “Infra team” section of the [Manychat Service Desk](https://manychat.slack.com/apps/A037JEBA7BJ-manychat-servicedesk?tab=more_info) Slack application.

The change request must include enough detail so that all teams know the relative impact of the change and how it may affect other areas. Change Request should include the following data depending on the change type: description of the change, components affected, business need, and resource requirements.

All artifacts and communication details should be tracked in the [Manychat Service Desk](https://manychat.slack.com/apps/A037JEBA7BJ-manychat-servicedesk?tab=more_info) Slack application and corresponding YouTrack project. The process ends with the satisfactory implementation of the change and the communication of the result of that change to all interested parties.

Change management request types include:

- DNS changes;
- Gate web balancer changes;
- Run SQL query in prod RDS;
- Change environment configuration;
- Create AWS resource (EC2, RDS, etc.);
- Change AWS security group settings (network access);
- Key/token/secret management;
- Other requests.

The current version of the Standard displays the current status and goals to which the Company is aiming. We plan to work continually on improving this Standard to ensure greater transparency, manageability, documentation and security of the process.

It’s optional to create a Change Management request if the request is initiated by the Infrastructure team.

## **2.1 Technical Impact Analysis**

Technical Impact Analysis  is intended to evaluate and validate the technical feasibility, risk and effect a change can have on the production environment and user productivity.

This section describes the criteria a technical reviewer (**Technical Approver** or **Infrastructure team** member) should consider when evaluating the technical impact of a change.

For changes involving AI-enabled features or functionalities, the technical impact analysis shall also consider AI-related risks and potential impacts on individuals or groups, alignment with the organization’s AI objectives, and any changes to intended use or foreseeable misuse. Where applicable, completion or update of the AI Risk & Impact Assessment is required prior to implementation.

The technical reviewer should consider the following criteria while reviewing any change:

- Evaluate the effect of the change during and immediately after the change implementation.
- Review the technical completeness of the change description, including impact on start-up or shut down of systems, impact on disaster recovery plans, back-up requirements, storage requirements, and operating system requirements.
- Evaluate the technical feasibility of the change and the whole impact of the change in terms of:
    - Performance;
    - Capacity;
    - Security;
    - Operability.

After the technical impact assessment is complete, the reviewer **optionally** should assign a technical impact level to the change in YouTrack RfC issue comments.

The technical impact levels are described in the sections below:

- **Low** – For routine categories, the technical impact default is low.
    - Low complexity;
    - Low risk to system availability;
    - Easy implementation and rollback;
    - No impacts to service level agreements.
- **Medium** – The components of a medium technical impact include:
    - Significant complexity;
    - Moderate risk to system availability;
    - Some complexity to implementation and back-out plans;
    - Affects application, data or server security;
    - Impacts service level agreements (e.g. Business Non-Prime Time).
- **High** – A technical impact is considered to be classified as high if the following criteria apply to the change:
    - High complexity;
    - High risk to system availability;
    - Complex implementation and back-out plans;
    - Affects application, data or server security;
    - Impacts service level agreements (e.g. Business Prime/Peak Time).

The change implementer should act depending on the technical impact level of the change:

- **Low**:
    - It is possible to make changes during Business Prime/Peak Time.
- **Medium**:
    - Changes should be made, If possible, not in Business Prime/Peak Time,
    - For application related changes, the support team should be notified immediately before starting work.
- **High**:
    - Changes must be made not in Business Prime/Peak Time, during maintenance window,
    - Special attention should be paid to the rollback procedure,
    - All the necessary specialists from other teams should be involved in the planned work to check and validate change result,
    - For application related changes, the support team should be notified no later than 24 hours before the planned work and immediately before the start of work.

Notification of the **Change Requester** is required after change implementation.

## **2.2 Change testing and rollback procedure**

All Change Requests with a **high** technical impact level should undergo some level of testing. The change should be built, configured and integrated in the development environment before moving to the production environment. Testing phase focuses on quality assurance to ensure reliability and performance of all components of the Manychat application and technology infrastructure.

Development of the rollback plan is essential to ensure effective recovery in the event of a failed change. The rollback plan is primarily based on the technical impact analysis and the implementation plan.

## **2.3 Secrets and tokens changes**

Secrets, encryption keys and tokens are part of the configuration of the environment and their changes must be carried out in accordance with the Change Management procedure described in previous sections with the following additions:

- It is not allowed to disclose the contents of secrets of the production environment to employees outside the Infrastructure team.
- Secrets for the production environment that have been obtained for use not by the members of the Infrastructure team should not be used (as they are already known to third parties and/or other team members).
- Wherever possible, the configuration of secret rotation should be applied.
- When changing secrets, it is necessary to ensure that the previous version of the secret is kept so that the changes can be undone.

## **2.4 Security Groups changes**

AWS Security Group firewall rules are part of the configuration of the environment and their changes must be carried out in accordance with the Change Management procedure described in previous sections with the following additions:

- it is desirable to include YouTrack task number of the change in the Security Group and/or Security Group Rule description,
- current policies should be reviewed annually to identify and remove outdated rules and Security Groups.

## **2.5 Patch and update management**

Patch management is the practice of updating software with new pieces of code or packages – most often to address vulnerabilities that could be exploited but also to address other problems in the existing programs or add new functions to it.

Infrastructure team of Manychat must be notified about security issues via a centralized notification mechanism provided by Tenable vulnerability management system and Nessus agents distributed on all assets of Manychat’s AWS production and development infrastructure. Overall report provided by the Tenable system shall be used to evaluate the current patching levels of all systems and to assess the current level of risk.

In addition to describing the details of the security issues found, the report should contain a classification of these issues. Depending on the severity level of the problem, patches containing their fixes can be divided into the following categories:

| **Severity** | **CVSSv2 Range** | **CVSSv3 Range** |
| --- | --- | --- |
| Critical | The highest vulnerability score is 10.0. | The highest vulnerability score is between 9.0 and 10.0. |
| High | The highest vulnerability score is between 7.0 and 9.9. | The highest vulnerability score is between 7.0 and 8.9. |
| Medium | The highest vulnerability score is between 4.0 and 6.9. | The highest vulnerability score is between 4.0 and 6.9. |
| Low | The highest vulnerability score is between 0.1 and 3.9. | The highest vulnerability score is between 0.1 and 3.9. |

In addition, it is necessary to assess the possibility of exploiting the vulnerability and divide the hosts into the following groups:

- **Public-facing** - publicly available vulnerable components, with the possibility of remote exploitation of vulnerability.
- **Internal** - not available for public access, with the possibility of remote exploitation of vulnerability through client data processing.
- **Others** - not available for public access, without possibility of remote exploitation.

To the extent possible, the patching process must follow the timeline in the table below:

| **Patch Category** | **Patch completed** | **Patch completed** | **Patch completed** |
| --- | --- | --- | --- |
|  | **Public-facing** | **Internal** | **Others** |
| Critical | Within 24 hours of patch release | Within 7 days of patch release | Within 7 days of patch release |
| High | Within 7 days of patch release | Within 30 days of patch release | Within 3 weeks of patch release |
| Medium | Within 60 days of patch release | Within 4 months of patch release | Within 4 months of patch release |
| Low | Within 1 year of patch release | Within 1 year of patch release | Within 1 year of patch release |

Timely implementation of non-security related patches should be conducted to mitigate against degradation of functionality and/or interoperability. Examples of non-security patches include software updates to increase functionality.

Patch management process should meet the following requirements:

- deployment of security patches is to be prioritized over non-security patches, where possible;
- test for the stability and functionality of patches before deployment;
- non-security patch management is the part of standard change management flow described above;
- some patches require server reboot, which must be planned and carried out in the maintenance windows.

## **2.6 Emergency changes**

Emergency changes exist only as a result of:

- there is a severe degradation of service needing immediate action;
- there is an outage in communication;
- Manychat application is inoperable and the failure causes a negative impact;
- a response to AWS region or subsystems loss;
- a response to an emergency business need.

All emergencies are handled on an as-required basis with the approval of or by the Infrastructure team and must follow the guidelines below.

Inform the Infrastructure team either before or immediately after the change/event occurs.

The emergency request description should include the following information:

- what application component was affected;
- what users have been affected;
- should third-party service providers be notified (eg. Facebook, Twillio, Sendgrid, Stripe);
- if there is a possible work around until the problem is resolved;
- approximate time event or change occurred;
- the approximate length of the outage;
- notification of resolution, if any;
- any error messages or alerts, if applicable.

Change request form submission **before the change** is optional in case of emergency changes. The service restoration should be a priority. Emergencies after normal business hours, on the weekend or holidays, should be resolved immediately. A completed change request form must be submitted through the [Manychat Service Desk](https://manychat.slack.com/apps/A037JEBA7BJ-manychat-servicedesk?tab=more_info) slack application  on the first work day immediately following when the change was made or the event occurred.

Infrastructure team will review all emergency requests to ensure the change meets the criteria for an “emergency change” and to prevent the process from becoming normal practice to circumvent the Change Management process.

# **Roles and Responsibilities**

The CEO has the overall responsibility for Information Security at the Company, including information security regarding personnel and IT security. The CEO delegates the responsibility for security related documentation to the Head of Security. The Head of Security holds the primary responsibility for ensuring the information security at the Company.

Specific roles and responsibilities:

| **Role** | **Role description** |
| --- | --- |
| **All employees** | Employees are responsible to comply with the Standard and report the violations to the Security team. |
| **Managers** | Line managers are responsible to ensure the awareness of this Standard across their teams and direct reports (whether those direct reports are permanent employees, contractors, sub-contractors or agency personnel). |
| **Security team** | Security team facilitates and monitors compliance to the Standard, employs infrastructure safeguards and security controls, and provides vulnerability scanning. In addition, it investigates violations and tracks deviations to the Standard. |
| **Infrastructure team** | Infrastructure team is responsible for:
• Reviewing Requests for Changes for infrastructure,
• Planning and Implementing a change,
• Participating in roll-back actions, if needed. |
| **Change Requester** | A person who initiates a Request for Change; this person should be a Manychat employee related to Manychat product development, protection, maintenance, support, etc. |
| **Technical Approver** | Optional person who confirms the correctness and safety of the changes from a technical point of view	after launch of RfC by Change Requester and before assignment to the ****Infrastructure team. |

# **4. Compliance**

The proof of ISMS quality is the receipt and maintenance of the certificate of ISO/IEC 27001:2022 «Information Technology. Security techniques. Information security management systems. Requirements» compliance.

Manychat must comply with multiple state regulatory requirements of countries, Manychat operates in, such as:

- The General Data Protection Regulation (GDPR) (Regulation (EU) 2016/679);
- Personal data protection regulation in the countries or regions of operation (including CCPA and Law of Armenia on protection of personal data (Regulation ЗR-49-N));
- Canada’s Anti-Spam Law (or “CASL”);
- The CAN-SPAM Act;
- other mandatory state regulatory acts including acts on commercial secrets and intellectual property.

## **4.1 Enforcement**

Implementation and enforcement of this standard is ultimately the responsibility of all employees at Manychat. Security team may conduct ad-hoc checks to ensure compliance with this document without notice. Any violation shall require immediate corrective action. Violations shall be noted in the Manychat applications and responsible employees shall be dispatched to remediate the issue.

For Manychat employees, breaches of this standard may result in disciplinary action being taken and will be dealt with under the disciplinary process in accordance with state laws and regulations of the residence country. Any serious breaches or repeated breaches of this policy may be deemed by Manychat as gross misconduct and may result in disciplinary sanctions, including a remark, reprimand, and dismissal from work.

## **4.2 Exceptions**

Exceptions to this standard must be processed in accordance with the deviation handling rules by the Security team. All exceptions must be maintained taking into account associated risks, exceptions, and recorded approvals. Continuously detected deviations may trigger the changes or improvements of the measures defined in this document.

# **Document History**

| **Version** | **Date of**
**Change** | **Author and Contributors** | **Changes to the previous version** |
| --- | --- | --- | --- |
| 0.1 | 28.11.2022 | **Author**: Mikhail Kurzin, Head of Security | Draft  version |
| 1.0 | 14.12.2022 | **Author**: Mikhail Kurzin, Head of Security
**Contributors/Approvers**:
• [Sunny Manivannan](mailto:sunny.manivannan@manychat.com), CEO
• [Dmitry Kushnikov](mailto:dmitry@manychat.com), Head of Technology
• [Antony Gorin](mailto:antony@manychat.com), Head of Infra
• [Mikhail Mazein](mailto:m.mazein@manychat.com), Head of Engineering | Initial version |
| 1.1 | 16.07.2024 | **Author**: Mikhail Kurzin, Head of Security | Document review. No changes were made. |
| 2.0 | 06.06.2025 | **Author**: Mikhail Kurzin, Head of Security | 1. Switch to ISO/IEC 27001:2022
2. Document review |
| 3.0 | 22.01.2025 | **Author:** Sergey Muslaev, GRC lead | Document amendment in compliance with ISO/IEC 42001:2023 |