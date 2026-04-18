# OctoAcme Project Management Docs

## Overview

This folder contains OctoAcme's lightweight, cross-functional project management process documentation. The docs serve as a shared source of truth for how we initiate, plan, execute, release, and continuously improve delivery work across all product and engineering teams. If you are new to the process, start with the [Project Management Overview](./octoacme-project-management-overview.md), then follow the lifecycle docs in order.

OctoAcme's project management approach is built on a set of core principles: customer-first prioritization, iterative delivery of small and testable increments, clear ownership with named Project Managers and Product Leads, data-informed decision-making, and a culture of psychological safety. Projects move through a five-stage lifecycle—Initiation, Planning, Execution & Tracking, Release & Deployment, and Retrospective & Continuous Improvement—with defined artifacts, ceremonies, and decision gates at each stage.

Clear roles and consistent communication are central to how OctoAcme runs projects. The **Project Manager (PM)** coordinates delivery rhythm, schedules, risks, dependencies, and communications. The **Product Manager (PdM)** defines outcomes, prioritizes the backlog, and measures success. **Developers** implement features with testability and maintainability in mind, while **QA/Testing** validates quality and acceptance criteria. Stakeholders contribute inputs and approvals, and escalation paths are explicit—moving from team triage to PM and Product Lead, then to sponsor-level escalation for business-impacting blockers when needed. See [Roles & Personas](./octoacme-roles-and-personas.md) and [Risk Management & Communication](./octoacme-risks-and-communication.md) for full details.

Quality assurance is built into both the development workflow and the release process. OctoAcme prefers **small pull requests**, requires linking PRs to issues and acceptance criteria, and expects CI checks (tests, linting, and security scanning) before review—requiring at least one approval prior to merge. Testing spans unit tests for new logic, integration tests where appropriate, and end-to-end smoke testing for critical flows, with manual QA used for feature acceptance. For releases, teams follow a standardized deployment checklist through staging verification, production rollout, post-deploy checks, and stakeholder announcements—backed by a rollback/incident playbook and blameless retrospectives that convert learnings into owned, time-bound action items.

---

## Lifecycle Summary

| Stage | Description | Doc |
|-------|-------------|-----|
| **Initiation** | Validate the business need, align stakeholders, produce a Project One-pager, and decide go/no-go before planning begins. | [Project Initiation Guide](./octoacme-project-initiation.md) |
| **Planning** | Turn the approved initiative into an actionable plan: kickoff, prioritized backlog with acceptance criteria, estimation, Definition of Done, dependencies, and a milestone/release map. | [Project Planning](./octoacme-project-planning.md) |
| **Execution & Tracking** | Run the day-to-day delivery cadence (standups, weekly syncs, demos), manage work on a project board, and follow PR and QA workflows. Blockers escalate from team → PM → Product Lead → Sponsor. | [Execution & Tracking](./octoacme-execution-and-tracking.md) |
| **Release & Deployment** | Meet pre-release requirements, follow the deployment checklist, verify in staging and production, communicate the release, and be prepared with rollback/incident steps and release notes. | [Release & Deployment Guide](./octoacme-release-and-deployment.md) |
| **Retrospective & Continuous Improvement** | After sprints, releases, milestones, and incidents, capture learnings and define a small number of owned, time-bound action items tracked to completion. | [Retrospective & Continuous Improvement](./octoacme-retrospective-and-continuous-improvement.md) |

---

## Full Index of Docs in This Folder

- [Project Management Overview](./octoacme-project-management-overview.md)
- [Project Initiation Guide](./octoacme-project-initiation.md)
- [Project Planning](./octoacme-project-planning.md)
- [Execution & Tracking](./octoacme-execution-and-tracking.md)
- [Risk Management & Communication](./octoacme-risks-and-communication.md)
- [Release & Deployment Guide](./octoacme-release-and-deployment.md)
- [Retrospective & Continuous Improvement](./octoacme-retrospective-and-continuous-improvement.md)
- [Roles & Personas](./octoacme-roles-and-personas.md)
