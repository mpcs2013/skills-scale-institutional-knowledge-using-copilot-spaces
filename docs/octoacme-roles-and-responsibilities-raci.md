# OctoAcme — Roles & Responsibilities RACI

## Purpose
Provide a lightweight RACI matrix that maps key project activities across the lifecycle to the roles defined in [Roles & Personas](./octoacme-roles-and-personas.md). Use this document to assign clear ownership, avoid duplicated effort, and identify gaps during project setup.

## RACI Key
| Code | Meaning |
|------|---------|
| **R** | Responsible — does the work |
| **A** | Accountable — single DRI; approves and owns the outcome |
| **C** | Consulted — provides input before the activity or decision |
| **I** | Informed — kept up to date on progress or outcomes |

> **DRI (Directly Responsible Individual):** Every activity should have exactly one **A**. The DRI is the person who answers if something goes wrong and who makes the final call when there is disagreement.

---

## RACI Matrix

### Initiation Phase
> Reference: [Project Initiation Guide](./octoacme-project-initiation.md)

| Activity | Project Manager | Product Manager | Developer | QA Lead | UX/UI Designer | DevOps Engineer | Business Analyst | Security Champion | Customer Success Manager |
|----------|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| Define problem statement & business case | C | **A** | I | I | C | I | **R** | C | C |
| Identify stakeholders & communication plan | **A** | R | I | I | I | I | R | I | C |
| Draft Project One-pager | **A** | R | I | I | C | I | R | C | C |
| Confirm team composition & roles | **A** | C | C | C | C | C | C | C | I |
| Initial risk identification | **A** | C | C | C | C | C | R | R | I |
| Go/no-go decision | C | **A** | I | I | I | I | C | C | I |

---

### Planning Phase
> Reference: [Project Planning](./octoacme-project-planning.md)

| Activity | Project Manager | Product Manager | Developer | QA Lead | UX/UI Designer | DevOps Engineer | Business Analyst | Security Champion | Customer Success Manager |
|----------|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| Kickoff meeting facilitation | **A** | R | R | R | R | R | R | R | I |
| Backlog creation & prioritization | C | **A** | C | C | C | I | R | C | C |
| Backlog refinement & acceptance criteria | C | **A** | R | R | C | I | R | C | I |
| UX/design artifacts & handoff | I | C | R | I | **A** | I | C | I | I |
| Estimation & capacity planning | **A** | C | R | R | R | R | C | I | I |
| Define Definition of Done | **A** | C | R | R | I | C | C | C | I |
| Test strategy & QA approach | C | C | R | **A** | I | C | C | C | I |
| Security requirements & threat model | C | C | C | C | I | C | C | **A** | I |
| CI/CD pipeline & environment setup | C | I | C | C | I | **A** | I | C | I |
| Release plan & milestone map | **A** | C | C | C | C | R | C | I | C |
| Risk register setup | **A** | C | C | C | I | C | R | R | I |

---

### Execution Phase
> Reference: [Execution & Tracking](./octoacme-execution-and-tracking.md)

| Activity | Project Manager | Product Manager | Developer | QA Lead | UX/UI Designer | DevOps Engineer | Business Analyst | Security Champion | Customer Success Manager |
|----------|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| Daily standup facilitation | **A** | I | R | R | R | R | I | I | I |
| Feature implementation | I | I | **A** | C | C | C | I | C | I |
| PR review & merge | I | I | **A** | C | I | C | I | C | I |
| Security review of PRs | I | I | R | I | I | I | I | **A** | I |
| QA / acceptance testing | C | C | R | **A** | I | I | C | I | I |
| Board management & status updates | **A** | I | R | R | R | R | I | I | I |
| Blocker escalation (Level 1) | R | I | **A** | C | C | C | C | C | I |
| Blocker escalation (Level 2+) | **A** | R | I | C | I | C | I | C | I |
| Risk register updates | **A** | C | C | C | I | C | R | R | I |
| Weekly sync facilitation | **A** | R | I | I | I | I | I | I | I |

---

### Release Phase
> Reference: [Release & Deployment Guide](./octoacme-release-and-deployment.md)

| Activity | Project Manager | Product Manager | Developer | QA Lead | UX/UI Designer | DevOps Engineer | Business Analyst | Security Champion | Customer Success Manager |
|----------|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| Pre-release sign-off coordination | **A** | C | I | R | I | R | I | R | I |
| QA release sign-off | I | C | I | **A** | I | I | I | I | I |
| Security sign-off | I | I | I | I | I | I | I | **A** | I |
| Deployment execution | C | I | C | I | I | **A** | I | I | I |
| Smoke tests & post-deploy verification | C | I | R | R | I | **A** | I | C | I |
| Release notes authoring | C | **A** | R | C | I | C | C | C | C |
| Stakeholder & customer announcement | R | R | I | I | I | I | I | I | **A** |
| Rollback decision | **A** | C | R | C | I | R | I | C | I |

---

### Retrospective Phase
> Reference: [Retrospective & Continuous Improvement](./octoacme-retrospective-and-continuous-improvement.md)

| Activity | Project Manager | Product Manager | Developer | QA Lead | UX/UI Designer | DevOps Engineer | Business Analyst | Security Champion | Customer Success Manager |
|----------|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| Retro facilitation | **A** | I | R | R | R | R | R | R | I |
| Retro action item ownership | **A** | C | R | R | R | R | R | R | I |
| Process improvement proposals | C | C | R | R | R | R | R | R | **A** (customer feedback) |
| Metrics review & outcome assessment | C | **A** | R | C | I | C | C | I | R |

---

## DRI Assignment Guidance

### Principles
1. **One A per activity.** If you find two people marked Accountable, resolve it before the project begins. Shared accountability means no accountability.
2. **The DRI decides, not the committee.** Consulted parties give input; the DRI makes the call.
3. **Accountable ≠ Does the work.** A Project Manager may be Accountable for risk register updates while a Business Analyst is Responsible for maintaining the content.

### Assigning DRIs for Key Decisions
| Decision Area | Default DRI | Notes |
|---------------|------------|-------|
| Scope changes | Product Manager | Must consult Project Manager for timeline impact |
| Go/no-go for release | Project Manager | Requires sign-off from QA Lead, DevOps Engineer, and Security Champion |
| Security risk acceptance | Security Champion | Escalates to PM if risk is High or above |
| Architectural/technical design | Lead Developer | Consults DevOps Engineer for infrastructure-impacting decisions |
| Budget/resource changes | Project Manager | Escalates to Sponsor as needed |
| Customer communication | Customer Success Manager | Coordinates content with Product Manager |

### Risk Ownership
- Every identified risk in the Risk Register must have a named **Owner** (equivalent to the A in RACI).
- Default risk ownership by type:
  - **Schedule / dependency risks** → Project Manager
  - **Scope / requirements risks** → Product Manager
  - **Technical / implementation risks** → Lead Developer
  - **Security risks** → Security Champion
  - **Quality risks** → QA Lead
  - **Infrastructure / deployment risks** → DevOps Engineer
  - **Customer / market risks** → Customer Success Manager

### Release Coordination
The release coordination group includes: **Project Manager (DRI), QA Lead, DevOps Engineer, Security Champion,** and **Product Manager**. All four non-Project-Manager roles must provide explicit sign-off before a production deployment proceeds. See the pre-release sign-off checklist in [Release & Deployment](./octoacme-release-and-deployment.md).

---

## How to Use This Document
- **At Initiation:** Populate the team composition section of the Project One-pager with role assignments. Reference this matrix to confirm all key activities have a named DRI.
- **At Planning:** Walk through the Planning Phase table during kickoff to ensure every role knows their accountabilities.
- **During Execution:** Use the Execution Phase table to resolve ownership disputes quickly.
- **At Release:** Use the Release Phase table to drive the pre-release sign-off checklist.
- **At Retrospective:** Review DRI assignments and update this matrix if roles or activities change.
