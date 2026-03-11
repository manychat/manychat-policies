# Physical Security Standard

Owner: Mikhail Kurzin
Area: InfoSec
Approvers: Mike Yan, Dmitry Kushnikov, Antony Gorin
Document ID: STD-IS-05
Document Type: Standard
Document application: All Contractors, All Employees
Effective date: December 14, 2022
Status: Published
Tag: ISO27001
Version: 2

<aside>

**Key points:**

- Access control system;
- Access control perimeter (areas within the access control system);
- Restricted zones (secure areas);
- Requirements for third party access.
</aside>

<aside>

*This Standard describes the physical security requirements for the existing and/or future office workspaces, defines security perimeters inside offices with essential safeguards, and requirements for third-party providers.*

</aside>

---

# Table of contents

---

# 1. General

## **1.1 Purpose**

This Standard describes the physical security requirements for office workspaces, defines security perimeters inside offices with essential safeguards, and requirements for third-party office providers.

This Standard defines

- access control system;
- access control perimeter (areas within the access control system);
- restricted zones (secure areas);
- employee requirements;
- requirements for third party access.

The Standard describes our vision for:

- establishing the rules for granting, control, monitoring, and removal of physical access to office premises;
- identifying sensitive areas inside offices;
- defining and restricting access to offices’ areas.

This document shall be utilized as a guide for launching any new Manychat physical offices.

## **1.2 Scope**

This document contains requirements for Manychat’s physical offices and rented facilities (coworking premises).

The coworking premises where Manychat staff might be located shall follow all possible requirements of this Standard.

Colocation third-party data centers are out of scope of this Standard.

The document is reviewed at least annually, to ensure it meets the requirements of Manychat in-house, partner, customer, and external organizations, and Manychat business objectives.

# 2. Physical Security Standard

Each Manychat office shall have a set of zones split by their access limitations:

- **Public areas**: all zones freely accessible by anyone apart from Manychat employees. Those may include recreation zones outside of the access control perimeter, staircases, delivery and loading areas, business lounge, cafeterias, etc. Coworkings with shared open workspaces are considered a public zone.
- **Work areas**: open spaces with workplaces within the access control perimeter, which may be accessed by Manychat employees. Dedicated areas in coworkings that can be locked with a local access control system may be considered as work areas.
- **Secure work areas**: areas with sensitive premises that require additional safeguards. Coworkings usually don’t have such areas.

All physical security controls must comply with all applicable local regulations and legislation such as, but not limited to, data protection, building codes and fire prevention codes.

Local Health and Safety instructions must take precedence over this standard.

Access to non-public areas must be granted only to Manychat employees, contractors, vendors, or other individuals who have a justified and documented reason for requesting access.

## **2.1 Office Entry controls, Delivery & Loading Areas**

Each Manychat office shall have a controlled list of entry points including, but not limited to:

- Main entrance;
- Reception zone;
- Secondary/service entrances (parking lots, fire stairs, evacuation exits);
- Cargo elevators, etc.

Entrances need to be protected by the appropriate entry controls to ensure only authorized personnel are allowed access:

1. Security perimeters shall be developed to protect areas that contain server and network equipment to prevent unauthorized physical access, damage and interference.
2. Physical access to the internal resources shall be monitored to detect and respond to physical security incidents.
3. Access points such as delivery and loading areas and other points where unauthorized persons could enter the premises should be controlled and isolated from Work areas to avoid unauthorized access. The following controls for access points should apply:
- location inside the main office building;
- extra guarding (eg. turnstiles);
- separation by access control system;
- CCTV monitoring & recording ingress/egress points and delivery/loading areas;
- duty personnel or security guards, if applicable;
- procedures to prevent external and internal access being open at the same time, e.g. turnstiles open in both directions at the same time.

## **2.2 Access Control System**

Access Control System is an electronic security system that uses an identifier such as an access card to authorize personnel to enter certain allowed areas (access control perimeter).

For Manychat access control perimeter all entrances to work and secure work areas  must be bounded by the electronic Access Control System. All areas outside the Manychat access control system are considered non-trusted areas.

For employees and guest visitors, the following controls need to be implemented:

### 2.2.1 Physical entry controls for employees

The following guidelines for employees should be considered:

- Each employee is provided with a registered personal pass;
- All Manychat employees must undergo access card/ badge validation before entering non-public areas;
- Employee pass allows access to authorized locations;
- It is not allowed to give the pass to anyone else. In case if the pass is forgotten, the guest pass with minimum access level may be given till end of current business day.
- In case of loss of the pass, office managers must be immediately notified to block and reissue the pass.

### 2.2.2 Thirdparty physical access

The following guidelines for third-parties (visitors, contractors, suppliers, office maintenance firms, etc.) should be considered:

- The identity of visitors should be authenticated by appropriate means (ID, driver’s license, verification by the landlord etc.);
- All visitors and contractors must be provided with a temporary identification badge for the entire period of their visit to Manychat premices;
- Visitors and contractors must return their temporary identification badge prior to leaving the Manychat premices;
- The purpose of visiting Manychat location shall be identified;
- Dedicated delivery and loading areas shall be established;
- Access of authorized third-parties to work areas and secure work areas must be performed only under supervision of a responsible Manychat employee;
- Employees should challenge and/or report to the Security Team anyone within a Manychat premices who is not displaying a valid identification badge or not supervised by responsible Manychat employee.

### 2.2.3 Alarms and protection from environmental threats

The following guidelines for alarms and environmental threats protection systems should be considered:

- Emergency lighting, alert communication systems should be provided.
- Emergency switches and valves to cut off power, water, gas or other utilities should be located near emergency exits or engineering and utility services rooms.
- Emergency evacuation plans must be located on each floor in a visible location.
- Fire drills and test evacuations must be conducted and reported at least annually.
- Each office should have a nominated emergency coordinator in case of a disaster.

## **2.3 Secure Work Areas**

### 2.3.1 Entry controls to secure work areas

1. List of secure areas in the office must be nominated. Locations to be considered secure areas, shall include:
- server rooms;
- offices with sensitive paper records storage;
- storage rooms;
- commutation nodes;
- facility switchboards.
1. Secure areas must have a second access factor (physical key or a pin code).

### 2.3.2 Additional requirements for server rooms

Server rooms located in each office shall follow minimum requirements:

1. Air conditioning is performed according to equipment manufacturers’ standards.
2. CCTV is installed at the entrance to the server room.
3. Access logs to the server room are reviewed at least every 6 months.
4. Cabling security rules specific for server rooms are followed:
- If a server room contains more than one rack, the rules of hot/cold areas apply.
- Free area around the rack must be at least 60cm.
- Cables must be secured by placing them into the cable shell.
- Cables in the rack must not block the rack doors for closing.
- Power and network cables must be separated.

## **2.4 Protecting against external and environmental threats**

Head of Security is responsible for planning and operations of physical security.

Apart from access control, physical security mechanisms shall cover protection against:

- Environmental controls. Environmental threats could be naturally-occurring (e.g. floods, tornados, lightning, etc);
- Man-made (e.g. water leakage from facilities, civil unrest, etc).

Equipment needs to be protected from power failures and other disruptions caused by failures in supporting utilities:

- dual power supplies from different sub-stations;
- backup power generation facilities;
- regular testing of power provision and personnel.

For telecommunications:

- dual or multiple Internet providers;
- load balancing and redundancy in switching equipment;
- bandwidth capacity monitoring and alerting.

Evacuation plans, fire equipment inspections, and periodic training evacuations shall be established and maintained.

## **2.5 Equipment Siting and Protection**

### 2.5.1 Cabling security

The following guidelines for cabling security should be considered:

1. Power and telecommunications lines into information processing facilities should be a subject to adequate protection (in walls, ceilings, or covered by shells to prevent accidental damage).
2. Power cables should be segregated from communications cables to prevent interference.
3. Backup power sources must be tested regularly.

### 2.5.2 Facility maintenance

Specialist advice from third party subject matter experts should be obtained on how to avoid damage from fire, flood, earthquake, explosion, civil unrest and other forms of natural or man-made disaster.

Office facility services should be equipped and secured:

1. Power and plumbing nodes must be physically secured to prevent unauthorized access to avoid damage from fire, flood, explosion and other forms of natural or man-made disaster.
2. Facilities must be maintained by third party companies with appropriate licenses and expertise.

## **2.6 Equipment Maintenance by third-party suppliers**

Equipment hosted in the office building should be correctly maintained to ensure its availability and integrity. Maintenance needs to be carried out on equipment at appropriate frequencies to ensure that it remains effectively functional and to reduce the risk of failure. Logs of this maintenance should include who carried out the maintenance, what was done and who authorized the maintenance.

Third party suppliers’ access during maintenance/repair work on power and telecommunications cabling, sanitary engineering, fire system inspections:

- should be maintained by a licensed supplier with required specialists, usually by landlords;
- should always be accompanied by a responsible Manychat personnel.

## **2.7 Unattended user equipment in public zones**

Users shall be made aware of their responsibilities for leaving unattended equipment in public zones. The user shall handle equipment in a secure manner and handle unattended equipment upon discovery in accordance with [Office Security Standard](https://docs.google.com/document/d/12m-iQKNZQtRF9aVx6VNqFnRvtm5CqNhZ/edit?usp=share_link&ouid=105608147576229526248&rtpof=true&sd=true).

Unattended equipment can include:

- laptops;
- flash drives or any accessory which can be plugged into a laptop or PC;
- gadgets (including personal phones).

If suspicious equipment is found, it should be handed over to the local helpdesk team from the reception or by the employee who identified such equipment directly.

For any loss of personal equipment outside Manychat access control perimeter, including both corporate laptops and personal cell phones, a security incident shall be submitted to [security@manychat.com](mailto:security@manychat.com).

# 3. Roles and Responsibilities

The CEO has the overall responsibility for Information Security at the Company, including information security regarding personnel and IT security.

Process specific roles and responsibilities:

| **Role** | **Role description** |
| --- | --- |
| **All employees** | Take responsible actions to comply with the standard. |
| **Managers** | Responsible for ensuring their direct reports (whether those direct reports are permanent employees, contractors, sub-contractors, and agency personnel) are familiar with the requirements of this document. |
| **Office managers** | Take responsible actions to follow the Standard requirements on the following:
• Managing IDs for employees and guests
• Establishing the process of guest entry
• Communicating with the landlord on physical security controls on the facility
• Escorting facility maintenance specialist to avoid unattended access to areas with Manychat employees or data
• Assisting Security team on physical security improvement |
| **Security team** | Responsible for monitoring the effectiveness of the physical security in the offices, acting as an independent approver for comprehensive requests from the office managers, providing guidance on improvements. |

# 4. Compliance

The proof of ISMS quality is the receipt and maintenance of the certificate of ISO/IEC 27001:2022 «Information Technology. Security techniques. Information security management systems. Requirements» compliance.

Manychat must comply with multiple state regulatory requirements of countries, Manychat operates in, such as:

- The General Data Protection Regulation (GDPR) (Regulation (EU) 2016/679);
- Personal data protection regulation in the countries or regions of operation (eg. CCPA);
- Canada’s Anti-Spam Law (or “CASL”);
- The CAN-SPAM Act;
- other mandatory state regulatory acts including acts on commercial secrets and intellectual property.

## **4.1 Enforcement**

Implementation and enforcement of this Standard is ultimately the responsibility of all employees at Manychat. Security team may conduct ad-hoc checks to ensure compliance with this document without notice. Any violation shall require immediate corrective action. Violations shall be noted in the Manychat applications and responsible employees shall be dispatched to remediate the issue.

For Manychat employees, breaches of this Standard may result in disciplinary action being taken and will be dealt with under the disciplinary process in accordance with state laws and regulations of the residence country. Any serious breaches or repeated breaches of this Standard may be deemed by Manychat as gross misconduct and may result in disciplinary sanctions, including a remark, reprimand, and dismissal from work.

## **4.2 Exceptions**

Exceptions to this standard must be processed in accordance with the deviation handling rules by the Security team. All exceptions must be maintained taking into account associated risks, exceptions, and recorded approvals. Continuously detected deviations may trigger the changes or improvements of the measures defined in this document.

# Document History

| **Version** | **Date of**
**Change** | **Author and Contributors** | **Changes to the previous version** |
| --- | --- | --- | --- |
| 0.1 | 08.11.2022 | **Author**: Mikhail Kurzin, Head of Security | Draft |
| 1.0 | 14.12.2022 | **Author**: Mikhail Kurzin, Head of Security | Initial version |
| 1.1 | 16.07.2024 | **Author**: Mikhail Kurzin, Head of Security | Document review. No changes were made. |
| 2.0 | 09.06.2025 | **Author**: Mikhail Kurzin, Head of Security | 1. Switch to ISO/IEC 27001:2022
2. Document review |