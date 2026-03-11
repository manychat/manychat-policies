# AI System Design and Development Procedure

Owner: Sergey Muslaev
Area: AI
Last edited time: January 23, 2026
Approvers: Dmitry Kushnikov
Document ID: PR-AI-02
Document Type: Procedure
Document application: All Contractors, All Employees
Reviewers: Mikhail Kurzin, Thu Nguyen, Ivan Ilin, Xavier Gumara Rigol
Status: In review
Tag: ISO42001
Version: 1

# Table of contents

---

# 1. Purpose and Scope

## 1.1 Purpose

This procedure defines the requirements governing the design, development, integration, testing, deployment, operation, and modification of AI-enabled systems within the Manychat platform. The purpose of this procedure is to ensure that AI systems are developed and operated in a responsible, controlled, and auditable manner, consistent with Manychat’s Artificial Intelligence Management System (AIMS), organizational objectives, and applicable standards.

## 1.2 Scope and Applicability

This procedure applies to all AI-enabled features developed, integrated, or operated by Manychat.

Manychat operates as an AI system integrator and deployer and relies on third-party AI service providers for underlying AI models. This procedure applies to the design, integration, deployment, operation, and modification of AI-enabled features within the Manychat platform.

If and when Manychat performs or commissions model training or fine-tuning (including using customer-managed or Manychat-managed datasets), the requirements of this procedure shall apply to the relevant datasets and lifecycle activities.

# 2. AI System Lifecycle and Intended Use

## 2.1 AI System Lifecycle

Manychat shall apply a defined AI system lifecycle model informed by ISO/IEC 22989 and adapted to its organizational role and products. The lifecycle encompasses concept definition, requirements and design, risk and impact assessment, development and integration, verification and validation, release and deployment, operation and monitoring, and change, improvement, or decommissioning.

Each lifecycle stage shall have defined inputs, controls, responsibilities, and documented outputs, appropriate to the nature and criticality of the AI system.

## 2.2 Concept Definition and Intended Use

For each AI-enabled system or material enhancement, Manychat shall document the intended purpose, expected benefits, and context of use of the AI system. Reasonably foreseeable misuse and limitations shall be identified and documented. Alignment with Manychat’s responsible AI objectives shall be confirmed prior to proceeding with design and development activities.

No AI system shall be designed, developed, or integrated without a documented intended use.

# 3. Requirements, Design, and Human Oversight

## 3.1 System Requirements and Design

Manychat shall document functional and non-functional requirements for AI systems, including performance expectations, usability considerations, controllability, data usage boundaries, security and privacy constraints, and operational limitations. System design shall take into account the nature of AI-assisted decision-making and shall avoid unjustified reliance on automated outputs.

## 3.2 Human Oversight and Controllability

AI systems shall be designed to support appropriate human oversight. Where AI systems may affect natural persons, design decisions shall explicitly address human review, escalation, override, or intervention mechanisms. The level and form of human oversight shall be proportionate to the potential risks and impacts associated with the AI system.

AI-enabled systems shall be designed to be usable and controllable within their intended context, allowing users to understand, influence, or limit AI behavior in accordance with documented functionality.

# 4. Risk, Impact, and Data Considerations

## 4.1 AI Risk and Impact Assessment Integration

An AI Risk and Impact Assessment shall be performed prior to the initial release of an AI-enabled system and shall be updated when material changes are introduced, when significant incidents occur, or when the context of use changes materially.

The results of the AI Risk and Impact Assessment shall be taken into account during system design, implementation, testing, and release decisions. Identified risks and impacts shall inform the selection of safeguards, monitoring requirements, and approval conditions.

## 4.2 Training Data Expectations and Rules

Responsibilities for training data governance, quality, labelling, representativeness, and evaluation are allocated to the relevant party as defined by applicable service, vendor, and contractual arrangements.

Operational and contextual data used to support AI system functionality shall be managed in accordance with Manychat’s established privacy, security, and data governance framework, as applicable.

If and when model training or fine-tuning activities are performed or commissioned by Manychat, this procedure shall apply to all datasets used throughout the AI system lifecycle, including training, validation, test, and production datasets, and to the associated governance, documentation, and evaluation requirements.

# 5. Development, Testing, Release, and Change Control

## 5.1 Development and Integration

Development of AI systems at Manychat primarily consists of the integration and orchestration of third-party AI services, where applicable, configuration of prompts and workflows, and implementation of safeguards and controls. Development activities shall follow established secure development practices and internal engineering standards and shall remain within the documented intended use.

## 5.2 Verification and Validation

AI systems shall be verified and validated prior to release to ensure conformity with documented requirements, intended use, and risk mitigation measures. Verification and validation activities shall include testing under expected and reasonably foreseeable conditions, confirmation of safeguard effectiveness, and assessment of fallback and escalation mechanisms.

## 5.3 Release, Approval, and Deployment

AI-enabled systems shall not be released into production without completion of required verification and validation activities, completion or update of the AI Risk and Impact Assessment where applicable, and approval by designated Product and Engineering authorities. Where required by the risk profile, Compliance or Security approval shall also be obtained. Deployment shall follow the Change Management Standard.

## 5.4 Change Control and Continuous Improvement

Changes to AI-enabled systems shall be subject to change impact analysis and shall consider potential effects on intended use, risks, impacts, and safeguards. Material changes shall trigger an update of the AI Risk and Impact Assessment prior to implementation. AI systems shall be continuously monitored, and feedback from users, incidents, or monitoring activities shall be used to support improvement and corrective actions.

# 6. Governance, Documentation, and Review

## 6.1 Roles, Competence, and Interested Parties

Design, development, and oversight of AI systems shall be performed by personnel with appropriate competence and understanding of AI-related risks and limitations. Manychat shall consider the perspectives of relevant interested parties, including internal teams, customers, and AI service providers, during the design, development, and improvement of AI systems.

## 6.2 Documentation and Record Keeping

Documentation relating to AI system design and development shall be maintained and controlled, including design specifications, risk and impact assessments, testing records, approvals, and change records. Documented information shall be managed in accordance with the organization’s documented information controls.

## 6.3 Review and Maintenance

This procedure shall be reviewed periodically and updated as necessary to reflect changes in AI systems, organizational practices, regulatory expectations, or applicable standards.

# **Document History**

| **Version** | **Date of**
**Change** | **Author and Contributors** | **Changes to the previous version** |
| --- | --- | --- | --- |
| 0.1 | 23.01.2026 | **Author**: Sergey Muslaev, GRC Lead | Draft  version |
| 1.0 |  | **Author**:  Sergey Muslaev, GRC Lead
**Contributors**: Mikhail Kurzin, Head of Security
Thu Nguyen, AI Product Director
Ivan Ilin, AI Research Lead
Xavier Gumara Rigol, Head of Data
 | Initial version |