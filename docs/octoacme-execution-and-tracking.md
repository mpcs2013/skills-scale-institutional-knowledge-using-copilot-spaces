# OctoAcme — Execution & Tracking

## Purpose
Guidance for managing day-to-day execution and tracking progress toward project milestones.

## Team Rhythm
- Daily standups (15 min) — focus on progress, blockers, dependencies
- Weekly delivery sync — show progress, updates, and flagged risks
- Demo/Review at the end of each sprint or milestone

## Workflows
- Use the project board (e.g., GitHub Projects) with columns: Backlog, Ready, In Progress, In Review, QA, Done
- Pull Request workflow:
  - Small PRs (<= 400 lines when possible)
  - Include issue link and acceptance criteria in PR description
  - Run automated tests and linting in CI before requesting review
  - Require at least one approval before merging (or team-defined policy)

## Board Handoff Policy
Clear handoff criteria prevent work from stalling between columns. The following minimum criteria apply:

| Transition | Criteria | Responsible |
|-----------|----------|-------------|
| In Progress → In Review | PR opened, CI passing, self-review complete | Developer |
| In Review → QA | PR approved by at least one reviewer, merged to integration branch | Reviewer / Developer |
| QA → Done | All acceptance criteria validated (including security criteria), QA Lead sign-off | QA Lead |
| QA → In Progress (re-open) | QA Lead documents defect with severity; critical/high bugs block Done | QA Lead |

- **QA Lead responsibilities on the board:** owns the QA column; triages new items entering QA within one business day; maintains a defect log linked from the project board; communicates test status in daily standups.

## Quality & Testing
- Unit tests for new logic
- Integration tests where applicable
- End-to-end smoke tests for critical flows before release
- Security scanning in CI
- Manual QA for feature acceptance when needed

## Reporting & Metrics
- Track velocity and burndown
- Monitor success metrics identified in the Project One-pager
- Use dashboards for key signals (errors, latency, usage)

## Blocker Escalation
- Level 1: Team-level triage in daily standup
- Level 2: PM escalates to Product Lead and dependent teams
- Level 3: Sponsor-level escalation for business-impacting issues

## Execution Checklist
- [ ] Branching and PR conventions documented in repo
- [ ] CI configured for tests and lint
- [ ] Regular demos scheduled
- [ ] Risk register updated weekly
- [ ] QA Lead managing QA column and defect log
- [ ] Board handoff criteria communicated to team (see Board Handoff Policy above)

For role ownership of execution activities, see the [Roles & Responsibilities RACI](./octoacme-roles-and-responsibilities-raci.md).
