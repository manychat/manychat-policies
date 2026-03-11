# Infrastructure Security Standard

Owner: Mikhail Kurzin
Area: InfoSec, Infra
Approvers: Mike Yan, Dmitry Kushnikov, Antony Gorin
Document ID: STD-IS-10
Document Type: Standard
Document application: All Contractors, All Employees
Effective date: December 20, 2022
Status: Published
Tag: ISO27001
Version: 2

<aside>

**Key points:**

- Network security and firewalling
- Data storage and backups
- Secure configuration baselines (laptops, servers, cloud)
- Monitoring
- User laptops protection
</aside>

<aside>

*This document outlines main safeguards of AWS infrastructure and core workplace equipment to maintain the maximum levels of confidentiality, integrity and availability of Manychat platform.*

</aside>

---

# Table of contents

---

# **1. General**

## **1.1 Purpose**

This document outlines main safeguards of AWS infrastructure and core workplace equipment to maintain the maximum levels of confidentiality, integrity and availability of Manychat platform.

## **1.2 Scope**

This standard applies to all divisions, teams, and services of Manychat and all personnel of Manychat. It also applies to external organizations and their personnel who have been granted access to the Manychat infrastructure and services.

The document is reviewed at least annually to ensure it meets the current business requirements of Manychat, partners, customers, and external organizations.

# **2. Infrastructure Security Standard**

## **2.1 Standard summary**

The standard covers the following technical areas:

- AWS cloud environment protection;
- Additional mechanisms of production Manychat application protection;
- Endpoint devices protection for employee workstations and laptops.

The standard is developed as a reference guideline with the description of desired technical controls implementation based on the most important [CIS 18 Critical Security Controls](https://www.cisecurity.org/controls/cis-controls-list).

## **2.2 Infrastructure Protection**

### 2.2.1 AWS general architecture diagram

![AWS infra architecture 2025.jpg](Infrastructure%20Security%20Standard/AWS_infra_architecture_2025.jpg)

Link to diagram:

https://miro.com/app/board/uXjVKFX-T00=/?share_link_id=778491308506

The architecture is based on the AWS cloud environment. Access control requirements are fulfilled with network controls (security groups) and a granular built-in AWS IAM access-control mechanism.

The AWS infrastructure is hosted in the **EU-central-1** data center located in Frankfurt (Germany).

### 2.2.2 Network security and fire-walling

The network includes the following segments:

1. **Public facing.** The segment contains hosts with public IP addresses. It includes web gateway, load balancers, analytics hosts, API handlers, webhook and service nodes required to provide customer connections.
2. **Private.** The segment contains hosts with no or limited inbound and outbound Internet connectivity. Such segment include:
    1. **Production environment** with databases and application nodes accessible by a restricted list of Manychat employees only through VPN with MFA;
    2. **Development environment**, accessible by the Manychat responsible employees through VPN without MFA;
    3. **Analytics Snowflake environment.** Separate database for analytic purposes accessed through VPN without MFA.

The following mechanisms are used to configure and manage the proper segmentation and network access:

| **Toolset** | **Description** |
| --- | --- |
| [AWS Security Groups](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_SecurityGroups.html) | AWS build-in mechanism that controls the inbound and outbound network traffic for the AWS resources (eg. EC2, RDS). |
| Pritunl VPN | VPN solution with group-based access control mechanism and MFA to provide secure network access to the environment for Manychat employees and third-parties. |
| [AWS IAM](https://aws.amazon.com/iam/) | Provides granular permissions to AWS services and resources on top of the VPN layer. |
| [AWS CloudTrail](https://aws.amazon.com/ru/cloudtrail/) | Changelog of AWS account actions (including changes in Security Groups and AWS IAM). |

### 2.2.3 Tags & Data requirements

All EC2 hosts and RDS databases should be marked with custom tags to indicate the environment they belong to and backup settings:

| **AWS custom tag** | **Tag variables and description** |
| --- | --- |
| **ENV** | **[dev]**
AWS resources related to the development environment and contain no customer data. No production data in development environment is allowed.
**[production]**
AWS resources related to the production environment and contain customer data. 
• Access to production data should be available only to Infra Team;
• Audit logs should be turned on;
• The frequent backups must be scheduled.
The RDS instances requirements: 
• RDS instances should not be publicly accessible by anyone on the internet;
• Access to RDS with any production data  should be available only to Infra Team;
• Audit logs should be turned on;
• The frequent backups must be scheduled.
• For RDS with downtime-sensitive data maintenance windows and update notifications should be set up 
**[internal]**
AWS resources related to the internal environment (internal business systems) and contain no customer data. |
| **ForSnapshot** | **[0,1]** Tag resources  for AWS Data Lifecycle Manager backup policy to automate the creation, retention, and deletion of EBS snapshots and EBS-backed AMIs. |

### 2.2.4 Load balancing

Load balancers are intended to protect the Manychat application against unexpected customer activity, which may result in downtime.

Load balancers are represented with the following solutions and functionality:

| **Load balancer** | **Function** |
| --- | --- |
| OpenResty MC/gate (18.185.191.84) | Intermediate load balancer based on OpenResty stack with LUA script support. |
| Martech ALB | Additional internal Elastic Load Balancer for Amazon ECS services. |
| Main ALB | Edge AWS application load balancer with AWS WAF support. |
| Main NLB | Edge AWS network load balancer. |

### 2.2.5 Infra secure configuration baselines

Manychat uses Level 1 profile CIS benchmarks as a general secure configuration **reference** for different technologies.

The following table describes security baselines utilized for the secure configuration of Manyсhat infrastructure components depending on the technology.

| **Software/Technology** | **Link** | **Notes** |
| --- | --- | --- |
| Ubuntu Linux | [https://www.cisecurity.org/benchmark/debian_linux/](https://www.cisecurity.org/benchmark/debian_linux/)
Manychat-tailored list of settings is located here:
[Ubuntu Security Benchmark](https://docs.google.com/spreadsheets/d/1NnTxupmhPnqFxClEYNPdzPsWXTev1XzDQk0Ecgsf-jk/edit#gid=0) | Includes system specific settings, audit settings, password policy. 

All settings with priority **high** are mandatory to be set up. |
| PostgreSQL | [https://www.cisecurity.org/benchmark/postgresql/](https://www.cisecurity.org/benchmark/postgresql/) | Includes system specific settings, audit settings, password policy. |
| AWS account | [https://www.cisecurity.org/benchmark/amazon_web_services](https://www.cisecurity.org/benchmark/amazon_web_services) | Includes system specific settings, audit settings, password policy. |

### 2.2.5 Logging and Monitoring

The following logging and monitoring solutions are implemented on the **infrastructure** level:

| **Toolset** | **Description** |
| --- | --- |
| [AWS CloudTrail](https://aws.amazon.com/ru/cloudtrail/) | Monitoring of AWS user activity and AWS API usage. |
| [AWS GuardDuty](https://aws.amazon.com/guardduty/) | AWS threat detection solution. |
| [AWS CloudWatch](https://aws.amazon.com/cloudwatch/) | AWS resources performance monitoring and Manychat application monitoring service |
| Tenable.io (Nessus) compliance checks
(cloud.tenable.com) | Compliance scan solution to ensure that hosts are configured in accordance with [secure configuration baselines](https://docs.google.com/document/d/1z8olLv2kQx6jP5pz0hZONJdnxMuLIQjF/edit#heading=h.2qu8jf1j4rbv). 
Nessus agents must be deployed on all AWS production and development servers. |
| Tenable.io (Nessus) vulnerability checks
(cloud.tenable.com) | Vulnerability management and monitoring in accordance with [Vulnerability and Patch Management Standard](https://docs.google.com/document/d/1TiuL37J8oReH-QEKhwpLG2ANMMXOdTwi/edit?usp=share_link&ouid=105608147576229526248&rtpof=true&sd=true). 
Nessus agents must be deployed on all AWS production and development servers. |
| Wazuh Security Platform
(wazuh.Manychat.io) | File integrity monitoring, malware detection, log management, monitoring, threat detection, and alerting of security events and incidents. 
Wazuh agents must be deployed on all AWS production and development servers. |
| AWS EC2 operation systems logging | Build-in OS logging configured in accordance with  [secure configuration baselines](https://docs.google.com/document/d/1z8olLv2kQx6jP5pz0hZONJdnxMuLIQjF/edit#heading=h.2qu8jf1j4rbv). |
| Application level monitoring | Application level events logging and monitoring solution based on Sentry and/or Rollbar. |

## **2.3 User workstations protection**

### 2.3.1 Workstation protection requirements

User workstations of Manychat employees shall be configured to comply with [Office Security Standard](https://www.notion.so/Office-Security-Standard-2b7b12e9aa1a8005ab2edd693784d06f?pvs=21). The list of the software installed on the user workstation includes the following:

| **Application** | **Description** |
| --- | --- |
| AntiVirus solution | **SentinelOne** **EDR** must be installed on all endpoint devices (laptops, desktops).
**XProtect**, a built-in AV protection for MacOS based devices. |
| MDM solution | **JAMF PRO** agents must be installed on all MacOS based devices to control the following:
• HDD encryption;
• Password policy;
• Restricted software;
• Centralized patch management of vulnerable software;
• Remote block or wipe in case of emergency.
**Microsoft Intune** must be enrolled on all Windows-based devices. |
| Vulnerability checks agent | **SentinelOne** **EDR** collects data on OS vulnerabilities. 
**MDM solutions** collect data on unpatched applications. |
| Managed Google Chrome browser | All Google Chrome browsers should be installed in managed mode and connected to Manychat’s Google Workspace.
Only whitelisted Chrome Extensions are approved for installation. |

### 2.3.2 Workstation secure configuration baselines

Manychat uses Level 1 profile CIS benchmarks as a general secure configuration **reference** for MacOS and Windows operation systems.

The following table describes security baselines utilized for secure configuration of Manychat workplace operation components depending on the utilized technology.

| **Software/Technology** | **Link** | **Notes** |
| --- | --- | --- |
| Setting up a new user device | All devices must have MDM solution installed.
New comers user account guideline: [**IT Services Setup Guide**](https://www.notion.so/IT-Services-Setup-Guide-f7ecc5eb4abc4ca7a47e8e97f265da59?pvs=21)  | All mandatory configuration settings are applied by MDM solutions. |
| MacOS | [https://www.cisecurity.org/benchmark/apple_os](https://www.cisecurity.org/benchmark/apple_os)
Manychat-tailored list of settings is located here:
[MacOS Security Benchmark](https://docs.google.com/spreadsheets/d/1yXzmBI2tOqVd6-D5jLl6c5pAAg6BShZ7QgyCK6MS8Ms/edit#gid=0) | Includes system specific settings, audit settings, password policy. |
| Windows OS | [https://www.cisecurity.org/benchmark/microsoft_windows_desktop](https://www.cisecurity.org/benchmark/microsoft_windows_desktop) | Includes system specific settings, audit settings, password policy. |
| Google Workspace | [https://support.google.com/a/answer/7587183](https://support.google.com/a/answer/7587183) | Includes settings for Administrator accounts, User Accounts, Calendar, Chrome browser, Drive, Gmail, Groups |

# **3. Roles and Responsibilities**

The CEO has the overall responsibility for Information Security at the Company, including information security regarding personnel and IT security. The CEO delegates the responsibility for security related documentation to the Head of Security. The Head of Security holds the primary responsibility for ensuring the information security at the Company.

Specific roles and responsibilities:

| **Role** | **Role description** |
| --- | --- |
| **Security team** | Security team is responsible for monitoring overall awareness with this Standard, monitoring, and investigating the violations, and deviations handling. |
| **Head of Infrastructure** | Head of Infrastructure is responsible for management of infrastructure settings in accordance with this Standard and global ownership of Google Workspace environment for Manychat employees. |
| **Helpdesk/Workplace admins** | Helpdesk and workplace admin are responsible to comply with user workstation management requirements and ensure that all required installations have been performed. |

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
| 0.1 | 05.12.2022 | **Author**: Mikhail Kurzin, Head of Security | Draft  version |
| 1.0 | 20.12.2022 | **Author**: Mikhail Kurzin, Head of Security
**Contributors/Approvers**:
• [Sunny Manivannan](mailto:sunny.manivannan@manychat.com), CEO
• [Dmitry Kushnikov](mailto:dmitry@manychat.com), Head of Technology
• [Antony Gorin](mailto:antony@manychat.com), Head of Infra | Initial version |
| 1.1 | 16.07.2024 | **Author**: Mikhail Kurzin, Head of Security | Document review. No changes were made |
| 2.0 | 06.06.2025 | **Author**: Mikhail Kurzin, Head of Security | 1. Switch to ISO/IEC 27001:2022
2. Document review |