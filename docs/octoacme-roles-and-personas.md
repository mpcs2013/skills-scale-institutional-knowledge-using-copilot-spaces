# OctoAcme Personas

This document defines typical roles and responsibilities used in OctoAcme project docs and exercises.

For a mapping of these roles to key project activities, see [Roles & Responsibilities RACI](./octoacme-roles-and-responsibilities-raci.md).

---

## Developers

### Role Summary
Developers design, build, test, and deliver software components. They collaborate with product and project leads to implement features that meet acceptance criteria and quality standards.

### Responsibilities
- Implement features and fixes to meet acceptance criteria
- Write and maintain tests and documentation
- Participate in design and code reviews
- Assist in estimating and planning work
- Help identify technical risks and propose mitigations

### Goals
- Deliver reliable, maintainable code
- Reduce cycle time from idea to production
- Maintain high test coverage and observability

### Typical Communication
- Daily standups and sprint planning
- PR descriptions and code review comments
- Technical design docs when needed

---

## Product Managers

### Role Summary
Product Managers define what should be built to deliver customer and business value. They own the product vision, prioritize the backlog, and measure outcomes.

### Responsibilities
- Define problem statements and success metrics
- Prioritize the roadmap and backlog
- Collaborate with stakeholders and engineering on trade-offs
- Validate solutions through user research and metrics

### Goals
- Maximize customer value and impact
- Make clear, data-driven prioritization decisions
- Ensure product-market fit and usability

### Typical Communication
- Weekly alignment with PM and engineering leads
- Roadmap updates and stakeholder briefings
- Acceptance criteria and feature specs

---

## Project Managers

### Role Summary
Project Managers coordinate delivery activities, manage schedules, risks, and communications. They enable the team to deliver on commitments efficiently.

### Responsibilities
- Create and maintain project plans and timelines
- Manage risks, dependencies, and resource constraints
- Facilitate meetings (kickoff, planning, retrospectives)
- Ensure consistent project documentation and status reporting
- Coordinate cross-team and stakeholder communication

### Goals
- Deliver projects on time and within scope
- Minimize unplanned work and escalations
- Maintain transparency and alignment across stakeholders

### Typical Communication
- Weekly status updates and stakeholder reports
- Risk registers and decision logs
- Coordination via project boards and meeting facilitation

---

## Quality Assurance Lead

### Role Summary
The QA Lead owns the quality strategy across the project lifecycle. They define test plans, coordinate testing activities, and act as the final quality gate before releases reach production.

### Responsibilities
- Define and maintain the test strategy, test plans, and acceptance test suites
- Coordinate manual and automated testing activities across sprints
- Triage and prioritize defects in collaboration with Developers and Product Managers
- Own the QA column on the project board and enforce the Definition of Done
- Participate in sprint planning to estimate testing effort and flag risks early
- Sign off on release readiness from a quality perspective

### Goals
- Prevent regressions and ensure acceptance criteria are fully validated
- Reduce defect escape rate to production
- Build a sustainable, automated test coverage baseline

### Typical Communication
- Daily standups to surface test blockers
- Sprint planning and backlog refinement to clarify acceptance criteria
- Pre-release sign-off with PM, DevOps Engineer, and Security Champion
- Defect triage sessions with Developers

### Interaction with Existing Roles
- **Product Managers**: aligns on acceptance criteria and definition of done; escalates ambiguous requirements before they enter development.
- **Project Managers**: reports test progress and defect status in weekly syncs; flags scope or timeline risks from a QA perspective.
- **Developers**: collaborates on testability of implementations; reviews PRs for test coverage; pairs on complex edge cases.
- Appears in [Execution & Tracking](./octoacme-execution-and-tracking.md) (board workflow, QA column handoffs) and [Release & Deployment](./octoacme-release-and-deployment.md) (pre-release sign-off).

---

## UX/UI Designer

### Role Summary
The UX/UI Designer creates user experiences and interfaces that align with product goals and customer needs. They bridge the gap between business requirements and what users actually interact with.

### Responsibilities
- Conduct user research and translate insights into design artifacts (wireframes, prototypes, design specs)
- Maintain a shared design system and component library
- Collaborate with Product Managers to translate requirements into user flows
- Facilitate usability tests and incorporate feedback into iterative designs
- Provide design handoff artifacts (Figma files, redlines, interaction notes) to Developers

### Goals
- Deliver intuitive, accessible, and consistent user experiences
- Reduce design rework by catching usability issues early
- Ensure designs are technically feasible and align with engineering constraints

### Typical Communication
- Design reviews with Product Managers and Developers during planning and execution
- Async design feedback via shared design tools and PR comments
- Usability test readouts with Product Managers and stakeholders

### Interaction with Existing Roles
- **Product Managers**: partners closely to translate problem statements and user needs into design solutions; participates in roadmap discussions to flag UX risks.
- **Project Managers**: communicates design milestone status and flags dependencies (e.g., design must precede development of a feature).
- **Developers**: provides detailed handoff specs; reviews implemented UI against design intent; unblocks implementation questions quickly.
- Appears in [Project Planning](./octoacme-project-planning.md) (backlog refinement, acceptance criteria that include UX acceptance).

---

## DevOps Engineer

### Role Summary
The DevOps Engineer owns the CI/CD pipelines, infrastructure automation, deployment processes, and production observability. They enable the team to ship reliably and safely.

### Responsibilities
- Design and maintain CI/CD pipelines (build, test, security scan, deploy)
- Manage infrastructure-as-code and environment configurations (staging, production)
- Coordinate deployment windows and rollback procedures with Project Managers
- Monitor production systems and set up alerting for key signals
- Enforce and automate security and compliance controls in the pipeline

### Goals
- Reduce deployment risk through automation and consistent processes
- Keep lead time to production short while maintaining reliability
- Ensure observability and rapid incident response

### Typical Communication
- Release planning sync with PM, QA Lead, and Security Champion
- Deployment status updates and post-deploy verifications
- Incident response coordination and post-mortems

### Interaction with Existing Roles
- **Product Managers**: provides technical feasibility input on release timelines; flags infrastructure dependencies.
- **Project Managers**: coordinates deployment windows and confirms environment readiness in release planning.
- **Developers**: maintains CI standards Developers work within; reviews infrastructure-impacting PRs; pairs on observability and environment issues.
- Appears in [Release & Deployment](./octoacme-release-and-deployment.md) (deployment coordination and sign-off).

---

## Business Analyst

### Role Summary
The Business Analyst bridges business stakeholders and the delivery team by analyzing needs, documenting requirements, and ensuring solutions deliver intended business value.

### Responsibilities
- Elicit and document business requirements, user stories, and acceptance criteria
- Facilitate backlog refinement sessions to clarify scope and resolve ambiguity
- Create process flow diagrams, data models, and business rules documentation
- Validate delivered features against business requirements during UAT
- Support change management and stakeholder communication

### Goals
- Ensure solutions address real business needs with clear, unambiguous requirements
- Reduce rework caused by misunderstood requirements
- Bridge communication gaps between technical and non-technical stakeholders

### Typical Communication
- Backlog refinement sessions with Product Managers and Developers
- Requirements walkthroughs and UAT coordination with stakeholders
- Written requirement specs and acceptance criteria updates in the project board

### Interaction with Existing Roles
- **Product Managers**: partners to decompose high-level product goals into detailed requirements; contributes to roadmap prioritization based on business impact analysis.
- **Project Managers**: provides requirements status and flags scope changes that affect timeline or capacity.
- **Developers**: clarifies acceptance criteria during sprint planning and daily development; conducts UAT sign-off with stakeholders.
- Appears in [Project Planning](./octoacme-project-planning.md) (backlog refinement, acceptance criteria definition).

---

## Security Champion

### Role Summary
The Security Champion embeds security best practices into the development lifecycle. They advocate for secure design, conduct security reviews, and own the escalation path for security risks.

### Responsibilities
- Review features and architectural decisions for security vulnerabilities and risks
- Define and maintain security requirements and threat models for the project
- Ensure security scanning is configured and actionable in CI/CD
- Serve as the first point of contact for security questions from Developers
- Escalate significant security risks to the Project Manager and Product Manager
- Coordinate with external security reviews or penetration testing if required

### Goals
- Prevent security vulnerabilities from reaching production
- Build a security-aware engineering culture
- Ensure compliance with applicable security policies and standards

### Typical Communication
- Security review checkpoints during planning and pre-release
- Async feedback on PRs and architecture docs with security implications
- Risk escalation to PM when a security issue affects scope, timeline, or compliance

### Interaction with Existing Roles
- **Product Managers**: advises on security trade-offs in feature prioritization; communicates compliance requirements that constrain product decisions.
- **Project Managers**: escalates security risks that require schedule or scope adjustments; contributes security sign-off in release gate.
- **Developers**: provides actionable security guidance during implementation; reviews security-sensitive code changes; unblocks security tool integration questions.
- Appears in [Risk Management & Communication](./octoacme-risks-and-communication.md) (security risk escalation path) and [Release & Deployment](./octoacme-release-and-deployment.md) (pre-release sign-off).

---

## Customer Success Manager

### Role Summary
The Customer Success Manager (CSM) represents the voice of the customer within the project team. They gather end-user feedback, communicate release impact to customers, and monitor post-release satisfaction.

### Responsibilities
- Collect, synthesize, and prioritize customer feedback and feature requests
- Coordinate customer communications around upcoming releases or changes
- Monitor customer health metrics and satisfaction signals post-release
- Participate in retrospectives to surface customer impact of delivery decisions
- Act as the customer advocate in backlog prioritization discussions

### Goals
- Ensure customers derive value from each release
- Reduce customer-reported issues through proactive communication and early feedback loops
- Build long-term customer trust and satisfaction

### Typical Communication
- Regular customer feedback summaries shared with Product Managers
- Release communication drafts coordinated with Project Managers and Marketing
- Post-release check-ins with customers and reporting back to the team

### Interaction with Existing Roles
- **Product Managers**: primary feedback-loop partner; brings customer insights to roadmap and prioritization discussions; validates that shipped features meet customer expectations.
- **Project Managers**: coordinates rollout communication timelines; flags customer-impacting risks or change management needs.
- **Developers**: occasionally provides direct customer context for complex bugs or usability issues; reviews release notes for customer-facing clarity.
- Appears in [Release & Deployment](./octoacme-release-and-deployment.md) (stakeholder and customer announcements).

---

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.
- For a full mapping of roles to project activities, see the [Roles & Responsibilities RACI](./octoacme-roles-and-responsibilities-raci.md).

