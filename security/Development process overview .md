# Development process overview

Owner: Kate Vekova
Area: Development
Approvers: Anastasia Shchogoleva, Mikhail Kurzin
Document ID: REC-DEV-01
Document Type: Standard
Document application: All product teams
Effective date: May 4, 2022
Status: Published
Tag: ISO27001
Version: 2.1

<aside>

**Key points:**

- Product areas
- Communities of practice
- Cybersecurity review
- Organization of scrum team work
</aside>

<aside>

*This standard sets the key principles and requirements for the SCALED SCRUM process at Manychat.*

</aside>

---

# Table of contents

---

# **GENERAL**

The document is intended for internal use. The goal of the document is to familiarize the employees with the organizational process of Scrum product development in ManyChat.

The document is not strictly fixed regulations for the organization of the product development process.

# **DESCRIPTION OF THE LARGE SCALE SCRUM (LESS) PROCESS**

At Manychat in Research & Development (R&D), the product development process is based on the following principles and guides:

- Agile Manifesto: [http://agilemanifesto.org/iso/en/manifesto.html](http://agilemanifesto.org/iso/en/manifesto.html);
- Large Scale Scrum Principles [https://less.works/less/principles](https://less.works/less/principles)
- The official Scrum Guide [https://www.scrumguides.org/](https://www.scrumguides.org/)
- LeSS & LeSS Huge frameworks [https://less.works/less/framework](https://less.works/less/framework) & [https://less.works/less/framework/introduction#LeSSHugeFramework](https://less.works/less/framework/introduction#LeSSHugeFramework)

![output-onlinepngtools.png](Development%20process%20overview/output-onlinepngtools.png)

## **Scaled Scrum IMPLEMENTATION AT MANYCHAT AS A PROCESS:**

[](https://lh7-us.googleusercontent.com/2plPFJXO96OW-XZREQCOFPtKW4ZzlMwLgS711wMvXbs9_h_xaHcuBk-GP9Bqjo2YTx7JojQvqtxH2jRKDbcQJ_jaIYcZkzR4SsmNp6BcD2XtvVXjm1BFgr26C6KAzJuUEsOfWC5viGJjJPv6-kJKMg)

## **Scaled Scrum IMPLEMENTATION AT MANYCHAT AS A STRUCTURE:**

[](https://lh7-us.googleusercontent.com/G3QS4lOPw93nT2UfhwK7Lh9RnhvDN42pQ9OAPi-rw-a5dhWADNZVcjfnuVoe_EvqWf6WRIZi_PuRZiNW8HvPGXx-HhRXEs53XVoB4Tq_s45RVD4bLyiTnRNe96gKyiHXiBgcZ05HQT_FEO1V8HRlPQ)

## **PRODUCT UNITS & AREAS**

The product group consists of several units and areas formed around business requirements and goals. 

The area’s size is from 2 to 8 product teams. Areas are dynamic. Over time an area will change in importance, and then it grows or shrinks with teams joining or departing — to or from the other area.

Product teams focus on one Area Product Backlog managed by Area Product Owner.

There is one product-level Sprint, not a different Sprint for each area. It ends in one integrated whole product.

The number and composition of product areas may vary depending on the business  needs.

## **AREA PRODUCT OWNER**

Each area has an Area Product Owner who specializes in that area and focuses on its Area Product Backlog.

Area Product Owner is accountable for maximizing the value of the product resulting from the work of the product teams.

Area Product Owner is also accountable for effective Area Product Backlog management, which includes:

- Communicating the Product Goal;
- Creating and clearly communicating Area Product Backlog items;
- Ordering Area Product Backlog items; and,
    
    Ensuring that the Area Product Backlog is transparent, visible and understood.
    

## **PRODUCT TEAMS**

Manychat Product Group is represented by Product Teams (Web, Mobile Teams, Infrastructure Team, Product Owner Team, and System Partner).

Each Product Team:

- is [self-managing](https://less.works/less/management/self_managing_teams)
- is cross-functional — all skills required are inside the team or the team can acquire them
- shares responsibility for all the team’s work
- has a shared team goal
- has responsibility for managing its own relationships with external teams and people
- Is dedicated — each team member is dedicated for 100% of his time to one and only one product team
- Is long-lived — product team stays together ‘forever’

The core competencies in each Product Team are: backend, frontend, design.

The core competencies in Mobile Team are iOS, Android, backend, design.

The entire Product Team is accountable for creating a valuable, useful Increment every Sprint.

The current list of product teams with corresponding team members:

[https://miro.com/app/board/uXjVJIkkWj4=/?share_link_id=920036281411](https://miro.com/app/board/uXjVJIkkWj4=/?share_link_id=920036281411)

## **COMMUNITIES OF PRACTICE**

Communities of Practice are groups of people who share a concern, a set of problems, or a passion about a topic, and who deepen their knowledge and expertise in this area by interacting on an ongoing basis.

Communities of Practice (CoP) are rooted in self-organization. They do not appear on an organization chart. Participation is voluntary—people engage because they have a passion to learn or contribute.

There are key communities in Manychat: Frontend community, Backend community, Design Community, iOS community, Android Community. Communities can emerge and terminate on their own using the principle of self-organization.

## **SYSTEM PARTNER**

At Manychat there are full-time System Partners.

They serve Product Teams, Area Product Owners, Product Group as a whole system.

System Partners teache Scaled Scrum to the organization and coach them in their never-ending adoption. They have mastered Scrum and use this deep Scrum understanding to guide everybody to discover how they can best contribute to creating the most valuable product.

System Partners:

- coach Product Teams and Product Areas
- facilitate events and stakeholder collaboration
- teach Manychat Scaled Scrum, empirical control process, system thinking, etc.
- help Manychat to reflect and improve towards their perfection vision
- uphold Scrum Values, Agile and LeSS principles
- are change agents.

## **CYBERSECURITY TEAM**

The Cybersecurity team ensures that security requirements are met and risks assessed in the Scrum product development process. It integrates security into continuous integration, continuous delivery, and deployment pipeline.

The Cybersecurity team should be involved at the following Scrum product development stages:

1. [Security Design Review](https://www.notion.so/Security-Design-Review-Guidelines-d15ed5c0a54c4324bc6e3a47bad94aad?pvs=21) and Threat-Modeling at **Product Roadmap planning** for cyber-risk assessment of new business requirements.
2. **PBR** for assessing cyber-related risks.
3. **Sprint Planning and Review** for tracking progress on cyber-related issues.
4. **Development** for [Security Code Review](https://www.notion.so/Security-Code-Review-Guidelines-480d2194da57446da78d4377d70b4802?pvs=21) of Github repositories(e.g. backend/frontend/etc.) and Pull Requests using the **Semgrep Pro** as SAST, SCA and secret scanning tool and manual code review according to [Secure Code Best Practice](https://www.notion.so/Secure-Coding-Best-Practices-c6ab1c5f9c6c484684d4c2c8f8094515?pvs=21) at “Code Review” status (see PRODUCT ARTIFACTS section of this document) and alerting for any possible vulnerability findings in repository-related Slack channels like vulnrs-front, vulnrs-back, vulnrs-analytics, etc.
5. and upon any ad-hoc request form Product Team (example, security check for planned technical architecture of a new feature).

# **SCALED SCRUM EVENTS**

There are 3 events which are common for both Product Areas:

- **Sprint**. There is one product-level Sprint leading to one integrated [Potentially Shippable Product Increment](https://less.works/less/framework/potentially-shippable-product-increment). The length is 2 weeks.
- **Sprint Review.** It is an inspect-adapt point at the end of the Sprint for all of the Product Teams and stakeholders to review the potentially shippable Product Increment together. The focus is on the whole product.
- **Overall Retrospective.** Its purpose is to discuss cross-team, organizational and systemic problems within the organization.

There are also events that take place separately in each Product Area or Product Team:

- **Product Backlog Refinement.** Ongoing Product Backlog Refinement (PBR) is needed within each Sprint to refine items to be ready for future Sprints. Key activities of PBR are (1) splitting big items, (2) clarifying items until ready for implementation without further “what” questions, and (3) estimating size, “value”, risks, and so forth. In short form: split, clarify, estimate.

There are 3 types of PBR: Multi-team PBR, Overall PBR, Single-team PBR.

![output-onlinepngtools (1).png](Development%20process%20overview/output-onlinepngtools_(1).png)

- **Sprint Planning** consists of two parts that boil down to what and how. **Sprint Planning One** focuses on selection of ready items from those offered by the Area Product Owner, wrapping up lingering questions, and definition of the Sprint Goal. **Sprint Planning Two** focuses on creating a plan of work to get to ‘done’ for each item. The items and plan of action or tasks comprise the Sprint Backlog.

![output-onlinepngtools (2).png](Development%20process%20overview/output-onlinepngtools_(2).png)

- **Daily Scrum.** The purpose of the Daily Scrum is to inspect progress toward the Sprint Goal and adapt the Sprint Backlog as necessary, adjusting the upcoming planned work. The Daily Scrum can be used for coordination between teams by having people from other teams join in to observe. Based on information learned during the Daily Scrum, team members may decide to have follow up discussions outside the Daily Scrum.
- **Area Sync.** Daily short meeting for Product Area to check progress toward the Sprint Goal. Area Sync can be used for coordination between teams – there are representatives from each Product Team there. Area Product Owner can also attend the Area Sync.
- **Team Retrospective.** The purpose is to plan ways to increase quality and effectiveness. Each Product Team inspects how the last Sprint went with regards to individuals, interactions, processes, tools, and their Definition of Done. They discuss what went well during the Sprint, what problems it encountered, and how those problems were (or were not) solved.

![output-onlinepngtools (3).png](Development%20process%20overview/output-onlinepngtools_(3).png)

## **PRODUCT ARTIFACTS**

There are several levels of product development planning.

1. **Product Goal.** The Product Goal describes a future state of the product which can serve as a target for the Scrum Team to plan against. At Manychat Product Goal represented through OKRs.
2. **Product Roadmap.** A product roadmap is a strategic plan of action for how a product or solution will evolve over time. Head of Product and Area Product Owners in collaboration create Product Roadmaps based on Product Goal and OKRs.
3. **Area Product Backlog.** It is an ordered list of deliverables required to execute the strategic plan set forth in the roadmap. The Area Product Backlog should communicate what’s next on the Product Team’s to-do list as they execute on the Product Roadmaps’ big-picture vision.

## **AREA PRODUCT BACKLOG**

In each Product Area multiple teams build a single product work from a single Area Product Backlog that defines all of the work to be done.

The Area Product Backlog is an emergent, ordered list of what is needed to improve the product. It is the single source of work undertaken by the Product Teams.

The Area Product Backlog:

- Is ordered by the Area Product Owner.
- Has items described and sized.

## **SPRINT BACKLOG**

The Sprint Backlog is composed of the Sprint Goal (why), the set of Product Backlog items selected for the Sprint (what), as well as an actionable plan for delivering the Increment (how).

Sprint Backlog is owned by the Product Team. The Product Team chooses suitable tools to manage Sprint Backlog on their own.

Inside the sprint, the development process is continuous (Continuous Delivery). In ManyChat, the deployment process takes place on a daily basis, so the Scrum team goes through all the main stages of development within the sprint:

| **Status** | **Purpose** |
| --- | --- |
| Inbox | The new task (YouTrack issue) without description is awaiting PBR. |
| PBR | Prioritized tasks are  ready for PBR. |
| Ready | The task is ready for development (PBRd, prioritized) |
| In progress | The task is in the development process. |
| On hold | The task is on pause. No work conducted, blocker exist. |
| Won't fix | The product decision has been made that the task won’t be done. |
| Done | The task is deployed on the production servers and meets [DoD criteria](https://www.notion.so/Definition-of-Done-DoD-ef88628c11134ec789ce56a6dc755081?pvs=21). |

## **ORGANIZATION OF SCRUM TEAMS WORK**

All Scrum teams record artifacts and keep records of their work in the YouTrack product.

Each Scrum team within the YouTrack  product has its own team Team Space.

The Team Space contains, but is not limited to, the following:

- Backlog;
- Current sprint;
- Next sprint;
- Team Processes;
- Archive.

Scrum teams lead all their core activities in Miro, Notion, YouTrack, Google Calendar and other business systems.

# **Administration**

| **Signs-off** |  |
| --- | --- |
| [Anastasia Shchogoleva](mailto:ashchogoleva@manychat.com) | Head of Operations |
| Dmitry Mironov | Cross-Functional Manager (Development) |
| [Irina Skrypnik](mailto:ira@manychat.com) | Agile Lead |

# **History**

| **Version** | **Description** | **Author** | **Date** |
| --- | --- | --- | --- |
| 0.1 | Initial version for discussion | [Mikhail Kurzin](mailto:kurzin@manychat.com) | 03.10.2021 |
| 1.0 | First approved version | [Irina Skrypnik](mailto:ira@manychat.com) | 04.05.2022 |
| 2.0 | Updated branding
Cybersecurity team section updates | [Mikhail Kurzin](mailto:kurzin@manychat.com) | 16.07.2024 |
| 2.1 | Document review | [Mikhail Kurzin](mailto:kurzin@manychat.com) | 06.06.2025 |