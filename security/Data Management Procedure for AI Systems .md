# Data Management Procedure for AI Systems

Owner: Sergey Muslaev
Area: AI
Last edited time: January 22, 2026
Approvers: Dmitry Kushnikov
Document ID: PR-AI-01
Document Type: Procedure
Document application: All Contractors, All Employees
Reviewers: Mikhail Kurzin, Thu Nguyen, Ivan Ilin, Xavier Gumara Rigol
Status: In review
Tag: ISO42001
Version: 1

# Table of Contents

# 1. Purpose

This procedure defines how Manychat manages data used in the **development, integration, deployment, operation, and monitoring of AI-enabled features**, ensuring that data is:

- appropriate for its intended purpose,
- of sufficient quality,
- traceable throughout its lifecycle,
- handled in a secure, privacy-respecting, and responsible manner.

This procedure supports compliance with **ISO/IEC 42001 Annex A (Data for AI systems)** and aligns with **Microsoft Responsible AI Standard – Data Governance & Management (Goal A4)**.

# 2. Scope and Applicability

## 2.1 AI Systems in Scope

This procedure applies to the following AI-enabled features:

| Feature | Description |
| --- | --- |
| Intent Classification | Automated classification of customer intent (e.g. orders, complaints, spam) |
| Pre-Sale AI | Two-way conversational engagement from Instagram posts/stories |
| 24/7 Conversational AI | Automated handling of conversations when creators are unavailable |
| Draft Generation | Context-aware reply suggestions |
| RAG Search | AI-assisted answers based on message history and uploaded files |

## 2.2 AI Model Usage Clarification

Manychat **does not train or fine-tune AI foundation models**.

AI capabilities are enabled through **third-party AI providers (e.g. Azure AI)**.

This procedure therefore applies to:

- **operational data** used by AI features (inputs, prompts, retrieved content, outputs, logs)
- **configuration and orchestration logic** controlled by Manychat

If Manychat introduces **model training or fine-tuning in the future**, **all requirements in this procedure will apply to training, validation, testing, and production datasets** without exception.

# 3. Data Categories Used by Manychat AI Systems

## 3.1 Categories of Data

| Data Category | Examples |
| --- | --- |
| User Inputs | Messages, text inputs, conversation history |
| Prompt Data | System prompts, orchestration logic, configuration parameters |
| Retrieved Data (RAG) | Uploaded files, FAQs, knowledge bases |
| Metadata | Timestamps, message IDs, workflow context |
| AI Outputs | Suggested replies, classifications, generated responses |
| Logs | Event logs, error logs (where enabled and proportionate) |

## 3.2 Data Sources

| Source Type | Description |
| --- | --- |
| Customer-provided | Messages and files provided by platform users |
| System-generated | Metadata, logs, workflow context |
| Configured content | Prompts, automation logic, RAG sources |
| Third-party AI services | Model inference results (no training data) |

## 3.3 Characteristics of Data Sources

Data used by Manychat AI systems is predominantly **dynamic, user-generated, and streamed in real time** through supported messaging channels. The volume, frequency, and content of such data vary depending on customer usage patterns, configuration choices, and end-user behavior.

Manychat exercises control over the **ingestion, processing, storage, retention, and deletion** of operational data used by AI-enabled features. Control over **model training data, model parameters, and internal model behavior** remains the responsibility of the third-party AI service provider.

# 4. Data Acquisition and Selection

Manychat shall ensure that only data **necessary and proportionate** to the intended purpose of each AI-enabled feature is acquired and processed.

Data acquisition and selection for AI systems shall:

- comply with Manychat’s Data Classification Policy and Data Retention Policy;
- follow privacy-by-design and security-by-design principles;
- avoid the collection or processing of unnecessary or excessive data.

Data sources shall be selected based on their relevance, suitability for the intended AI functionality, and compliance with applicable privacy and security requirements. Manychat shall not perform bulk data ingestion, scraping, or secondary use of data for AI purposes outside the documented scope.

# 5. Data Quality Management

## 5.1 Data Quality Principles

Manychat shall ensure that data used to operate AI-enabled features is **appropriate for its intended purpose** and supports the reliability and validity of AI-assisted outputs.

Data quality considerations include accuracy, relevance, completeness, timeliness, and consistency, in line with the principles described in ISO/IEC 25024. Given Manychat’s role as an AI system integrator and operator, data quality controls focus on **operational data**, rather than model training datasets.

## 5.2 Operational Data Quality Controls

Because Manychat does not train or fine-tune AI models, traditional machine learning dataset preparation activities (such as labeling target variables, normalization, scaling, or dataset partitioning) are not applicable under the current scope.

Instead, Manychat implements operational data quality controls, which may include:

- validation of input formats and structures;
- detection and handling of malformed or incomplete inputs;
- contextual consistency checks within AI-enabled workflows;
- monitoring of output anomalies and error patterns.

These controls are intended to reduce the likelihood of incorrect or misleading AI outputs.

## 5.3 Statistical Exploration and Monitoring

Statistical exploration techniques shall be applied **where meaningful and proportionate** to support monitoring, evaluation, and continuous improvement of AI-enabled features.

Such exploration may include analysis of:

- volume and frequency of AI feature usage;
- distribution of intent classifications or response categories;
- occurrence and trends of errors, failures, or user-reported issues.

Statistical exploration is used solely for **operational oversight and quality improvement**, and not for training or optimizing AI models.

# 6. Data Preparation and Transformation

Data preparation activities for AI-enabled features shall be limited to those necessary to support the intended functionality of the system.

Such activities may include:

- formatting and structuring of user inputs;
- aggregation of conversational context;
- retrieval and ranking of relevant documents for RAG-based features;
- filtering or exclusion of unsupported or unsafe content.

All data transformations shall be **deterministic, documented, and auditable**. No synthetic data generation or model-oriented data preparation is performed under the current scope.

# 7. Data Provenance and Traceability

Manychat shall maintain sufficient records to enable traceability of data used in AI systems throughout its lifecycle.

Data provenance records may include information relating to:

- the origin of data (e.g. user input, system-generated data, customer-provided files);
- timestamps of creation, update, and use;
- transformations applied during AI processing;
- retention, deletion, or transfer of control.

Data sharing without transfer of control and internal data transformations are considered part of data provenance.

# 8. Privacy, Security, and Safety Considerations

Data processed by AI-enabled features shall be handled in accordance with applicable data protection laws and Manychat’s information security management system.

Personal data processed by AI features does not exceed the categories already processed by the Manychat platform. Access to AI-related data shall follow least-privilege principles, and appropriate technical and organizational measures shall be applied to protect data confidentiality, integrity, and availability.

AI-specific security and safety threats related to data usage (e.g. unintended disclosure, prompt manipulation) are identified and managed through the AI Risk & Impact Assessment and Incident Management processes.

# 9. Transparency and Explainability

Manychat shall provide appropriate information to users regarding the use of AI-enabled features, including their intended purpose, limitations, and the role of human oversight.

Where transparency or explainability is required, Manychat shall be able to explain:

- the categories of data used by AI features;
- how such data contributes to AI-assisted outputs at a system level;
- the limitations associated with data dependency and AI behavior.

Model-level explainability and training data transparency are inherited from the AI service provider.

# 10. Human Oversight and Responsibilities

AI-enabled features shall be designed and operated to support **human decision-making**, not replace it.

Human oversight mechanisms may include:

- configuration and approval workflows;
- feature toggles, overrides, and escalation paths;
- monitoring and review by designated roles.

Responsibilities for AI data management are shared across Product, Engineering, Security, Compliance, and Customer Support functions, according to their respective roles.

# 11. Monitoring, Review, and Continuous Improvement

Data-related risks, incidents, and performance indicators associated with AI systems shall be reviewed as part of:

- AI Risk & Impact Assessments;
- monitoring and measurement activities;
- management reviews.

This procedure shall be reviewed periodically and updated where necessary to reflect changes in AI features, data usage, regulatory expectations, or third-party AI services.

# **Document History**

| **Version** | **Date of**
**Change** | **Author and Contributors** | **Changes to the previous version** |
| --- | --- | --- | --- |
| 0.1 | 22.01.2026 | **Author**: Sergey Muslaev, GRC Lead | Draft  version |
| 1.0 |  | **Author**:  Sergey Muslaev, GRC Lead
**Contributors**: Mikhail Kurzin, Head of Security
Thu Nguyen, AI Product Director
Ivan Ilin, AI Research Lead
Xavier Gumara Rigol, Head of Data
 | Initial version |