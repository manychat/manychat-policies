# Artificial Intelligence Policy

Owner: Sergey Muslaev
Verification: Verified
Area: AI
Last edited time: January 25, 2026
Approvers: Dmitry Kushnikov
Document ID: POL-AI-01
Document Type: Policy
Document application: All Contractors, All Employees
Effective date: February 19, 2026
Reviewers: Mikhail Kurzin, Thu Nguyen, Ivan Ilin, Xavier Gumara Rigol
Status: Approved
Tag: ISO42001
Version: 1

# Table of Contents

---

# 1. Purpose

This Artificial Intelligence (AI) Policy defines Manychat’s management direction and commitments for the **responsible design, development, provision, and use of AI systems** within the scope of the Artificial Intelligence Management System (AIMS).

This policy complements the **Information Security Management System (ISMS) Policy** and establishes AI‑specific governance to address risks and impacts arising from AI systems, beyond traditional information security risks.

# 2. Scope of applicability

This policy applies to:

- all AI systems within the scope of Manychat’s AIMS;
- all employees, contractors, and third parties involved in AI‑related activities on behalf of Manychat;
- AI lifecycle activities including design, development, integration, deployment, operation, monitoring, change management, and decommissioning.

The detailed boundaries, roles, and exclusions are defined in the **AIMS Context and Scope document**.

# 3. Alignment with organizational context, ISMS, and strategy

This policy is established in consideration of:

- Manychat’s organizational context and business objectives;
- internal and external issues relevant to the development and use of AI;
- the needs and expectations of relevant interested parties;
- the organization’s risk appetite and existing governance structures.

The application of this policy and associated controls is **proportionate to the level of risk posed by the AI systems** within scope, taking into account the organization’s risk appetite and the **evolving AI risk environment**, including technological, regulatory, and misuse-related risks.

AI governance under this policy is aligned with and builds upon the controls, processes, and culture established under the **ISMS**, including risk management, supplier management, incident management, access control, and monitoring activities.

# 4. Principles for responsible AI

In alignment with its information security principles, Manychat commits to the following principles for AI systems:

- **Lawfulness and compliance:** AI systems are designed and used in compliance with applicable legal, regulatory, and contractual requirements.
- **Risk‑based approach:** AI‑related risks and impacts are identified, assessed, treated, and monitored throughout the AI system lifecycle.
- **Human oversight and accountability:** Appropriate human oversight mechanisms are maintained, with clear accountability for AI system outcomes.
- **Transparency and information:** Relevant information about AI systems is made available to users and other interested parties to support correct use and understanding.
- **Data governance and quality:** Data used for AI systems is governed to address quality, provenance, appropriateness, and limitations, complementing data protection measures under the ISMS.
- **Security by design:** AI systems are developed and operated in alignment with Manychat’s information security practices, including secure development, access control, and monitoring.
- **Continual improvement:** AI governance and the AIMS are continually improved based on monitoring, audits, incidents, and management review.

Manychat defines and applies specific processes for the responsible design and development of AI-enabled systems. These processes ensure that considerations related to intended use, reasonably foreseeable misuse, AI objectives, and potential risks and impacts are taken into account during the design and development of AI-enabled features, and that appropriate safeguards and controls are integrated prior to deployment and material changes.

# **5. AI Governance Objectives**

The organization establishes AI governance objectives aligned with its strategic goals, stakeholder expectations, and applicable legal and regulatory requirements.

These objectives include:

- ensuring compliance with applicable AI-related legal and regulatory requirements;
- promoting transparency and explainability of AI-enabled features;
- preventing bias and promoting fairness in AI outcomes;
- managing AI-related risks and impacts throughout the AI lifecycle;
- promoting competence and awareness in responsible AI use.

The achievement of these objectives is supported through the organization’s governance processes and performance management mechanisms, including OKRs, and is reviewed as part of management review activities.

# 6. Governance, roles, responsibilities and resources

Top management is responsible for:

- approving and supporting this AI Policy;
- ensuring integration of AIMS requirements into organizational processes;
- providing adequate resources for effective AI governance;
- reviewing AIMS performance and effectiveness.

## **6.1 Resources for AI system lifecycle and AI-related activities**

Manychat identifies and maintains the resources necessary to support AI-related activities across the AI system lifecycle and other activities relevant to the Artificial Intelligence Management System (AIMS).

Resources are identified and documented in a manner proportionate to the organization’s role as an integrator and operator of AI-enabled systems and may include, as applicable:

- human resources with appropriate competence and responsibilities for AI governance, risk and impact management, development, operation, and oversight;
- technical resources, including platforms, tools, and third-party AI services required to design, integrate, deploy, operate, and monitor AI systems;
- data resources, including AI-relevant data used across the AI system lifecycle, such as user input data, contextual data used for retrieval-augmented generation (RAG), prompt configurations, AI outputs, usage metadata, and configuration data, as documented in supporting AIMS records;
- information and governance resources, including documented procedures, registers, records, and monitoring information supporting AI lifecycle management and oversight.

The identification and documentation of AI-related resources are maintained through supporting AIMS documentation and are reviewed as part of ongoing AI governance and management review activities.

AI‑related roles and responsibilities, including accountability for risk management, impact assessment, development, operation, and incident handling, are defined and maintained through supporting governance, standards, and procedures, consistent with existing ISMS role assignments.

# 7. AI risk and impact management

Manychat commits to:

- identifying and assessing AI‑related risks and impacts to individuals, groups, and society;
- performing AI risk assessments and AI system impact assessments where required;
- implementing appropriate risk treatment measures, including reference to Annex A controls of ISO/IEC 42001;
- ensuring residual risks are accepted by appropriate authority;
- reviewing risks and impacts following significant changes to AI systems or context.

AI risk and impact management is aligned with the organization’s established risk management practices under the ISMS, while addressing AI‑specific considerations.

# 8. Lifecycle management of AI systems

AI systems within the AIMS scope are managed throughout their lifecycle through documented processes that address:

- requirements definition and specification;
- responsible design and development;
- verification and validation;
- controlled deployment;
- operational monitoring and maintenance;
- change management and decommissioning.

Manychat determines and documents the AI system lifecycle phases at which event logging is enabled. Event logging is enabled at a minimum during the operation of AI-enabled systems to support monitoring, incident detection, investigation, and accountability. Logging may also be enabled during other lifecycle phases, such as testing, deployment, and change activities, where necessary to support verification, validation, or troubleshooting, taking into account technical feasibility and proportionality.

Objectives guiding the responsible development and use of AI-enabled systems are defined and maintained as part of Manychat’s AI Risk & Impact Assessment process. These objectives are used to inform the identification of AI-related risks and impacts, the selection of mitigation measures, and decisions taken throughout the AI system lifecycle.

Manychat defines the intended use of AI-enabled features and provides accompanying documentation and information to users to support correct and responsible use. Reasonable safeguards are implemented within AI-enabled systems to discourage or limit use outside the intended purpose. Where deviations from intended use, misuse, or adverse impacts are identified or reported, they are addressed through established concern reporting and incident management processes.

Where applicable, lifecycle controls leverage existing secure development, change management, and operational controls defined under the ISMS.

# 9. Use of third-party AI components and services

Manychat’s AI systems may rely on third-party AI components, services, or infrastructure as part of their design, development, and operation.

Manychat commits to:

- identifying and assessing AI-related risks and impacts arising from the use of third-party AI components and services;
- ensuring that roles, responsibilities, and accountabilities across the AI system lifecycle are clearly allocated between Manychat and relevant third parties;
- managing third-party AI risks through appropriate contractual, technical, and organizational measures;
- monitoring the continued suitability of third-party AI components and services in line with the organization’s risk appetite and obligations.

Third-party AI governance is aligned with the organization’s vendor management, risk management, and incident management processes under the ISMS and AIMS.

# 10. Communication, awareness, and reporting

## 10.1 Communication and awareness

Manychat ensures that:

- this AI Policy is communicated to relevant personnel;
- personnel involved in AI‑related activities are aware of their responsibilities;
- mechanisms exist to report AI‑related concerns, incidents, or adverse impacts;
- external communication regarding AI systems is controlled and aligned with organizational obligations.

## 10.2 Reporting of AI-related concerns

Manychat maintains a documented process that enables employees and other relevant stakeholders to report concerns related to the organization’s role with respect to AI systems throughout their lifecycle.

Reportable concerns may include ethical, legal, safety, security, misuse, or compliance-related issues, including potential risks or adverse impacts arising during the design, development, deployment, operation, modification, or decommissioning of AI systems.

AI-related concerns may be reported through established internal reporting and escalation channels. Reports are reviewed and addressed in accordance with the organization’s AI risk and impact management, incident management, and governance processes.

The organization encourages the reporting of AI-related concerns and ensures that such reports can be raised without fear of retaliation.

# 11. Monitoring, review, and continual improvement

The effectiveness of this policy and the AIMS is monitored through:

- performance monitoring and metrics;
- internal audits;
- incident and issue management;
- management review.

This policy is reviewed at planned intervals and updated as necessary to ensure its continuing suitability, adequacy, and effectiveness.

# 12. Policy enforcement

Compliance with this AI Policy is mandatory. Violations or nonconformities are addressed through corrective actions in accordance with AIMS and ISMS improvement processes.

# 13. Deviations and exceptions

Deviations or exceptions from this AI Policy may be permitted only where justified by business need or technical constraints, and where associated risks and impacts have been assessed.

All deviations and exceptions shall:

- be documented;
- be subject to risk and impact assessment;
- be approved by appropriate authority;
- be reviewed periodically to determine continued necessity.

Deviations and exceptions are managed in accordance with the organization’s AIMS and ISMS risk management and improvement processes.

---

# **Document History**

| **Version** | **Date of**
**Change** | **Author and Contributors** | **Changes to the previous version** |
| --- | --- | --- | --- |
| 0.1 | 25.01.2026 | **Author**: Sergey Muslaev, GRC Lead | Draft  version |
| 1.0 | 19.02.2026 | **Author**:  Sergey Muslaev, GRC Lead

**Contributors**: Mikhail Kurzin, Head of Security
Thu Nguyen, AI Product Director
Ivan Ilin, AI Research Lead
Xavier Gumara Rigol, Head of Data
 | Initial version |