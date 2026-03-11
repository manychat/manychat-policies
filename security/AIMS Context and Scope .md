# AIMS Context and Scope

Owner: Sergey Muslaev
Verification: Verified
Area: AI
Last edited time: January 25, 2026
Approvers: Dmitry Kushnikov
Document ID: STD-AI-02
Document Type: Standard
Document application: All Contractors, All Employees
Effective date: February 19, 2026
Reviewers: Mikhail Kurzin, Thu Nguyen, Ivan Ilin, Xavier Gumara Rigol
Status: Approved
Tag: ISO42001
Version: 1

# Table of contents

# 1. Purpose

This document defines the **context, scope, and boundaries** of the Artificial Intelligence Management System (AIMS) implemented at **Manychat** (the “Company”), in accordance with **ISO/IEC 42001:2023**.

The AIMS scope and boundaries are determined considering:

- the Company’s business model and strategy;
- internal and external issues relevant to the use of AI;
- the requirements and expectations of relevant interested parties;
- dependencies between activities performed by the Company and those performed by third parties.

This document confirms the commitment of Manychat’s leadership to establish, implement, maintain, and continually improve an AIMS that complies with ISO/IEC 42001:2023.

The AIMS is integrated with the Company’s **Information Security Management System (ISMS)** and privacy management processes to ensure consistent risk management, policy alignment, and evidence collection across governance frameworks.

# 2. Organizational context

Manychat is a SaaS chat marketing platform that enables businesses to build and manage automated and AI-assisted conversations with their customers across multiple messaging channels.

The Company processes large volumes of data, including personal data, through integrations with third-party platforms such as Facebook, Instagram, WhatsApp, and other messaging and commerce services. Due to this scale and nature of processing, Manychat places particular importance on privacy, security, and responsible AI governance.

Manychat seeks to provide assurance to customers, partners, regulators, and other stakeholders that AI systems are governed and operated in accordance with applicable legal, ethical, and regulatory requirements, ensuring transparency, fairness, human oversight, and responsible use.

The Company believes that establishing and continually improving an AIMS enables effective governance of AI systems and helps prevent ethical, regulatory, reputational, and operational risks arising from AI-enabled functionality.

## 2.1 External issues

External issues relevant to the AIMS include:

- **Economic factors:** budgetary constraints affecting AI and information security governance;
- **Competitive environment:** high expectations regarding confidentiality, integrity, availability, reliability, and trustworthiness of AI-enabled services;
- **Regulatory and compliance landscape:** global data protection laws (e.g. GDPR, CCPA), AI-specific frameworks and regulations (e.g. EU AI Act, NIST AI RMF);
- **Fraud and misuse risks:** increasing abuse of digital communication channels and AI-generated content;
- **Ethical and societal expectations:** demand for fairness, transparency, non-discrimination, and accountability in AI systems;
- **Reputational risk:** potential loss of trust, regulatory sanctions, or customer harm arising from AI failures or misuse;
- **Environmental considerations:** awareness of sustainability impacts related to AI computation and data processing.

## 2.2 Internal issues

Internal issues relevant to the AIMS include:

- large-scale data processing and storage;
- reliance on cloud infrastructure and third-party service providers, including AI APIs;
- distributed and international teams operating across multiple jurisdictions;
- AI system design and development risks, including incomplete testing or flawed assumptions;
- data quality, provenance, and bias risks;
- model lifecycle management challenges such as model drift;
- dependency on third-party AI services for core functionality;
- defined human oversight responsibilities for AI system outputs;
- evolving maturity of AI governance structures, policies, and procedures.

---

# 3. Interested parties and their requirements

Manychat recognizes that effective AI governance depends on understanding the needs and expectations of relevant interested parties. These are considered when defining the AIMS scope and during ongoing AIMS review.

Key interested parties include:

## 3.1 External interested parties

- **Regulators and legislators:** compliance with applicable data protection, AI, consumer protection, and anti-spam laws and regulations.
- **Customers, end users, and society:** reliable and secure AI-enabled services; transparency and explainability of AI features; protection from bias, misinformation, or harm; accountability for AI outcomes.
- **Platform partners (e.g., Meta, TikTok):** compliance with platform terms and policies, including restrictions on data access, use, retention, and sharing; adherence to required security controls, review processes, and ongoing compliance obligations to maintain integrations and platform access.
- **Service providers (e.g., cloud and infrastructure vendors):** secure and compliant delivery of outsourced services, including appropriate security, privacy, and AI-related safeguards; meeting contractual and regulatory requirements (e.g., incident notification, subprocessor controls, audit rights), and ensuring reliable, resilient operations.
- **Service providers and platform integrations (e.g. cloud providers):** adherence to contractual security and compliance requirements; responsible handling of data and AI-enabled processing.
- **AI model and API providers:** compliance with contractual AI governance clauses, data-use limitations, ethical AI commitments, and incident notification obligations.

## 3.2 Internal interested parties

- **Leadership and management:** oversight of AI risk and performance; approval of policies, objectives, and resources; assurance of regulatory compliance.
- **Employees and contractors:** clear responsibilities for secure and responsible AI use; training and awareness; mechanisms to report AI-related concerns.
- **Internal business units:** protection of information assets; continuity and resilience of AI-enabled services; integration of legal, ethical, and regulatory requirements into AI processes.

# 4. AIMS framework

The AIMS is established to ensure the responsible design, development, provision, operation, and monitoring of AI systems within the defined scope.

The framework defines processes for:

- AI risk management and impact assessment;
- transparency, accountability, and human oversight;
- lifecycle management of AI systems.

# 5. Scope of the AIMS

Manychat operates an Artificial Intelligence Management System in accordance with the following scope:

> Development, provision, and operation of AI-enabled SaaS functionalities, integrating third-party artificial intelligence services, for AI-enabled functionality, automated conversation and AI-assisted workflow automation within the Manychat platform.
> 

## 5.1 Activities and processes in scope

The following activities and processes are within the scope of Manychat’s Artificial Intelligence Management System (AIMS) insofar as they relate to AI-enabled functionalities of the Manychat platform:

### 5.1.1 AI governance and oversight

- Governance activities related to the definition, approval, review, and maintenance of the AI Policy and related AI governance documentation;
- Allocation and oversight of roles and responsibilities for AI across Product, Engineering, Security, Legal, Compliance, and Customer Support functions;
- Management review and continual improvement of the AIMS.

### 5.1.2 AI risk and impact management

- Activities related to the identification, assessment, and treatment of AI-related risks;
- Performance of AI system impact assessments, including impacts on individuals, groups, and, where relevant, society;
- Maintenance of AI risk and impact assessment records and registers.

### 5.1.3 AI design and feature development

- Design and development activities for AI-enabled product features and workflows;
- Definition of responsible AI objectives and integration of safeguards into feature design;
- Specification and review of requirements for new AI features and material enhancements;
- Documentation of AI system design and AI-enabled feature behaviour.

### 5.1.4 AI integration and configuration

- Selection, configuration, and integration of third-party AI services (e.g. large language model APIs) into the Manychat platform;
- Configuration of prompts, orchestration logic, inference flows, and output constraints;
- Activities related to the definition and application of human oversight and fallback mechanisms for AI-enabled features.

### 5.1.5 AI verification, validation, and testing

- Feature-level verification and validation of AI-enabled functionalities;
- Testing of AI outputs, safeguards, and system behaviour under expected and reasonably foreseeable conditions;
- Validation of integration performance and reliability of third-party AI services.

### 5.1.6 AI deployment and change management

- Planning and execution of deployments of AI-enabled features;
- Change management activities for AI features, including risk-based review prior to release;
- Rollback and remediation activities related to AI functionality.

### 5.1.7 AI operation and monitoring

- Ongoing operation of AI-enabled features in production;
- Monitoring of AI system performance, availability, and abnormal behaviour;
- Logging of AI system events where technically feasible, proportionate, and aligned with risk and contractual constraints;
- Incident detection, response, and communication related to AI systems.

### 5.1.8 Data management for AI systems

- Management of data inputs under Manychat’s control used in AI-enabled features (e.g. prompts, user inputs, metadata);
- Definition and application of data quality requirements and validation checks;
- Documentation of data provenance and data handling practices for AI-related data.

### 5.1.9 Responsible use and transparency

- Definition and enforcement of intended use of AI-enabled features;
- Provision of information to users regarding AI functionality, limitations, and configuration responsibilities;
- Handling of user and stakeholder feedback, including reports of adverse AI impacts.

### 5.1.10 Supplier and third-party management

- Governance of third-party AI service providers used within AI-enabled features;
- Assessment of supplier alignment with Manychat’s responsible AI approach;
- Management of contractual and operational dependencies related to AI services.

## 5.2 Resources supporting AI lifecycle and AI-related activities

Manychat identifies and documents the resources required to support activities within the scope of the Artificial Intelligence Management System (AIMS) across the AI system lifecycle and other AI-related activities.

Resources are identified in a manner proportionate to Manychat’s role as an integrator and operator of AI-enabled systems and include human, technical, and information or governance resources.

| AI lifecycle stage / activity | Key human resources | Key technical resources | Key information & governance resources |
| --- | --- | --- | --- |
| AI governance and oversight | Product, Engineering, Security, Data and Analytics | Internal collaboration tools | AI Policy, AIMS Context & Scope, management review records |
| AI design & feature development | Product Managers, Software Engineers, Data Engineers | Development environments, third-party AI APIs | Design documentation, feature requirements |
| AI integration & configuration | Engineering, Security | AI service configuration tools, orchestration logic | Risk & Impact Assessment records, supplier documentation |
| AI verification & testing | Engineering | Test environments, monitoring tools | Validation and test records |
| AI deployment & change management | Engineering, Operations | CI/CD pipelines | Change records, release approvals |
| AI operation & monitoring | Operations, Support, Security | Monitoring and logging tools | Operational logs, incident records |
| AI risk & impact management | Security, Product | Risk registers, assessment templates | AI Risk & Impact Register, SoA |
| AI incident & concern handling | Support, Security | Ticketing systems | Incident and concern records |
| Management review & improvement | Leadership Team, Security | Reporting tools | KPIs, management review minutes |

### 5.2.1 Data resources

Manychat documents information about the data resources utilized by AI-enabled systems as part of the identification of resources supporting activities within the scope of the Artificial Intelligence Management System (AIMS).

This documentation focuses on data resources under Manychat’s control or influence and is maintained in a manner proportionate to Manychat’s role as an integrator and operator of AI-enabled systems.

| Data resource category | Description | Source | Purpose in AI system | Data ownership / control |
| --- | --- | --- | --- | --- |
| User input data | Messages and text inputs provided via the Manychat platform | End users / customers | Processed by AI-enabled features for conversation analysis and automation | Customer / Manychat (platform control) |
| Prompt configurations | Prompt templates and system instructions defined by Manychat | Manychat | Guide AI behaviour and constrain outputs | Manychat |
| AI outputs | Text or structured outputs generated by AI services | Third-party AI providers | Returned to users as part of AI-enabled functionality | Manychat (delivery and presentation) |
| Usage metadata | Logs, timestamps, and usage indicators related to AI feature use | Manychat systems | Monitoring, troubleshooting, and improvement | Manychat |
| Configuration data | Parameters and settings controlling AI feature behaviour | Manychat | Ensure intended use and safeguards | Manychat |
| RAG retrieval data (message history and user-provided documents) | Conversation history and user-provided content (including uploaded files/documents) stored and indexed to enable retrieval of relevant context for AI-assisted responses. | End users / customers (via Manychat platform) | Used for retrieval-augmented generation (RAG) to retrieve and supply relevant context to AI models at inference time, improving response relevance, continuity, and domain accuracy. | Customer / Manychat (platform control: storage, indexing, access restrictions, retention and deletion controls) |

### 5.2.2 Tooling resources

Manychat documents information about the tooling resources utilized to support AI-enabled systems as part of the identification of resources supporting activities within the scope of the Artificial Intelligence Management System (AIMS).

Tooling resources include internal platforms, development and operational tools, and third-party services used to design, integrate, deploy, operate, monitor, and govern AI-enabled functionalities, in a manner proportionate to Manychat’s role as an integrator and operator of AI-enabled systems.

| Tooling category | Description | Purpose in AI lifecycle | Ownership / control |
| --- | --- | --- | --- |
| AI service platforms | Third-party AI services integrated into the Manychat platform | Provide AI capabilities for conversation analysis and automation | Third-party provider / Manychat (integration & configuration) |
| Development tools | Internal development and testing environments | Design, build, and test AI-enabled features | Manychat |
| Configuration & orchestration tools | Tools used to configure prompts, workflows, and AI feature logic | Control AI behaviour and intended use | Manychat |
| Monitoring & logging tools | Monitoring and logging systems for AI-enabled features | Monitor performance, availability, and abnormal behaviour | Manychat |
| Incident & ticketing tools | Internal ticketing and incident management systems | Handle AI-related incidents and concerns | Manychat |
| Risk & governance tools | Registers, templates, and tracking tools | Support AI risk and impact management | Manychat |

### 5.2.3 System and computing resources

Manychat documents information about the system and computing resources utilized to support AI-enabled systems as part of the identification of resources supporting activities within the scope of the Artificial Intelligence Management System (AIMS).System and computing resources include the infrastructure and platform components used to host, execute, integrate, and operate AI-enabled functionalities, in a manner proportionate to Manychat’s role as an integrator and operator of AI-enabled systems.

| System / computing resource category | Description | Role in AI system | Ownership / responsibility |
| --- | --- | --- | --- |
| Application hosting environment | Infrastructure hosting the Manychat platform and AI-enabled features | Executes and delivers AI-enabled functionality | Manychat |
| Cloud computing infrastructure | Cloud-based compute, storage, and networking resources supporting AI operation | Supports execution, scalability, and availability of AI features | Cloud service provider / Manychat |
| Integration infrastructure | Systems enabling integration between the Manychat platform and third-party AI services | Enables secure communication and data exchange | Manychat |
| Test and staging environments | Non-production environments used for testing AI-enabled features | Verification, validation, and change testing | Manychat |
| Logging and monitoring infrastructure | Systems supporting collection and storage of operational and AI-related logs | Monitoring, troubleshooting, and oversight | Manychat |

## 5.3 Products and services in scope

The following products and services are within the scope of the AIMS to the extent that they include AI-enabled functionalities:

### Manychat platform services

- Manychat Web Application, including AI-enabled features , AI-assisted workflow configuration, and prompt-based AI automation;
- Manychat Mobile Applications (iOS and Android), including access to and interaction with AI-enabled features;
- Manychat Application Programming Interfaces (APIs), where APIs expose, trigger, or support AI-enabled functionalities.

### AI-enabled functionalities (current and future)

- Automated conversation classification (e.g. AI-based labelling and prioritisation);
- AI-assisted onboarding and configuration of AI-driven workflow steps;
- Prompt-based AI steps embedded in automations;
- Any future AI-enabled features introduced into the Manychat platform that rely on machine learning, generative AI, or similar AI techniques and are subject to the AIMS risk and impact assessment process.

## 5.4 Explicit exclusions

The following activities are explicitly excluded from the scope of the AIMS:

- Development, training, and internal governance of AI models provided by third-party AI service providers;
- Customer-defined automations, prompts, and downstream business decisions beyond the controls and safeguards provided by Manychat;
- Non-AI platform functionalities and internal productivity tools that do not affect customer-facing AI-enabled features.

The AIMS scope and exclusions are reviewed periodically to ensure continued suitability, adequacy, and effectiveness, and are updated to reflect technological, regulatory, or organizational changes.

# 6. Information assets, technology, and infrastructure

The AIMS covers information assets and technologies including:

- datasets and data resources used for AI operation , configuration, monitoring, and  validation under Manychat's control ;
- AI models, parameters, artefacts, and technical documentation;
- AI system logs, outputs, and monitoring metrics;
- customer and subscriber data processed by AI-enabled features;
- contracts and records related to AI governance and supplier management.

AI systems are supported by cloud-based infrastructure provided by third-party service providers. AI-related assets are identified and maintained in the **AI Risk Management Register**, and are subject to AI risk and impact assessments in accordance with the AIMS Risk Management Procedure.

# 7. Interfaces and dependencies

The AIMS interfaces with:

- internal business systems supporting AI-related activities;
- internal teams performing roles across the AI lifecycle;
- third-party platforms, integrations, and AI service providers;
- cloud infrastructure providers supporting AI computation and hosting.

Dependencies on third parties are governed through contractual, technical, and organizational controls and are considered as part of AI risk and impact management.

# 8. Organizational and physical boundaries

The AIMS applies across Manychat legal entities and locations involved in AI-related activities, including distributed and remote teams. Physical office locations support governance, development, operations, and support activities relevant to AI-enabled services.

# 9. Statement of Applicability and exclusions

The applicable controls and justifications for inclusion or exclusion are defined in the **AIMS Statement of Applicability (SoA)**, which is maintained as controlled documented information.

## 9.1 Rationale for scope definition

The AIMS scope was defined to ensure responsible and trustworthy operation of AI-enabled features within Manychat products and services. The scope reflects stakeholder expectations regarding transparency, fairness, accountability, and compliance.

## 9.2 Exclusions

Sales, marketing, and source code development activities unrelated to AI system design, development, or operation are excluded from the AIMS scope, as they do not directly influence AIMS objectives.

The AIMS scope is reviewed periodically to ensure continued suitability, adequacy, and effectiveness, and updated to reflect technological, regulatory, or organizational changes.

# **Document History**

| **Version** | **Date of**
**Change** | **Author and Contributors** | **Changes to the previous version** |
| --- | --- | --- | --- |
| 0.1 | 25.01.2026 | **Author**: Sergey Muslaev, GRC Lead | Draft  version |
| 1.0 | 19.02.2026 | **Author**:  Sergey Muslaev, GRC Lead
**Contributors**: Mikhail Kurzin, Head of Security
Thu Nguyen, AI Product Director
Ivan Ilin, AI Research Lead
Xavier Gumara Rigol, Head of Data | Initial version |