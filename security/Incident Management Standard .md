# Incident Management Standard

Owner: Mikhail Kurzin
Area: InfoSec, Infra
Last edited time: January 20, 2026
Approvers: Dmitry Kushnikov
Document ID: STD-IS-07 
Document Type: Standard
Document application: All Contractors, All Employees
Effective date: May 2, 2022
Reviewers: Mikhail Kurzin, Mike Yan, Dan McKelvey, Antony Gorin, Oleg Krasnov, Ido Mart, Anastasia Shchogoleva, Ashraf Bashir, Valeryia Karzhova
Status: Published
Tag: ISO27001
Version: 3

<aside>

**Key points:**

- Incident monitoring
- Cyber attack life cycle
- Containment, eradication, recovery
- Post-incident handling
</aside>

<aside>

*This Standard is a complement to the ISMS Policy and security practices applied by Manychat to its infrastructure, networks, systems, and applications in order to prevent potential cybersecurity incidents from occurring.*

</aside>

---

# Table of contents

---

# 1. General

## **1.1 Purpose**

The purpose of this document is:

- Systematization of information on the life cycle of a cyberattack and response to Information security (IS) incidents;
- Description of the incident response process;
- Description of tools used at each stage of the incident investigation.

## **1.2 Scope**

The Manychat Incident Management Standard takes the following areas into consideration (scope):

- Manychat application;
- Manychat production server infrastructure;
- Manychat mobile applications;
- Partner (eg. Facebook) applications;
- Third-party integrations;
- Manychat internal corporate/office network.

This document doesn't cover non-computer related incidents, such as natural disasters, hardware failures etc.

# 2. Incident Management Standard

## **2.1 Incident response fundamentals**

### 2.1.1 Attack life cycle (Kill Chain)

During the cyber attack, attackers implement a structured sequence of steps, called the Kill Chain. Based on the information of stages of information system compromise, the staff responsible for information security can build relevant protection measures.

![Screenshot 2025-12-05 at 1.29.38 PM.png](Incident%20Management%20Standard/Screenshot_2025-12-05_at_1.29.38_PM.png)

The effectiveness of the investigation and the amount of material and damage inflicted on Manychat depend on the stage at which the Kill Chain was detected. Detection at the stage of “Actions on Objectives” (later detection) means that the information security system was unable to resist the attack and the attacker achieved the set goals. The least damage will be done in the case of detection at the stages of “Delivery” (early detection).

### 2.1.2 Events and Incidents

An **event** is any observable activity occurrence in a system or network. It could be an action taken by a legitimate user, web application updating user configuration in a database, mobile application connecting to a server API, or user report on suspicious activity, etc.

A **malicious event** is an event with a negative impact, such as unauthorized access to user account or business data, crashing a system with a denial of service attack, forging forensic log records etc.

A **security incident** (or just incident) is a violation of Manychat Privacy Policy, ISMS Policy, and general security standards (PCI DSS, ISO27001, etc.), best practices (such as OWASP Top 10), and fair use policies. Incidents include a user exposing information about high-level vulnerabilities in Manychat platform to the public internet, distributed denial of service attack causing downtime or complete system crash, defacement of a public web site etc.

For AI-enabled systems, events and incidents may also include concerns or reports related to unintended behavior, misuse, misleading or harmful outputs, or other adverse impacts arising from the design, configuration, or operation of AI-enabled features, even where no cybersecurity incident has occurred. Such concerns may be reported by users, partners, or internal stakeholders and are handled in accordance with this Standard.

## **2.2 Computer Security Incident Response Team (CSIRT)**

**Computer Security Incident Response Team (CSIRT)** is the main subject of responding to a cyber incident. The main responsibility of the CSIRT is to expose and avert cyber attacks targeting an organization. This is a cross-functional team represented by multiple business team members, covering their appropriate areas of expertise.

### 2.2.1 CSIRT Activation

The CSIRT is activated if an incident has been confirmed to be affecting ManyChat business systems or infrastructure at an enterprise or at multi-team level. Attacks attempts do not necessarily require CSIRT activation.

### 2.2.2 CSIRT Contacts

CSIRT should be contacted by [**security@manychat.com**](mailto:security@manychat.com) email address or [**#security**](https://manychat.slack.com/archives/C02QYCPRF3J) Slack channel.

AI-related concerns or reports of adverse impacts may also be submitted through the same channels and will be assessed and escalated as appropriate.

### 2.2.3 CSIRT Structure

- *CSIRT lead* is responsible for coordinating all the incident response team members, communication with incident reporters, and representation of the CSIRT to the outside third-parties. If an incident was reported, CSIRT lead reports to Management Representative the information on the incident. This role is performed by the Head of Security.
- *Legal/Finance representative* is responsible for reviewing incident outcomes to ensure compliance with federal laws, consulting on legal risks associated with incident and mitigation actions, communication with law enforcement, lawyers and law teams of entities affected by the incident.
- *Management representative* is responsible for coordinating incident response among various stakeholders and ManyChat teams (e.g. Legal/Finance team to discuss legal consequences, Human Resources team in case of internal breach), business continuity decisions, and final decisions on how to proceed with the incident response.
- *Marketing/Public Relations representative* is responsible for communicating incident and the related information and news to the public and affected customers and organizations.
- *Duty representative* is responsible for being available 24/7 hours for capturing incident alert, initial incident response and further communication of information about the incident to the Incident team lead.

### 2.2.4 CSIRT Members

| **Role** | **Name** | **Email/Slack** | **Incident Severity** |
| --- | --- | --- | --- |
| **CSIRT team lead** | Mikhail Kurzin | [kurzin@manychat.com](mailto:kurzin@manychat.com) / @maskishe | P1-P4 |
| **CEO** | Mike Yan | [mike@manychat.com](mailto:mike@manychat.com) / @mike | P1-P2 |
| **Legal/Finance representative** | Dan McKelvey | [dan.mckelvey@manychat.com](mailto:dan.mckelvey@manychat.com) / @dan.mckelvey | P1-P2 |
| **Chief Architect** | Antony Gorin | [antony@manychat.com](mailto:antony@manychat.com) / @antony | P1-P2 |
| **Cross Functional Manager (Development)** | Anastasia Shchogoleva | [ashchogoleva@manychat.com](mailto:ashchogoleva@manychat.com) / @ashchogoleva | P1-P2 |
| **Cross Functional Manager (Backend and Platform related issues)** | Ashraf Bashir | [ashraf.bashir@manychat.com](mailto:ashraf.bashir@manychat.com) / @ashraf.bashir | P3 |
| **Cross Functional Manager (Frontend related issues)** | Valeryia Karzhova | [valeriia.korzhova@manychat.com](mailto:valeriia.korzhova@manychat.com) / @valeriia.korzhova | P3 |
| **Head of Infra** | Dmitry Yackevich | [dmitry.yackevich@partner.manychat.com](mailto:dmitry.yackevich@partner.manychat.com)/@[dmitry.yackevich](mailto:dmitry.yackevich@partner.manychat.com)  | P1-P2 |
| **Head of Support** | Oleg Krasnov | [oleg.krasnov@manychat.com](mailto:oleg.krasnov@manychat.com)
 / @ok | P1-P2 |
| **Marketing/Public Relations** | Ido Mart | [idomart@manychat.com](mailto:idomart@manychat.com)  / @Ido Mart | P1-P2 |
| **Duty representative** | Support team member | **@support-team or [#support_chat](https://manychat.slack.com/archives/CEK9GTEDU)** | P1-P3 |

### 2.2.5 CSIRT services

The main focus of **CSIRT team lead** is incident response, but it is his responsibility to commit to the following services:

- **Intrusion Detection.** The incident analyst assumes responsibility for intrusion detection. The team generally benefits because it should be poised to analyze incidents more quickly and accurately, based on the knowledge it gains of intrusion detection technologies.
- **Advisory Distribution.** CSIRT team leads issues advisories within the organization regarding new vulnerabilities and threats. Automated methods are used whenever appropriate to disseminate information.
- **Education and Awareness.** The more the users and technical staff know about detecting, reporting, and responding to incidents, the less drain there should be on the CSIRT team lead. This information is communicated through many means: workshops, newsletters, Slack posts, etc.

## **2.3 Incident handling**

This section describes the major phases of the incident response process - preparation, detection and analysis, containment, eradication and recovery, and post-incident activity.

### 2.3.1 Preparation

Incident response methodologies typically emphasize preparation - not only establishing an incident response capability so that the organization is ready to respond to incidents, but also preventing incidents by ensuring that systems, networks, and applications are sufficiently secure.

The Security team should ensure the protection of systems and inform users, as well as IT staff, about the importance of security measures. Specialists, responsible for information security, should regularly improve their skills by means of trainings and seminars, should follow the latest security trends and be aware of the latest software and hardware solutions in the field of information security, and be aware of new types of threats and attack scenarios. Internal security awareness programs shall include training materials against common threats.

### 2.3.2 Incident Handler Communications and Facilities

- Corporate business systems inventory with defined system owners and emergency contact;
- Clear communication channels:
    - @support-team in Slack in #emergency, #support-team or #dev in accordance with the [Emergency Protocol](https://www.notion.so/Emergency-Protocol-11fa4eb6b7584a0ca3ecd6bac8632ec5?pvs=21);
    - Slack messenger, dedicated channel: #security;
    - Telephone call/Zoom list entry for coordination;
    - Understanding which parties are to be notified.
- Tracking system for tracking incident information, status, etc.
    - Slack #security, #helpdesk, #emergency, #support-team or #dev channels.

For incidents involving AI-enabled systems, Manychat assesses whether communication to affected users or other interested parties is required based on the nature, severity, and potential impact of the incident. Where applicable, communication is coordinated through the Marketing/Public Relations representative and conducted via appropriate channels, in alignment with legal, contractual, and regulatory obligations.

### 2.3.3 Incident Detection Facilities

- AWS infrastructure Logs and Monitors – (such as Amazon Cloudtrail, Amazon S3 access logs) and security monitoring services (such as Amazon GuardDuty, AWS Security Hub):
    - Amazon CloudWatch alarms (#sec_alerts, #sec_alerts_ai);
    - #infra-alarms and #backend-alarms channel in Slack;
- Security Systems Logs, including:
    - SentinelOne EDR logs;
    - SIEM system logs;
    - MDM systems logs;
    - Secure DNS system logs.
- Billing Activity – A sudden change in billing activity can indicate a security event;
- Support tickets alerting malicious actions;
- [Alarm Protocol](https://www.notion.so/Alarm-Protocol-0caa7d95e38e467d99653b4cca6e0782?pvs=21)s;
- Vulnerability management tools logs;
- Operating systems logs.

### 2.3.4 Incident Domains

There are four domains where security incidents might occur: service, infrastructure, application, and third-party.

- **Service Domain** – Incidents in the service domain affect professional services misuse, such as, billing, technical support, and other areas. A service domain event is one that includes malicious activities driven by the Manychat personnel interacting directly with the customers.
- **Infrastructure Domain** – Incidents in the infrastructure domain include data or network-related activity, such as the traffic in the cloud infrastructure environment and office networks.
- **Application Domain** – Incidents in the application domain occur in the Manychat application code or in software deployed to the services or infrastructure including Manychat application source code.
- **Third-party** - Incidents in a third-party (partner) application that require post-discovery fixes and immediate reactions after the actual discovery, and containment is mostly performed by the supplier.

### 2.3.5 Incident Severity and Prioritization

Severity may be increased as the investigation develops.

| **Severity** | **Criteria** | **Incident Response** |
| --- | --- | --- |
| **Critical** - P1 | Event that causes significant disruption to Manychat infrastructure or services, sensitive/confidential data loss, or reputational impact.
• Business-critical asset are affected and their Maximum Tolerable Period of Disruption (MTPD) are violated
• Business is not operational with no effective workaround
• The outage impacts significant volume of customers
• Significant financial impact (e.g., in-scope financial systems, ransomware, wire fraud)
• Cross tenant contamination, session takeover, exploitation (or even attempts) of any vulnerability above CVSS score 8.5 resulting in loss or exposure of sensitive/confidential data
• Exposure of administrative, privileged or elevated credentials
• Installed malware on high-value assets (e.g. credential harvesting, web shell, RAT - remote access Trojan)
• Confirmed exposure of regulated, sensitive, or highly confidential information, which may include:
    ◦ Personally identifiable information (PII)
    ◦ Billing/Payment information
    ◦ Manychat confidential information
    ◦ Other information that may be reportable or trigger notification requirements
    ◦ Intellectual property, to include source code and bug databases | Notify CSIRT team P1 level members upon discovery of intake and initial assessment after incident detection. |
| **High** - P2 | Event that causes, or has the potential to cause, severe disruption of services, financial, or reputational impact.
• Potential data loss or exposure
• Business is operational with acceptable workarounds
• Remote access/control by unauthorized user
• Includes a partial outage impacting multiple customers
• Possible impact of sensitive/confidential data
• Unauthorized third-party authenticating to Manychat or a Manychat-hosted customer environment
• Cyber-related legal request from an external party
• Validated notification from security researcher or law enforcement about a potential compromise of Manychat or exposure of Manychat data | Notify CSIRT team P2 level members upon discovery of intake and initial assessment after incident detection. |
| **Medium** - P3 | Event that causes, or potentially can cause, partial, non-critical disruption of services to the organization or customers.
• Business is operational with acceptable workarounds
• No critical organizational or customer services are impacted
• No sensitive/confidential data impacted
• Installed malware on non-high-value assets (i.e. credential harvesting, web shell, RAT)
• Remote access/control by an unauthorized user against systems with no sensitive information and no connection to Manychat corporate environment | Notify CSIRT team P3 level members upon discovery of intake and initial assessment after incident detection. |
| **Low** - P4 | Event that causes minor/negligible impact to the organization or customers.  
• No effect to Manychat’s ability to provide services to users and customers
• No customer data affected
• No reputational impact | Notify CSIRT team P4 level members upon discovery |

### 2.3.6 Incident Monitoring

Security and Infrastructure teams continuously monitor security events that could lead to incident discovery.

Incident tracking and live chat rooms are available directly and in shared channels using [Incident Handler Communications and Facilities](https://www.notion.so/Incident-Management-Standard-2c0b12e9aa1a8013bfa3e6f0cf0251ab?pvs=21). Shared communication channels are used to escalate suspicious actions and for report reviews.

The Security team is responsible for maintaining the incident knowledge base.

## **2.4 Incident reporting**

### 2.4.1 Containment, Eradication, and Recovery

One of the first key actions to be taken after the initial investigation (and often as part of that investigation) is to **contain** the damage being done by the cyber security incident.

Containment strategies vary based on the type of incident. Criteria for determining the appropriate strategy include:

- Potential damage to and theft of resources;
- Need for evidence preservation;
- Service availability (e.g., network connectivity, services provided to Manychat clients);
- Time and resources needed to implement the strategy
- Duration of the solution (e.g., emergency workaround to be removed in four hours, temporary workaround to be removed in two weeks, permanent solution).

There are many ways in which a cyber security incident can be **contained**, which include:

- Blocking (and logging) of unauthorized access;
- Blocking malware sources (eg email addresses and websites);
- Closing particular ports;
- Changing system passwords where compromise is suspected;
- Firewall filtering;
- Isolating systems.

After an incident has been contained, eradication is often required to eliminate key components of the incident (eg. removing the attack from the network, deleting malware and disabling breached user accounts), as well as identifying and mitigating vulnerabilities that were exploited.

During the **eradication** process, there are a number of actions you can take, which include:

- Identifying all affected hosts within (and sometimes beyond) your organization, so that they can be remediated;
- Carrying out malware analysis;
- Checking for any response from the attacker to your actions;
- Developing a response (preferably in advance) if the attacker uses a different method of attack;
- Allowing sufficient time to ensure that the network is secure and that there is no response from the attacker.

Effective eradication plans must be executed with speed and precision because attackers often try to re-establish a base and then entrench themselves again into the network once they sense they have been discovered and eradication is underway. Therefore, it is important to ensure that all elements of the attack have been eradicated and that the attackers cannot carry out further attacks.

The final step in responding to a cyber security incident is to **restore** systems to normal operation, confirm that the systems are functioning normally, and remediate vulnerabilities to prevent similar incidents from occurring.

It is therefore important to have an appropriate recovery plan in place, which should include:

- Rebuilding infected systems (often from known ‘clean’ sources);
- Replacing compromised files with clean versions;
- Removing temporary constraints imposed during the containment period;
- Resetting passwords on compromised accounts;
- Installing patches, changing passwords and tightening network perimeter security, such as firewall rulesets;
- Testing systems thoroughly – including security controls;
- Confirming the integrity of business systems and controls.

It is important to validate that systems are operating normally again, which can often be achieved by carrying out an independent penetration test of the affected systems, complemented by a security controls assessment.

All listed actions shall be reported for history.

### 2.4.2 Post-Incident Activity

Holding a “Lessons learned” meeting with all involved parties after a major incident can be extremely helpful in improving security measures and the incident handling process itself.

Multiple incidents can be covered in a single “lessons learned” meeting. This meeting provides a chance to achieve closure with respect to an incident by reviewing what occurred, what was done to intervene, and how well intervention worked.

Questions to be answered in the meeting include:

- Exactly what happened, and at what times?
- How well did staff and management perform in dealing with the incident? Were the documented procedures followed? Were they adequate?
- What information was needed sooner?
- Were any steps or actions taken that might have inhibited the recovery?
- What would the staff and management do differently the next time a similar incident occurs?
- How could information sharing with other organizations have been improved?
- What corrective actions can prevent similar incidents in the future?
- What precursors or indicators should be watched for in the future to detect similar incidents?
- What additional tools or resources are needed to detect, analyze, and mitigate future incidents?

Small incidents need limited post-incident analysis, with the exception of incidents performed through new attack methods that are of widespread concern and interest. After a serious attack has occurred, it is usually worthwhile to hold post-mortem meetings that cross team and organizational boundaries to provide a mechanism for information sharing.

Reports from these meetings are good material for training new team members by showing them how more experienced team members respond to incidents. Updating incident response policies and procedures is another important part of the lessons learned process.

Another important post-incident activity is creating a follow-up report for each incident, which can be quite valuable for future use. The report provides a reference that can be used to assist in handling similar incidents.

# 3. Roles and Responsibilities

The CEO has the overall responsibility for Information Security at the Company, including information security regarding personnel and IT security.

Specific roles and responsibilities:

| **Role** | **Role description** |
| --- | --- |
| **All employees** | Employees are responsible to comply with the Standard and report the violations and suspicious actions to the Security team. |
| **Managers** | Line managers are responsible to ensure the awareness of this Standard across their teams. |
| **Security team** | Security team is responsible for monitoring overall awareness with this Standard, monitoring, and investigating the violations, and deviations handling. |

# 4. Compliance

The proof of ISMS quality is the receipt and maintenance of the certificate of ISO/IEC 27001:2033 «Information Technology. Security techniques. Information security management systems. Requirements» compliance.

Manychat must comply with multiple state regulatory requirements of countries, Manychat operates in, such as:

- The General Data Protection Regulation (GDPR) (Regulation (EU) 2016/679);
- Personal data protection regulation in the countries or regions of operation (eg. CCPA);
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
| 0.1 | 22.02.2022 | **Author**: Mikhail Kurzin, Head of Security
**Approvers**:
• [Mike Yan](mailto:mike@manychat.com)
• [Dmitry Kushnikov](mailto:dmitry@manychat.com)
• [Antony Gorin](mailto:antony@manychat.com)
• [Maria Eremenko](mailto:eremenko@manychat.com)
• [Anastasia Shchogoleva](mailto:ashchogoleva@manychat.com)
• [Mikhail Mazein](mailto:m.mazein@manychat.com) | Draft  version |
| 1.0 | 02.05.2022 | **Author**: Mikhail Kurzin, Head of Security
**Contributors**:
• [Antony Gorin](mailto:antony@manychat.com), Head of Infra
• [Anastasia Shchogoleva](mailto:ashchogoleva@manychat.com), Head of Operations | Initial version |
| 1.1 | 16.07.2024 | **Author**: Mikhail Kurzin, Head of Security | 1. Updated branding.
2. CSIRT Members reviewed |
| 2.0 | 09.06.2025 | **Author**: Mikhail Kurzin, Head of Security | 1. Switch to ISO/IEC 27001:2022
2. Document review |
| 3.0 | 20.01.2026 | **Author:** Sergey Muslaev, GRC Lead | Updating document in accordance with ISO/IEC 42001:2023 |