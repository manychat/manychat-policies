# Cryptography Use Standard

Owner: Mikhail Kurzin
Area: InfoSec, Infra
Last edited time: June 6, 2025
Approvers: Dmitry Kushnikov, Antony Gorin, Artur Evstefeev
Document ID: STD-IS-06
Document Type: Standard
Document application: All Contractors, All Employees
Effective date: November 14, 2022
Status: Published
Tag: ISO27001
Version: 2

<aside>

**Key points:**

- Cryptography handling
- Encryption in transit and at rest
- Secure algorithms
- TLS/SSL certificates
</aside>

<aside>

*This standard sets the key principles and requirements for data encryption in transit and at rest. Encryption is a key security measure to ensure confidentiality of data processed within the Manychat product.*

</aside>

---

# Table of contents

---

# **1. General**

## **1.1 Purpose**

This document describes the use of cryptographic protection methods on all applicable communication channels to maintain maximum levels of confidentiality of data processed within Manychat.

## **1.2 Scope**

This standard applies to all divisions, teams, and services of Manychat and all personnel of Manychat. It also applies to external organizations and their personnel who have been granted access to the Manychat infrastructure and services.

The document is reviewed at least annually to ensure it meets the current business requirements of Manychat, partners, customers, and external organizations.

# **2. Standard**

## **2.1 Standard summary**

Approved ciphers, hashing functions, protocols and methods include:

- Symmetric encryption algorithms: ChaCha20, AES 128 and AES 256,
- Asymmetric encryption algorithms: ECDSA (with minimum 256 Bit key length) and RSA (with minimum 2048 Bit key length),
- Key-agreement methods: Elliptic-curve Diffie–Hellman (ECDH), Diffie-Hellman and MQV,
- Hashing algorithms: SHA-256 and above.

Proprietary or internally developed encryption algorithms must not be used.

Approved protocols for web communications are WSS (WebSockets over TLS 1.2/ 1.3) and HTTPS 2.0 over TLS 1.2/ 1.3.

TLS 1.1/1.0 are used for legacy purposes (support of old OS versions), however there must be a focus on their deprecation.

## **2.2 Data transmission**

### 2.2.1 Network channels

Web gateway is deployed at the edge of the production environment to limit traffic to authorized communication channels and protocols. Application and database servers sit behind this gateway to prevent direct access from public networks.

Administration of the production infrastructure is allowed only via secure shell (SSH) from  virtual private network (VPN) servers with a unique one-time token, which is used as an additional authentication factor (MFA) for the production environment.

### 2.2.2 Web communication channels

The Manychat platform supports TLS 1.1 and above, hardened by Grade B certificate.

All external communication channels are required to set up secure connections using WSS (WebSockets over TLS 1.2/ 1.3) or HTTPS 2.0 over TLS 1.2/ 1.3.

## **2.3 Encryption at rest**

### 2.3.1 Data centers

AWS EU (Frankfurt) hosting is used as a primary hosting of Manychat landing page, web, mobile API, and other  applications.

The hard drives and snapshots of AWS EU (Frankfurt) production databases and servers must be encrypted using AES 265-bit encryption protocol. File system and backup encryption keys must be stored and managed in the AWS Key Management Service (AWS KMS).

### 2.3.2 Workstations

All users' workstations must be pre-set to have encryption enabled.

FileVault is used for Mac OS based devices, Bitlocker is used for Windows-based devices.

## **2.4 Product key management process description**

Formal processes must be implemented (and tested) to cover all aspects of key management, including:

| **Life cycle stage** | **Description** |
| --- | --- |
| Generating and storing new keys/certificates. | This includes:
• generation of certificates in CA environments,
• secure storage procedures for private keys in AWS KMS. |
| Distributing keys/certificates to the required parties. | This includes manual or automated distribution of keys/certificates to environments.
Change management: Procedure shall be established to control changes of keys/certificates and notification of involved parties. |
| Deploying keys/certificates to application servers. |  |
| Rotating and decommissioning old keys/certificates | Rotation periods (cryptoperiods) shall be established for keys. Key destruction should be secure.
External CA should have mechanisms to monitor certificate lifetime. |
| Monitoring | Authenticity of certificates and availability of services, lifetime and expiration, successful and unsuccessful delivery and rotation, shall be monitored. |

### 2.4.1 CA requirements

Usage of self-signed certificates is allowed only for internal server communications as an exception after approval of the Security Team.

For production environment certificates, a Certification Authority (CA) that is reliable and serious about its certificate business and security must be chosen.

Selected CA should provide support for both Certificate Revocation List (CRL) and Online Certificate Status Protocol (OCSP) revocation methods.

Selected CA should provide support for Automated Certificate Management Environment (ACME) and Simple Certificate Enrollment Protocol (SCEP).

**Preferable CAs:**

- Letsencrypt - may be used for internal network resources (must not be used for customer-facing applications).
- Sectigo - all customer-facing applications and components.

### 2.4.2. Delivery Mechanisms

Access to private keys must be restricted.

Delivery and renewals of private keys must be executed through an established change management procedure with mandatory notification of interested parties.

Delivery of certificates can be performed manually or automatically as follows:

| **Delivery type** | **Description** |
| --- | --- |
| Automated | Certificate delivery over ACME,SCEP, API or CA agents. Automated delivery shall include verification of successful delivery and control of outdated certificates. |
| Manual | Manual delivery by server administrator. Additional controls shall be established to monitor successful delivery and control outdated certificates. |

## **2.5 Requirements for SSL certificates**

### 2.5.1 Lifetime and rotation

Estimated maximum certificate lifetime:

| **Type** | **Definition** | **Max Lifetime** |
| --- | --- | --- |
| Infrastructure certificates | Internally used certificates on non public-facing resources | 2 years |
| Wildcard certificates | A public certificate, which can be used with multiple sub-domains of a domain | 2 years |
| EV-certificates | Extended Validation Certificate (EV) is a certificate that proves the legal entity of the owner and is signed by a certificate authority key that can issue EV certificates | 1 year |
| Employee personal certificates | Personal certificates issued and stored on and employee’s laptop; generally used to connect to corporate networks and business systems | 2 years |

Encryption keys should be changed (or rotated) in the following cases:

- Before lifetime expires;
- If the previous key is known (or suspected) to be compromised;
- Replacing the certificates after someone who had access to the private key leaving the organization.

### 2.5.2 Strong Hashing Algorithms

SHA-256 and above must be used.

### 2.5.3 Complexity

RSA minimum key length must be 2048 Bit or higher.

ECDSA minimum key length must be 256 Bit or higher.

The following secure mechanisms should be used:

- TLS v1.2 and v1.3 are both without known security issues,
- DNS Certification Authority Authorization (CAA) should be enabled for web-based certificates if possible,
- HSTS should be enabled for web-based certificates if possible.

Secure cipher suites with authenticated encryption should be used to simultaneously assure the confidentiality and authenticity of data.

Prefered cipher suites:

- TLS_CHACHA20_POLY1305_SHA256
- TLS_AES_128_GCM_SHA256
- TLS_AES_256_GCM_SHA384
- TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256
- TLS_ECDHE_ECDSA_WITH_ARIA_128_GCM_SHA256
- TLS_ECDHE_ECDSA_WITH_AES_128_CCM
- TLS_ECDHE_ECDSA_WITH_AES_128_CCM_8
- TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384
- TLS_ECDHE_ECDSA_WITH_ARIA_256_GCM_SHA384
- TLS_ECDHE_ECDSA_WITH_AES_256_CCM
- TLS_ECDHE_ECDSA_WITH_AES_256_CCM_8
- TLS_ECDHE_ECDSA_WITH_CHACHA20_POLY1305_SHA256.

### 2.5.4 Monitoring

Authenticity of certificates and availability of services should be monitored. Certificates' lifetime and expiration dates should be controlled and monitored. Actions of delivery and rotation of certificates with integrity should be monitored. Services with pinned certificates (if used) should be separately monitored if possible.

# **3. Roles and Responsibilities**

The CEO has the overall responsibility for Information Security at the Company, including information security regarding personnel and IT security.

Process specific roles and responsibilities:

| **Role** | **Role description** |
| --- | --- |
| **All employees** | Employees are responsible to comply with the Standard and report the violations to the Security team. |
| **Managers** | Line managers are responsible to ensure the awareness of this Standard across their teams. |
| **Security team** | Security team is responsible for monitoring overall awareness with this Standard, monitoring, and investigating the violations, and deviations handling. |
| **Infrastructure team** | Infrastructure team is responsible for management of production keys and certificates and their timely rotation in Manychat application. |
| **Development team** | Development team is responsible for managing product secrets and keys. |

# **4. Compliance**

The proof of ISMS quality is the receipt and maintenance of the certificate of ISO/IEC 27001:2022 «Information Technology. Security techniques. Information security management systems. Requirements» compliance.

Manychat must comply with multiple state regulatory requirements of countries, Manychat operates in, such as:

- The General Data Protection Regulation (GDPR) (Regulation (EU) 2016/679);
- Personal data protection regulation in the countries or regions of operation (eg. CCPA and Law of Armenia on protection of personal data ( ЗR-49-N));
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
| 0.1 | 08.11.2022 | **Author**: Mikhail Kurzin, Head of Security | Draft |
| 1.0 | 14.12.2022 | **Author**: Mikhail Kurzin, Head of Security
**Contributors**:
• Antony Gorin, Head of Infra | Initial version |
| 1.1 | 16.07.2024 | **Author**: Mikhail Kurzin, Head of Security | Document review. No changes were made. |
| 2.0 | 06.06.2025 | **Author**: Mikhail Kurzin, Head of Security | 1. Switch to ISO/IEC 27001:2022
2. Document review |