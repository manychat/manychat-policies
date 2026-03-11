# [draft] Meta Platform Data Use Policy

Owner: Mikhail Kurzin, Sergey Muslaev
Approvers: Mike Yan, Dmitry Kushnikov
Status: Draft

**Reviewers:**

- Mikhail Kurzin, Head of Security
- Rei Sayag, Director of Data & Analytics
- Ivan Ilin, AI Research Lead
- Thu Nguyen, Product Director
- Xavier Gumara Rigol, Head of Data

---

## **Definitions**

- **Company Controlled Data**: information we collect directly from users via Manychat that describes their user account and use of the Service (e.g., user email/ID, workspace IDs, flows/config, onboarding checklists, access/audit logs, login history, feature-usage events). It excludes Customer Content processed on behalf of clients and any third-party platform data obtained via integrations (including Meta Platform Data). This category includes all templates, flow libraries, and automation configurations that are created and stored outside the context of a specific Meta thread.
- **Platform Data:** Any data obtained from Meta Platform (directly or indirectly)—**including anonymized, aggregated, or derived data** such as embeddings, features, vectors, or metrics created from Meta data.
- **Tech Provider:** A developer of an app whose primary purpose is to enable users to access/use Platform or Platform Data. We are a Tech Provider.
- **Restricted Platform Data**: Platform Data that (i) can reasonably be used to identify or track a specific person or device (e.g., user IDs, display name, conversation content, tokens, device IDs), or (ii) is collected via Meta’s restricted permissions. It does **not** cover fully de-identified, high-level statistics (e.g., total number of messages per day) that cannot be tied back to an individual or device.
- **User’s Purpose:** The particular user’s permitted use under Meta’s terms and docs (what that user is trying to do inside our app).

---

**Applies to:** All Manychat employees, contractors, and service providers who design, build, test, operate, or analyze features that access Facebook, Instagram, or WhatsApp data via Meta’s Platform (APIs, SDKs).

**Purpose:** Under Meta’s Platform Terms and the WhatsApp Business Solution Terms,, as a **Tech Provider** we may process **Platform Data** **only on behalf of and at the direction of the specific user** whose account we connect—not for Manychat’s own purposes or for any other user. This applies **even to anonymized, aggregated, or derived data**. 

<aside>
💡

> **Reminder**: Our own Terms prohibit using the Services in any way that violates the policies of Facebook/Instagram/WhatsApp. Meta’s rules control when handling Platform Data.
> 
</aside>

---

## 2) Core principles you must follow

- **User-direction only**
    
    Use Platform Data **only** for the benefit of the specific customer and according to their instructions—**never** for Manychat’s own purposes or any other customer. Use it only at runtime for customer-specific needs (delivery, moderation, per-customer analytics, inference-time RAG), and **do not** feed it back into or use it to train shared or cross-client models.
    
- **Strict user data isolation**
    
    Store and process each customer’s Platform Data **separately** from other customer’ data (data stores, indexes, caches, logs, analytics), so it is never merged into shared or cross-customer datasets.
    
- **Content created inside vs. outside a Meta context**
    
    Content that users create and store in Manychat **outside the context of any specific Meta conversation** (e.g., template libraries, generic flows, automation configurations, documentation) is treated as **Company Controlled Data** and is governed by Manychat’s own terms and controls (including possible use in training corpora after de-identification and subject to opt-out).
    
    However, **as soon as a user opens a Meta-sourced thread and sees Platform Data, any text they type or edit in that conversation UI** — including replies, prompts, internal notes, helper text, inserted or modified templates, automation messages, and drafts (even if never sent) — is treated as **Meta Platform-derived data** and is fully subject to Meta’s documentation and restrictions (including “no training” and no cross-customer analytics), even if it does not directly quote the original Meta message.
    
- **Share only when necessary, with guardrails**
    
    Share Platform Data **only**:
    
    - with the applicable user/customer;
    - when legally required;
    - with Manychat service providers **only as needed** to serve that customer and under terms mirroring Meta’s restrictions (e.g., sending conversation text to an LLM **transiently** to generate a reply, without training or long-term storage); or
    - with the customer’s own service provider when they **explicitly direct** us to do so.
        
        Always keep proof of such sharing and directions.
        
- **Minimize & delete**
    
    Collect only what you need, keep it only as long as necessary, and **delete** it when it’s no longer needed, when an end user or customer asks, when the client offboards, or when Meta requires it—subject only to Meta’s narrow exceptions. For example, when a customer disconnects their Meta integration or closes their Manychat workspace, we delete associated Platform Data (conversation logs, user IDs, tokens) under our [Data Retention Policy for inactive accounts](https://help.manychat.com/hc/en-us/articles/14281205806748-Data-Retention-for-inactive-accounts?utm_source=chatgpt.com), which permanently deletes closed accounts and their data within 90 days, keeping only limited audit records where legally required.
    
- **Extra care for Restricted Platform Data**
    
    Access or request Restricted Platform Data **only when strictly needed** to deliver or significantly improve a specific feature the user is actively using and that cannot work without it (e.g., reading message content to generate a reply). Be transparent about this use in the product (UI and/or docs), and follow all Meta Developer Docs for that permission (scope limits, storage/retention, bans on secondary use).
    
- **Security is non-negotiable**
    
    Protect Platform Data using standard security practices: encrypt data in transit and at rest, protect tokens and secrets with limited access, require MFA for sensitive systems, keep basic access logs, and quickly investigate and report any security incident involving Platform Data through Meta’s process. **Follow the Security team’s guidance, and if you’re unsure what to do, ask them before you proceed.**
    

---

## 3) What you **can** do with Meta data (valid use cases)

You may process Platform Data **only** if it is **(a)** necessary for a feature the specific user is using, **and (b)** squarely within Meta’s Platform Terms and Developer Policies.

**Examples (OK):**

- **Messaging & automation requested by the user**
    
    Receive content and metadata via Messenger/Instagram/WhatsApp APIs, trigger automations, respond within Meta’s messaging policies and windows, and store the minimal state to execute the flow for that user. 
    
- **Per‑user analytics/insights for that user**
    
    Compute delivery rates, response times, funnel step‑through, etc., **only visible inside that customer’s account** and used to improve that user’s experience; delete under Meta’s triggers. 
    
- **Per‑user retrieval or transformation for real‑time assist**
    
    Create ephemeral features (e.g., per‑user vector indexes or templates) to **generate** replies for that user’s conversations. Treat embeddings/vectors as **Platform Data** (derived) and keep **strictly per‑user**; do **not** reuse across users. 
    
- **Operational logging, security and support**
    
    Keep minimal logs needed to run, secure, and support the app; secure them; delete promptly per retention and customer/end-user requests; report breaches to Meta. 
    
- **Service providers usage** (DWH, infra, monitoring, etc.) **only as necessary** to deliver the user’s feature, under written terms that (i) bind the provider to process Platform Data **solely** for that user’s purpose; (ii) require deletion upon termination; and (iii) flow down Meta’s restrictions.

<aside>
💡

> Note on Manychat’s own legal docs: Our DPA and Privacy Policy allow us to use anonymized Customer Content for product improvement or analytics; however, when the data is Meta Platform Data, Meta’s rules govern. Because Meta defines Platform Data to include anonymized/aggregated/derived data, anonymization does not convert it into non‑Platform data. Do not rely on anonymization to reuse Meta‑sourced data for Manychat’s own purposes.
> 
</aside>

---

## 4) What you **cannot** do with Meta data

- **No Manychat‑wide training**
    
    Do **not** train, fine‑tune, or otherwise adapt **any** Manychat‑owned or vendor foundation model on Platform Data (including “anonymized,” “aggregated,” “de‑identified,” embeddings, or features). As a Tech Provider we may **not** use Platform Data for our own purposes. 
    
- **No cross‑user pooling**
    
    Never mix Platform Data between users (for any analytics, scoring, quality models, or benchmarks). Maintain strict per‑user separation. 
    
- **No user profiling, selling, licensing, or re‑identification**
    
    Do not sell/license Platform Data; do not build or augment user profiles; do not attempt to de‑anonymize/rewrap hashed IDs; do not use for surveillance or eligibility decisions.
    
- **No purpose creep**
    
    Don’t process Platform Data outside the permitted purposes in Meta’s Developer Docs; re‑submit to App Review before materially changing processing scope. 
    
- **No requesting Restricted Platform Data unless necessary**
    
    Only request Restricted data if **necessary** to meaningfully improve that user’s experience, and be explicit with the user. 
    

These restrictions apply in all cases—whether Platform Data is obtained through official integrations or any alternative means (e.g., data crawling).

---

## 5) Using LLMs and AI systems with Meta data

**AI / LLM usage over Platform Data**

- You **may** send Platform Data to external LLM/AI vendors when needed to deliver a user-requested feature, but only as **runtime, per-user processing**.
- **Hard rule: no training.** Neither Manychat nor vendors may use Platform Data (including “anonymized,” aggregated data, embeddings, or features) to train, fine-tune, evaluate, or improve shared/cross-client models.
- Treat vendors as **Service Providers**: limit use to that client’s purpose, forbid secondary use and unnecessary retention, require deletion on request/termination, and flow down Meta’s restrictions.
- Any feature that sends Platform Data to AI/LLM must get **Security & Legal sign-off before launch**.

> Important: Embeddings, prompts, caches, and model outputs computed from Platform Data are “derived data” and therefore Platform Data subject to the same restrictions. Keep them per‑user, minimize retention, and delete on Meta/user/user triggers.
> 

---

## 6) Data retention & deletion triggers (build these into jobs and playbooks)

Delete Platform Data **as soon as reasonably possible** when:

- no longer necessary for a legitimate purpose consistent with Meta’s terms;
- a user asks for deletion or closes account;
- a user asks for deletion or offboards;
- Meta requests deletion; or
- when we stop operating the product/service through which it was acquired.
    
    Maintain proofs where Meta requires them. 
    

> Note: Meta allows limited retention where data has been aggregated/obscured/de‑identified so it cannot be associated with a particular user/browser/device, but it remains “Platform Data” and cannot be repurposed for Manychat’s own objectives. Apply all restrictions.
> 

Service providers must **promptly delete** Platform Data when we stop using them. 

---

## 7) Engineer “Do & Don’t” checklist

**✅ Do**

- Scope every use of Platform Data to **one customer (account)** and a **specific feature**.
- Treat embeddings, features, summaries, prompts, model outputs and caches as **Platform Data**: keep them **per customer**, use the **minimum needed**, and hook deletion to Meta / customer / user / offboarding triggers.
- Use Platform Data only for **runtime** (delivery, moderation, per-customer analytics, inference-time RAG) — not for training.
- Keep data stores, indexes, caches, logs and analytics **separated per customer**.
- Before sending Platform Data to any external AI/infra/DWH/monitoring vendor, involve **Security and Legal** and treat the vendor as a **Service Provider** (no training, limited retention, deletion, Meta flow-downs).

---

**⛔️ Don’t**

- Don’t train, fine-tune, evaluate or improve **any** model (internal or vendor) on Platform Data, including “anonymized” or aggregated data, embeddings or features.
- Don’t pool Platform Data across **customers or their end users** for quality, benchmarking, safety or other cross-customer analytics.
- Don’t export Platform Data or raw logs into **shared** BI tools, notebooks or sandboxes.
- Don’t build or enrich profiles for Manychat’s own purposes; don’t sell or license Platform Data; don’t re-identify; don’t use it for eligibility decisions (credit, jobs, insurance, etc.).
- Don’t request or store **Restricted Platform Data** unless it is clearly necessary for the customer’s (or their end users’) experience and documented for that feature.
- Don’t skip **Security/Legal** review when you change what Platform Data you collect, where you store it, or which vendors/models you send it to.

---

## 8) Approvals & exceptions

Any exception to this policy (including experimental research, cross‑user statistics, or non‑ephemeral AI processing) **requires prior written approval** from Security Team, with documented scope, legal basis, retention plan, and Meta compliance mapping.

---

## Appendix: quick references

- [Meta **Platform Terms**](https://developers.facebook.com/terms/dfc_platform_terms/preview): Tech Provider limitations; sharing; retention/deletion; prohibited practices; security & incident reporting; audits.
- [Meta **Developer Policies**](https://developers.facebook.com/devpolicy/preview): general product/messaging rules.
- [Meta **Data Security Requirements**](https://developers.facebook.com/docs/resp-plat-initiatives/individual-processes/data-protection-assessment/data-security) (DPA guide): encryption, MFA, device controls, testing, secrets.
- [Manychat **DPA**](https://manychat.com/legal/dpa) / [**Privacy Policy**](https://manychat.com/legal/privacy) / [**Terms**](https://manychat.com/legal/tos) (applied subject to Meta’s rules).
- WhatsApp Business Solution Terms (preview): channel-specific rules for use of WhatsApp Business messaging – [https://www.whatsapp.com/legal/business-solution-terms/preview](https://www.whatsapp.com/legal/business-solution-terms/preview)

.