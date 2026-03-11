# AI System Impact Assessment (AISIA) Procedure

Owner: Sergey Muslaev
Verification: Verified
Area: AI
Last edited time: January 26, 2026
Approvers: Dmitry Kushnikov
Document ID: PR-AI-03
Document Type: Procedure
Document application: All Contractors, All Employees
Effective date: March 3, 2026
Reviewers: Mikhail Kurzin, Thu Nguyen, Ivan Ilin, Xavier Gumara Rigol
Status: Approved
Tag: ISO42001
Version: 1

# 1. Purpose

This procedure defines the context, scope, and boundaries for conducting AI system impact assessments (AISIA) at Manychat. It ensures the evaluation of potential effects on individuals and society, addressing both intended and unintended consequences of AI deployment.

In practical terms, this procedure helps Manychat teams identify and document how an AI-enabled feature could affect individuals, customers, and society before and during deployment. It ensures that impacts are systematically evaluated, discussed, and addressed as part of product development and change management processes.

This procedure is integrated with Manychat’s Information Security Management System (ISMS), AI risk management processes, and Artificial Intelligence Management System (AIMS) to ensure that **impacts are assessed independently of risk likelihood and are used as an input into AI risk management and decision-making**. 

This procedure supports the implementation of AI system impact assessment requirements referenced in ISO/IEC 42001 Annex B and is designed to align with ISO/IEC 42005 guidance.

## 1.2 Scope and Applicability

This procedure applies to all AI-enabled systems and features developed, integrated, or operated by Manychat.

Manychat acts as a provider and deployer of AI-enabled systems within the meaning of Article 3 of the EU AI Act. The procedure does not apply to the internal modification  of AI foundation models, which are managed by third-party AI service providers.

Where Manychat introduces model training or fine-tuning in the future, this procedure shall also apply to the assessment of impacts arising from training data, validation data, and model behavior.

# 2. Impact Taxonomy

Manychat recognizes that effective AI governance depends on understanding the needs of interested parties. In accordance with **ISO/IEC 42005**, impacts are classified as follows:

## 2.1 Individual Impacts

- **Privacy & Data:** Risks to personal data processed through the Manychat platform, including data collected via messaging integrations (e.g., Facebook, Instagram, WhatsApp), user interactions, and platform features.
- **Fairness:** Potential for bias or non-discrimination issues in AI outcomes.
- **Transparency:** Requirements for the explainability of AI features to customers and end-users.

## 2.2 Societal Impacts

- **Trust & Safety:** Risks of misinformation or misuse of AI-generated content.
- **Sustainability:** Environmental considerations related to computation and data processing.

## 2.3 Organizational Impacts

- **Compliance:** Alignment with global data protection laws (GDPR, CCPA) and AI regulations (EU AI Act, NIST AI RMF).
- **Reputation:** Potential loss of trust or customer harm arising from AI failures.

Impact identification shall consider both **actual and reasonably foreseeable impacts**, including impacts resulting from system failures, misuse, over-reliance on AI outputs, and changes in deployment context. Impacts may be positive or negative and may arise directly or indirectly from the operation of the AI system.

The assessment shall document the relevant demographic groups or populations to which the system is applicable based on the feature’s intended purpose, channels, supported languages, and foreseeable user groups, without requiring the collection of sensitive demographic attributes unless explicitly justified and permitted.

# 3. Measurement Methodology

## 3.1 Severity (Magnitude)

Severity is evaluated based on the scale and nature of processing. It represents the **magnitude of harm or benefit**, independent of likelihood, and reflects the seriousness, scale, and reversibility of impact on affected parties.

The impact scale used in this procedure is aligned with the organizational risk impact scale defined in the Risk Management Procedure.

| Severity Level | **Value** | **Description of the Impact options:** |
| --- | --- | --- |
| **Extreme** | 5 | Severe, widespread, or irreversible harm |
| **Major** | 4 | Serious impact affecting multiple parties or trust |
| **Moderate** | 3 | Noticeable impact affecting individuals or operations |
| **Minor** | 2 | Limited and reversible impact |
| **Trivial** | 1 | Negligible impact with no meaningful harm |

## 3.2 Probability (Likelihood)

Probability shall be rated using the categories Frequent, Likely, Possible, Unlikely and Rare as defined by operational evidence, historical incidents, monitoring signals, and foreseeable misuse scenarios for the relevant lifecycle stage.

Probability is rated using the same categories defined in the Risk Management Procedure and reflects the foreseeability of an impact occurring during the AI system lifecycle.

Probability represents the **foreseeability of an impact occurring** within the AI system lifecycle and is used to support prioritization and escalation decisions, not to replace risk assessment.

The following non-exhaustive factors may influence the assessment of probability depending on the AI system’s design, deployment context, and lifecycle stage:

- **System Complexity:** Use of RAG (Retrieval-Augmented Generation), external knowledge sources, and third-party APIs increases system architecture complexity and operational dependencies. While RAG may reduce hallucinations by grounding outputs in retrieved information, it introduces additional components (e.g., retrieval pipelines, indexing, external data sources) that require monitoring and governance and may influence the likelihood of inaccurate or inconsistent outputs if not properly managed.
- **Data Characteristics:** The scale, granularity, sensitivity, diversity, and provenance of data processed by the AI system may influence the likelihood of inaccurate, biased, privacy-intrusive, or non-compliant outcomes.
- **Human Oversight:** Defined responsibilities for monitoring AI outputs lower the probability of unmitigated harm.

# 4. Impact Rating Matrix

The intersection of Severity and Probability defines the **Impact Rating**, which dictates the required approval level. The resulting impact rating shall be used to determine escalation, approval, and mitigation requirements. Impact ratings do not represent risk acceptance decisions and shall be used as an input into AI risk management activities in accordance with the Risk Management Procedure.

| Impact / Probability | 1 – Trivial | 2 – Minor | 3 – Moderate | 4 – Major | 5 – Extreme |
| --- | --- | --- | --- | --- | --- |
| 5 – Frequent | Medium | High | High | Critical | Critical |
| 4 – Likely | Low | Medium | High | High | Critical |
| 3 – Possible | Low | Medium | Medium | High | High |
| 2 – Unlikely | Low | Low | Medium | Medium | High |
| 1 – Rare | Low | Low | Low | Medium | Medium |

# 5. Data Collection & Resources

Assessments must be evidence-based, utilizing data from the following AIMS resources:

- **Technical Resources:** Monitoring and logging tools, CI/CD pipelines, and third-party AI APIs.
- **Data Resources:** User input data (including end-user prompts and interaction content), system and template prompt configurations (including engineered instructions and retrieval queries), and RAG retrieval data.
- **Human Resources:** Input from Product Managers, Software Engineers, and Security teams.
- **Information Assets:** AI system logs, risk registers, and Statement of Applicability (SoA).

Data and resources shall be collected and reviewed with respect to the **relevant AI system lifecycle stage**, including design, testing, deployment, operation, and change.

Evidence sources may include AI feature documentation, Help Center disclosures, monitoring dashboards, incident and concern reports, and supplier documentation provided under vendor management.

# 6. Thresholds & Approvals

- **Low/Medium Impact:** Approved by Product and Engineering Leads.
- **High/Critical Impact:** Exceeds sensitive use thresholds; requires formal Management Review and AIMS Owner approval.
- **Mandatory Reassessment:** Triggered by significant changes to AI functionality, data inputs, or the deployment environment.

Probability shall be rated using the categories Frequent, Likely, Possible, Unlikely and Rare as defined by operational evidence, historical incidents, monitoring signals, and foreseeable misuse scenarios for the relevant lifecycle stage.

Where an impact is rated Major or Critical, continuation or deployment of the AI system is subject to completion of required actions and an explicit go/no-go decision by the approving authority.

## 6.1 Assessment Triggers

An AI system impact assessment shall be conducted prior to the initial deployment of an AI-enabled system and shall be reviewed or updated when significant changes occur, including changes to system functionality, data inputs, deployment context, affected populations, or following significant incidents or concerns.

## **6.2 Monitoring and Review**

Actual impacts observed during operation shall be monitored and compared against assessed impacts. Where discrepancies are identified, the assessment shall be reviewed and updated accordingly.

## **6.3 AISIA Process**

The AI System Impact Assessment process shall include the following activities and outputs. Manychat shall identify potential positive and negative impacts arising from the intended use and reasonably foreseeable misuse of the AI system, including predictable failures and their consequences. The organization shall analyze identified impacts by assessing severity and foreseeability using the methodology defined in Sections 3 and 4 and shall evaluate whether impacts are acceptable in the intended context of use. Where impacts are not acceptable or exceed defined thresholds, the organization shall determine and document required actions, which may include design changes, additional safeguards, increased human oversight, monitoring requirements, or escalation for approval. The organization shall document results, decisions, and required actions, and shall communicate outcomes to relevant interested parties in accordance with AIMS communication and documented information controls.

# 7. Roles, Responsibilities, and Independence

The AI System Impact Assessment shall be performed by designated personnel with sufficient competence and knowledge of the AI-enabled feature and its context of use. The assessment shall be reviewed by a function independent from the feature owner for assessments rated High or Extreme, such as Security, or the AIMS Owner. Approval responsibilities defined in Section 6 shall be applied based on the resulting impact rating. Conflicts of interest shall be avoided by ensuring that the final acceptance decision for High or Extreme impact assessments is not made solely by the feature development owner.

# 8. AISIA Record and Required Content

For each AI-enabled system or material enhancement, the organization shall retain an [AISIA record](https://docs.google.com/spreadsheets/d/1rE8tX-HBUR_SsFnqrzs3cn2WbTZLRA_8/edit?gid=1852662965#gid=1852662965) that includes the AI system identification, intended use, foreseeable misuse, affected parties including individuals, groups, and society as applicable, relevant demographic applicability, data categories used, human oversight capabilities and limitations, predictable failures and associated impacts, severity and foreseeability ratings, resulting impact rating, required actions and approvals, monitoring requirements, and references to related AIMS records including the AI risk register and incident records where applicable. AISIA records shall be managed as documented information in accordance with AIMS documented information controls.

# **Document History**

| **Version** | **Date of**
**Change** | **Author and Contributors** | **Changes to the previous version** |
| --- | --- | --- | --- |
| 0.1 | 26.01.2026 | **Author**: Sergey Muslaev, GRC Lead | Draft  version |
| 1.0 | 03.03.2026 | **Author**:  Sergey Muslaev, GRC Lead
**Contributors**: Mikhail Kurzin, Head of Security
Thu Nguyen, AI Product Director
Ivan Ilin, AI Research Lead
Xavier Gumara Rigol, Head of Data
 | Initial version |