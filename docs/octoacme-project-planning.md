# OctoAcme — Project Planning

## Purpose
Turn an approved initiative into an actionable plan and backlog for delivery.

## Objectives
- Break work into shippable increments
- Identify dependencies and risks
- Align timelines, releases, and responsibilities

## Activities
1. Kickoff meeting with stakeholders and delivery team
2. Create prioritized backlog with acceptance criteria
3. Estimate scope (T-shirt sizing or story points)
4. Define Definition of Done (DoD)
5. Identify dependencies and integration points
6. Create release plan and milestone map

## Backlog Refinement & Acceptance Criteria
- **Business Analyst** leads requirements documentation and works with **Product Manager** to decompose epics into stories.
- **QA Lead** reviews acceptance criteria for testability and adds test-specific conditions.
- **UX/UI Designer** provides design acceptance criteria for user-facing features (e.g., design spec link, accessibility requirements).
- **Security Champion** flags stories with security implications and adds security acceptance criteria as needed.
- Each backlog item should have clear, unambiguous acceptance criteria before entering a sprint. See the Backlog Item Template below.

## Test Plan & QA Approach
- The **QA Lead** owns the test strategy document and coordinates with Developers on automated test coverage.
- At a minimum, define: unit test targets, integration test scope, end-to-end smoke test scenarios, and manual UAT steps.
- Include a defect triage process: severity classification, escalation path (QA Lead → PM), and SLA for critical bugs.
- Test plan should be updated in the project repo under `docs/` or linked from the Project One-pager.

## Security Review
- The **Security Champion** participates in planning to identify security-sensitive features and define threat models.
- Security requirements are added to relevant backlog items as acceptance criteria.
- Agree on the security review checkpoint cadence (e.g., per sprint, per milestone, or pre-release only) during planning.
- Reference the [Risk Management & Communication](./octoacme-risks-and-communication.md) doc for security risk escalation paths.

## Backlog Item Template
- Title:
- Description:
- Acceptance criteria:
- Priority:
- Estimate:
- Owner:
- Related docs/links:

## Sprint / Iteration Planning
- Timebox planning to agreed sprint length
- Pull items that meet DoD and have clear acceptance criteria
- Ensure team capacity is respected

## Risk & Dependency Management
- Capture in Risk Register:
  - ID, Description, Impact, Probability, Owner, Mitigation
- Mark cross-team dependencies in the project board and escalate during weekly syncs

## Planning Checklist
- [ ] Project kickoff held
- [ ] Backlog prioritized and estimated
- [ ] Release timeline and milestones agreed
- [ ] Definition of Done documented
- [ ] Initial test plan / QA approach drafted (owned by QA Lead)
- [ ] Security requirements and threat model reviewed (owned by Security Champion)
- [ ] UX/design artifacts available for user-facing stories
- [ ] CI/CD environment confirmed ready (owned by DevOps Engineer)
- [ ] Role DRIs assigned — see [RACI](./octoacme-roles-and-responsibilities-raci.md)
