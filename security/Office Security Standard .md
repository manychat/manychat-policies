# Office Security Standard

Owner: Mikhail Kurzin
Area: InfoSec
Last edited time: December 15, 2025
Approvers: Mike Yan, Dmitry Kushnikov, Antony Gorin
Document ID: STD-IS-02
Document Type: Standard
Document application: All Contractors, All Employees
Effective date: December 12, 2022
Reviewers: Ivan Toropitsin, Anastasia Shchogoleva, Georgy Chistyakov, Mikhail Kurzin
Status: Published
Tag: ISO27001
Version: 4

<aside>

**Key points:**

- Hardware and Software Acceptable Use
- Clean desk
- BYOD usage
</aside>

<aside>

*This policy sets the key principles and requirements that must be followed by all Manychat employees during daily work for effective and acceptable use of customer and Manychat data, equipment, systems, and networks.*

</aside>

---

# Table of contents

---

# **1. General**

## **1.1 Purpose**

This standard sets the key principles and requirements that must be followed by all Manychat employees for effective and acceptable use of customer and Manychat data, systems, and networks.

## **1.2 Scope**

This standard applies to all divisions, teams, and services of Manychat, as well as to all personnel of Manychat. It also applies to external organizations and their personnel who have been granted access to the Manychat infrastructure and services.

The document is reviewed at least annually to ensure it meets the current business requirements of Manychat, partners, customers, and external organizations.

# **2. Office Security Standard**

## **2.1 General requirements**

1. Authorized access to Manychat information resources (such as laptops, PCs, business systems, services, information, and data including paper information) is provided on a **need-to-know basis**. This means that an employee has access to the information required for his/her job role and not more. The need-to-know basis is the main rule which needs to be followed when deciding whether to give such access or not. It is pleasurable to know something, but is it really important for your work? If your answer is no, do not transfer or use this information.
2. Access requests to any Manychat information resources must be approved by the line manager and/or Security team.
3. All your actions must comply with Manychat policies and standards that are focused on compliance with state regulations and legislations in our and clients’ countries of operation.
4. You will be supplied with cybersecurity awareness materials and necessary training at employment. You should finish the trainings and acknowledge assigned cybersecurity documents within 3 weeks after employment and then annually. The training completion rate is monitored. So it is your responsibility to complete the training on time. Without completion of these training sessions your access requests could be rejected or postponed till the training completion.
5. All verbal, written and electronic information related to Manychat business and/or processed in Manychat business systems (including your work equipment, e.g. company owned laptops, PCs, mobile devices) is considered as Manychat property and must be protected in accordance with Manychat security standards and procedures.
6. You must keep the personal, customer, and sensitive data, including passwords and credentials, in secret, and distribute them in accordance with classification and sensitivity level. Information processed within Manychat information resources may not be disclosed, unless it is classified as Public and approved for public disclosure.
7. It is strictly prohibited to perform any kind of abuse of Manychat business systems or resources. In case you discover any vulnerability in a business system or another company resource, you must notify the Security team for further investigations.
8. Any attempts to unauthorized access to Manychat systems, services, data, and assets must be reported to the Security Team immediately ([security@manychat.com](mailto:security@manychat.com) or [#security](https://manychat.slack.com/archives/C02QYCPRF3J) Slack channel). Employees, partners, and suppliers are obliged to immediately report potential security violations since Manychat has contractual obligations to protect clients’ data.
9. All contact with media must be performed after Corporate Communications (Marketing or HR Branding) approval only. If you do not have authorization from this department, do not communicate with the media. Use your social media profiles wisely: do not speak on behalf of the company and beware that your personal opinion may be associated with the company name.

## **2.2 User ID and Password**

1. Unique user IDs (user account) must be used to access Manychat resources, servers, systems, services, equipment, and network devices. We use mandatory **first_name.last_name@manychat.com** pattern for Okta SSO account and primary email, but in addition email alias can be created in order to meet personal preferences.
2. All actions performed under a personal user account are considered on behalf of the user. The main user’s responsibility is to keep credentials secret and safe and not disclose them for any reason. It is prohibited to share your credentials to any third-party.
3. Use only your work email address (@manychat.com) and Okta SSO connected to your work email to access any resources for your job responsibilities. If you use credentials associated with your personal (non-work) account for job responsibilities (except personal AppleIDs and GitHub accounts), this may be considered a violation, because your personal accounts operate under different Legal Terms.
4. Do not use your work email for registration in personal applications (eg. mobile) and systems.
5. User password must be changed at first login. If Okta SSO is not supported, the following password requirements should apply:
    - Is not based on the account name;
    - Contains at least 12 characters;
    - Contains characters from all of the following categories:
        - Uppercase alphabet characters (A-Z);
        - Lowercase alphabet characters (a-z);
        - Arabic numerals (0-9);
        - Special characters (!"#$%&'()*+,-./:;<=>?@[\]^_`{|}~).
6. Business system owners should set up password security settings (such as its length, complexity, lifetime, etc.) in accordance with [Access Management Standard](https://docs.google.com/document/d/107t5c16Z8rrsslBNchNpilKHZzfnPutg/edit#). requirements.
7. You must not tamper, forge or alter personal user accounts to get unauthorized access to data, systems, or services.
8. Attempts of privilege escalations must be reported to the Security team immediately ([security@manychat.com](mailto:security@manychat.com) or [#security](https://manychat.slack.com/archives/C02QYCPRF3J) Slack channel).
9. User passwords must not be stored in plain text on your computer or on any other device.
10. You are allowed to use a password manager with the following requirements:
    - Only Bitwarden password manager is allowed.
    Bitwarden must be configured according to the company security requirements.
    Step-by-step setup instructions for new users are available here:
    [https://www.notion.so/manychat/Password-Manager-Setup-Step-by-step-Bitwarden-install-for-new-users-190b12e9aa1a804fa8b0e14d3efa2bcf?source=copy_link](https://www.notion.so/Password-Manager-Setup-Step-by-step-Bitwarden-install-for-new-users-190b12e9aa1a804fa8b0e14d3efa2bcf?pvs=21)
11. The secure exchange must be used for user credentials and technical secrets (eg. API-tokens, service credentials) transmission in order to avoid unintended disclosure (e.g. direct message that must be erased after acceptance or temporary password that should be changed on the first log-on).

## **2.3 Electronic Email and Instant Messenger**

1. Only approved communication methods must be used within Manychat. You get access to the necessary services on your day one (Gmail, Slack, Zoom, Notion, task manager, etc.). Consult with HelpDesk (#helpdesk Slack channel) to ensure that the service is approved for corporate communications.
2. All email attachments are checked for viruses. This check is done automatically via Google services.
3. Any external, personal, or 3rd party email or IM accounts must not be used for communication or for sending/receiving any personal, customer, sensitive and Manychat corporate data if it is not classified as Public.
4. Use the “Reply to all” function carefully. Avoid sending any content on behalf of Manychat, which may discredit yourself and the company. You should also set the "**Undo Send:**" cancellation period in Gmail for your personal confidence. It will give you some time to revoke the email if for some reason it was sent by mistake.
5. It is strictly prohibited to share junk links, spam, pornography, obscene, depicting death or injuries to people or animals, gambling, terrorism, and illegal activities, fraud, offensive materials or weapons, forging, hacking, cracking, and other inappropriate content using Manychat corporate communication channels.
6. If you suspect a malicious email, please, report it to the Security team (using [#security](https://manychat.slack.com/archives/C02QYCPRF3J) Slack channel or "Report phishing/spam" option in Gmail).

## **2.4 Internet and Intranet use**

1. Manychat corporate internet or intranet (a.k.a. office network) should not be used for non-work-related activities, including actions with potential harmful impact on Manychat.
2. A user in Manychat corporate internet or intranet must not use any anonymized sites, peer-to-peer file sharing sites, and sites that can cause a security risk to Manychat IT infrastructure.
3. Avoid entering any kind of credentials on login pages with an HTTP (non-encrypted) connection or on any untrusted sites or applications.
4. All files downloaded from the internet (especially from mirrors and other untrusted websites) or received from customers are considered to be untrustworthy and should be checked by antivirus software or service (eg. VirusTotal.com) before use or sharing.
5. Software, especially executable code, binaries, and web extensions (extensions in system marketplaces, e.g. Zoom, Slack, Google Chrome, etc.), should be activated on computers after appropriate HelpDesk approval. Usage of non-licensed software and firmware is illegal and prohibited.

## **2.5 Workspace**

1. The screen of the user's desktop or laptop must be locked when the user is away. On MacBooks, you can use the Touch ID button to put the laptop in sleep/lock mode. On Windows laptops, you can use the "Win"+"L" hotkey combination.
2. Printed and uncontrolled copies of electronic records should be disposed of if unused. Paper copies with confidential data should be stored in lockers.
3. Office equipment. Take special care of sensitive documents printed in shared printer areas. It is very easy to forget sensitive documents in a public place. Do not leave it in the printers and copiers longer than is absolutely necessary. Before leaving work, remove all (especially classified) documents from printers and copiers.

## **2.6 Remote access**

1. The remote access to Manychat IT infrastructure is allowed only to authorized users with appropriate approval for limited actions.
2. The general rule of accessing any business system is to use your corporate computer.
3. The customer and sensitive data, including payment cardholder or financial data, must not be copied or moved into local hard drives or removable media, except with explicit permission for appropriate and approved business needs.
4. Privileged remote access (eg. root ssh access) to Manychat IT infrastructure must be provided via VPN.
5. Web access to SaaS business systems must be provided with corporate Google SSO/SAML login, if technically supported. For critical SaaS business systems MFA/2FA should be enforced.
6. P2P or other Torrent protocols are prohibited.
7. When working remotely, follow the same security rules as in the office. When leaving the laptop, always lock the screen. Do not leave mobile equipment out of sight and never allow third parties (including family members) to use your corporate devices.

## **2.7 Networks**

1. Only the Manychat office network and Wi-Fi network should be used in Manychat offices.
2. Public Wi-Fi networks should be avoided. If used, don't provide login/password credentials through unencrypted connection and use a corporate VPN solution to protect network traffic.
3. A user must not tamper and alter (including forging) any Manychat equipment or network devices without explicit permission from HelpDesk.
4. A user must not tamper and alter (including forging) any content of any network traffic within Manychat office and Wi-Fi networks. This includes the identity of the sender or the recipient, message headers and body, etc.
5. Any illegal actions within the corporate network, including usage of sniffers, spyware, malicious software, etc., will lead to disciplinary sanctions in accordance with internal policies and local laws and regulations.

## **2.8 User equipment: Desktops, Laptops, and personal devices**

1. Only approved devices (desktops and laptops) must be used to connect to Manychat networks or business systems.
2. Only encrypted removable media devices must be used by Manychat employees. It is recommended to use corporate cloud drives (Google Drive) for secure sharing instead of removable media.
3. All corporate desktops, laptops, and mobile devices must have an encrypted file system.
4. All corporate workstations and laptops must be running with approved antivirus software.
5. All corporate Apple workstations, laptops, tablets and phones must be running with approved MDM software (Jamf Pro).
6. A user must always ensure that his corporate equipment (e.g. laptop, mobile phone, tablet) is secured even when it is not in use.
7. Corporate personal equipment must not be left unattended in any public place (e.g. cafe).
8. The loss or theft of any equipment or devices storing Manychat data or data of Manychat customers, or corporate assets must be reported to Security team ([security@manychat.com](mailto:security@manychat.com) or [#security](https://manychat.slack.com/archives/C02QYCPRF3J) Slack channel) as soon as possible.
9. If you lost a personal mobile device with a corporate MFA code generator (eg. Google Authenticator), you must report immediately to reset your authenticator. In case you use your personal phone number for work purposes, make sure you reissue your sim card as soon as possible to avoid compromising one-time codes sent through SMS.
10. You are responsible to ensure backup of your data. For your ease, you may store your work files in the folder synced with corporate systems (eg. Google Drive, GitHub).
11. You are responsible to verify sensitive data on your screen cannot be read by unauthorized persons. Be alert about passers-by. If you have to leave your workspace or interrupt your work with a computer for a longer time, lock your computer screen, clear away all sensitive information from your desk.
12. If you have problems with your PC, please reach out to HelpDesk for assistance. Never perform on your own any actions that require disassembly of your device. Don’t make decisions on repairing your PC in an external repair center without consulting HelpDesk first. Manychat has a right to charge you with costs caused by loss of warranty or outage of equipment by your fault.
13. OFAC’s Economic Sanctions Enforcement Guidelines prohibits American companies from conducting various levels of interactions with specific countries and individuals. If you travel to countries or regions that are on the US sanctions list (Syria, Cuba, Iran, Crimea Region of Ukraine, North Korea, etc.) or travel to Russia/ Belarus, you must hand over your corporate device to HelpDesk before the travel.

## **2.9 Software and Applications**

1. Use only officially approved business systems, software, and Operating Systems. If you need to use a new tool, it must either (a) go through Vendor Security Assessment in [Zip](https://manychat.ziphq.com/) as part of the procurement process, or (b) if the tool is freeware/shareware or otherwise free, discuss it with HelpDesk.
2. Do not use unlicensed software in any case. If you have doubts about the selected software, please contact the HelpDesk team ([#helpdesk](https://manychat.slack.com/archives/CQCQSPK0B) Slack channel).
3. Any software should be used only in accordance with the End-user license agreement.
4. Commercial software including Operating Systems, end-user application, testing, and development tools must be purchased in accordance with Manychat internal procurement process.
5. It is not allowed to use any software licensed to any person or third party except Manychat and its direct contractors. Any kind of license misuse may lead to legal issues for both the user and the company.
6. Be careful when you download executable files and use files from unknown or untrusted sources. They can contain harmful code or viruses.
7. When starting any kind of trial, it is strictly prohibited to upload any kind of real Manychat data in test systems, unless it is approved by the Security team. Comprehensive trials must follow the same process as if it was a software purchase.
8. Software and Applications must be up to date and automatic updates must be enabled unless the Security team approves the opposite.
9. Use of any SaaS applications that are not explicitly approved and listed in Manychat’s business systems inventory is prohibited. 
Any new SaaS service—whether paid, free, or trial—must be reviewed and approved before use. Paid services must undergo a Vendor Security Assessment through Zip. 
Free, trial, or freeware SaaS must be reviewed and approved by the Security team prior to use.
10. It is prohibited to create, deploy, or operate external cloud environments or infrastructure (e.g., DigitalOcean, personal AWS/GCP accounts, Hetzner, Linode, OVH, or similar services) for work-related purposes unless the service has passed Vendor Security Assessment through Zip and the environment is deployed under Manychat-owned cloud accounts with Security approval. Any external infrastructure must not integrate with Manychat production systems or process Internal or Confidential data without explicit written approval from the Security team.

## **2.10 Usage of personal devices for work-related purposes (BYOD)**

1. Your corporate PC or laptop must be the main and primary device for your work-related activities. Development work related activities must only be carried out on corporate computers.
2. You are allowed to use your personal devices (mobile phone, laptop, or PC) under the following conditions:
    1. There are adequate reasons you can’t access your corporate device or some urgent situation.
    2. The business system (SaaS), which you're planning to access, requires MFA (eg. Slack, Notion, GitHub, Google Workspace).
    3. Mandatory logon personal device protection enabled (PIN, FaceID, etc.).
    4. You have anti-virus software with up-to-date signatures installed.
    5. Your OS has the latest available security patches installed.
3. Remember that your personal device does not contain security software provided by Manychat.
4. Installation of corporate VPN certificates to your personal PC or laptop is an exception and should be approved by the Security Team.
5. It is prohibited to store work-related data on your personal devices. Such action may be considered as an NDA violation.
6. HelpDesk has the right to reject your service request in case it requires them to perform any action on your personal device.
7. In case of a security incident, if your personal device is impacted, Manychat has a right to involve state authorities for incident investigation.
8. You may use official mobile applications downloaded from official mobile stores. For this reason, your personal phone must have a lock-screen password set up and the file system must be encrypted.
9. It is prohibited to use jailbroken or rooted mobile devices for work.
10. The loss or theft of your personal device storing Manychat data or data of Manychat customers, or having corporate system active sessions must be reported to Security team ([security@manychat.com](mailto:security@manychat.com) or [#security](https://manychat.slack.com/archives/C02QYCPRF3J) Slack channel) as soon as possible.

## **2.11 Monitoring and Review**

IT and Security teams may log and monitor any of your actions and activities in business systems for security reasons.

## **2.12 AI Systems and Generative Tools**

Only company-approved AI systems may be used for work-related purposes.

The use of external AI models or generative tools (including ChatGPT personal accounts, Claude, Gemini, Midjourney, or any other public AI service) is prohibited unless explicitly approved and included in Manychat’s business systems inventory.

1. Manychat’s corporate ChatGPT environment is the only permitted AI system for processing Internal information.
    
    Work-related queries must be submitted exclusively through the corporate ChatGPT workspace, which ensures enterprise-grade privacy, data isolation, and prohibits model training on submitted content.
    
2. Confidential information must not be entered into any AI system unless the system is explicitly approved for handling Confidential data.
    
    At present, Confidential data may only be processed in corporate ChatGPT if this usage is approved by the Security team based on the data category and business purpose.
    
3. It is strictly prohibited to input any customer data, personal data, authentication secrets, tokens, credentials, financial information, or production-related details into external AI tools.
    
    Such actions may lead to unauthorized data disclosure or breach of contractual obligations with customers and partners.
    
4. AI-generated outputs must be reviewed for accuracy, compliance, and appropriateness before use.
    
    Employees remain fully responsible for the correctness and security of any content produced using AI.
    
5. Automated use of AI systems (e.g., automated uploads, data pipelines, or integrations) requires prior approval from the Security team.
6. Employees are prohibited from connecting external AI plugins, browser extensions, or unofficial integrations to corporate systems unless explicitly approved.
7. Any suspected data exposure or malfunction involving AI systems must be reported immediately to the Security team (security@manychat.com or #security Slack channel).

## **2.13 Data handling and sharing**

1. All Manychat information, data, and assets must be classified with its sensitivity level described below in accordance with [**Data Classification Policy**](https://www.notion.so/Data-Classification-Policy-2bfb12e9aa1a809aa48bd02294c10582?pvs=21):
    - **‘Public’**
    - **‘Internal’**
    - **‘Confidential’.**
2. All verbal data and recorded data distributed within Manychat offices and using Manychat assets is classified as **‘Internal’** by default. All data classified as **‘Internal’** or above must be handled and processed on a need-to-know basis.
3. Data is approved for public distribution only by authorized personnel (executive team, marketing, HR branding, communication), and might be classified as **‘Public’** only after approval. There are no special handling requirements associated with information with a classification level of **‘Public’**.
4. There is a category of data that requires additional protection (**‘Confidential’** data). It includes customer data, product source code, information related to the production infrastructure (including Platform architecture, IP ranges, hostnames, and authentication secrets), sensitive data related to the Manychat employees.

Here is a table which might help you make a right decision on how to handle the data:

| **What do you want to do with the data/documents?** | **Classification** | **Handling Requirements** |
| --- | --- | --- |
| I want to store or process electronic documents or data in the office (i.e., while working on corporate devices within Manychat’s physical office premises). | Internal | The documents must be processed or stored on Manychat corporate devices or business systems.
Encryption on a file-level layer must be applied to storage. |
| I want to store or process electronic documents or data in the office (i.e., while working on corporate devices within Manychat’s physical office premises). | Confidential | As Internal, however, payment and customer data including personal customer data must be stored only in the production environment. |
| I want to store electronic documents or data in the corporate cloud infrastructure (Manychat business systems, corporate Google Drive) | Internal | Only company-approved solutions must be used. By default, the corporate Google Drive  and  approved systems from [business systems inventory](https://www.notion.so/Systems-access-checklist-cf4b67638ca54ac8987de1967c0d4586?pvs=21).
Access to documents must be provided on the need-to-know principle. The sharing options (eg. link-sharing, user rights, guest rights, etc.) must be carefully verified before providing access especially to external users. Avoid link-sharing in corporate Google Drive (only specified persons should have access to a file). |
| I want to store electronic documents or data in the corporate cloud infrastructure (Manychat business systems, corporate Google Drive) | Confidential | As Internal. For example, if you want to store personal customer data, Google Drive should be used and the file access should be limited to an approved user access list.
Link sharing is prohibited. |
| I want to store electronic documents or data in the non-corporate cloud infrastructure | Internal | Not allowed. Non-corporate cloud storage and personal email services must not be used for Internal or Confidential information, as they are not approved company systems and are treated as insecure locations for company data. |
| I want to store electronic documents or data in the non-corporate cloud infrastructure | Confidential | Not Allowed. Public hostings and mail services classify all uploaded content as publically available, which is not acceptable |
| I want to send electronic documents or data to my private email or personal device/laptop.
*Use of personal devices is allowed only under the BYOD rules in section 2.10 and never for storing or transferring Internal or Confidential data.* | Internal | Not Allowed |
| I want to send electronic documents or data to my private email or personal device/laptop. | Confidential | Not Allowed |
| I want to carry electronic documents or data out of the office on my corporate laptop | Internal | Allowed, as long as your laptop is:
• encrypted;
• strong password and screen policies are applied;
• Mobile device management (JAMF) and anti-virus solutions are used. |
| I want to carry electronic documents or data out of the office on my corporate laptop | Confidential | As Internal. |
| I want to carry electronic documents or data out of the office on removable media | Internal | Allowed. Removable media must be encrypted. |
| I want to carry electronic documents or data out of the office on removable media | Confidential | Allowed if and only if and as long as you have a business need to carry outside of the office with appropriate approval of your line manager.
If lost, the security incident must be raised.
Removable media  must be encrypted. |
| I want to send electronic documents or data internally (eg. to other Manychat team members) | Internal | Allowed via company-approved solutions from [business systems inventory](https://www.notion.so/Systems-access-checklist-cf4b67638ca54ac8987de1967c0d4586?pvs=21). |
| I want to send electronic documents or data internally (eg. to other Manychat team members) | Confidential | As Internal. Only share with internal parties who have a need to know in order to perform their job role. |
| I want to share or send electronic documents or data to external parties including Manychat customer | Internal | The documents must be shared or sent to an external party where there is an approved business need or other justification, and under NDA only or ToS confidentiality statements.
Also, you must ensure the external party is aware that the information must only be used for the declared purpose and forwarded only with the approval of the originator or document owner. |
| I want to share or send electronic documents or data to external parties including Manychat customer | Confidential | The documents must be shared or sent to an external party on a need-to-know basis where there is an approved business, contractual or legislative need and with the approval of the originator or document owner.
Also, you must ensure the external party knows the document classification level and is aware of the protection requirements.
If the content is sent it must be encrypted:
• set a strong, complex encryption password;
• communicate password verbally after confirming receipt of encrypted files or using SMS;
• Don’t reuse previous passwords.
OR
Use confidential mode for emails sent via Google Gmail interface. Confidential mode in Gmail, you can protect sensitive information from unauthorized access. Set an expiration date for messages, revoke access to messages and attachments at any time, and disable recipients' access to forward, copy, print, and download material.
OR
Send as a link to the document stored in approved corporate cloud storage (Google Drive) that requires authentication before the access and keeps access logs to the shared item. |
| I want to store, copy, print, or work in hardcopy information in the office | Internal | The information must be protected against accidental disclosure (e.g. left unattended in the printing area) and hidden from your desk once you have completed work. |
| I want to store, copy, print, or work in hardcopy information in the office | Confidential | The information must be protected against accidental disclosure and cleared away when not in use.
The information must be cleared away to complete the work and stored in a place that is restricted to authorized personnel only (i.e. locker, locked drawer, or restricted room).
All uncontrolled paper copies must be destroyed. |

# **3. Roles and Responsibilities**

The CEO has the overall responsibility for Information Security at the Company, including information security regarding personnel and IT security.

Specific roles and responsibilities:

| **Role** | **Role description** |
| --- | --- |
| **All employees** | Employees are responsible to comply with the Standard and report the violations to the Security team. |
| **Managers** | Line managers are responsible to ensure the awareness of this Standard across their teams. |
| **HelpDesk team** | HelpDesk team is responsible for maintenance of mandatory technical measures and settings for business systems, user equipment, and timely advisory on approved used mechanisms described within this Standard. |
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
| 0.1 | 10.12.2021 | **Author**: Mikhail Kurzin, Head of Security | Draft  version |
| 1.0 | 03.04.2022 | **Author**: Mikhail Kurzin, Head of Security
**Contributors**:
• Antony Gorin, Head of Infa
• Dmitry Kushnikov, Head of Technology
• Anastasia Shchogoleva, Head of Operations
• Nikolay Nestyurkin Workspace admin
• Irina Solodkaya, Internal HR lead. | Initial version |
| 2.0 | 12.12.2022 | **Author**: Mikhail Kurzin, Head of Security
**Approvers**:
• Sunny Manivannan, CEO Manychat Inc.
• Dmitry Kushnikov, Head of technology | 1. Updated branding.
2. Updated clause 4 on cyber awareness in section 2.1. |
| 2.1 | 16.07.2024 | **Author**: Mikhail Kurzin, Head of Security | Document review. No changes were made. |
| 3.0 | 09.06.2025 | **Author**: Mikhail Kurzin, Head of Security | 1. Switch to ISO/IEC 27001:2022
2. Document review |
| 4.0 | 15.12.2025 | **Author:** Sergey Muslaev, GRC Lead | Updating document in accordance with ISO/IEC 42001:2023 |