# OctoAcme — Risk Management & Communication

## Purpose
Explain how to identify, manage, and communicate risks and dependencies.

## Risk Register
Maintain a simple table with:
- ID
- Description
- Impact (High/Med/Low)
- Likelihood (High/Med/Low)
- Owner
- Mitigation plan
- Status

## Risk Lifecycle
- Identify: during planning and ongoing execution
- Assess: estimate impact and likelihood
- Mitigate: reduced via actions, contingency plans
- Monitor: review at weekly syncs and update status

## Stakeholder Communication
- Identify stakeholder groups and communication needs (e.g., engineering, sales, support)
- Provide regular updates (weekly or milestone-based)
- Use a single source of truth (project README or release doc) for status

## Communication Templates
Weekly Status Template:
- Progress this week:
- Next steps:
- Risks & blockers:
- Ask / decisions needed:

Incident Communication
- Triage summary
- Actions being taken
- Expected timeline
- Post-incident blameless retrospective scheduled

## Escalation Paths
- Team-level -> PM -> Product Lead -> Sponsor
- For security incidents, follow the security incident runbook and notify Security on-call

## Security Risk Escalation
Security risks require a clear ownership chain to ensure they are not lost in the general risk register:

1. **Identification:** Any team member can identify a security risk, but the **Security Champion** is the designated first receiver. Security risks found during development or code review should be raised directly with the Security Champion.
2. **Assessment:** The **Security Champion** assesses severity (Critical / High / Medium / Low) using the project's agreed classification (e.g., CVSS or internal rubric) and decides on the appropriate response:
   - **Critical / High:** immediately escalate to **Project Manager** and **Product Manager**. May require scope or timeline adjustment and should be added to the Risk Register with a named mitigation owner.
   - **Medium:** document in the Risk Register with mitigation plan; Security Champion tracks to resolution.
   - **Low / Informational:** document and monitor; address in a future sprint.
3. **Ownership:** The **Security Champion** is the Accountable owner for security risks in the Risk Register. The **Project Manager** is the Accountable owner for the overall Risk Register and schedule impact.
4. **Escalation beyond the project team:** If a security risk affects multiple teams, product lines, or involves a potential data breach, the Security Champion escalates to the organizational security team (or CISO) in addition to the Project Manager.
5. **Release gate:** No Critical or High unmitigated security risks may proceed to production without explicit acceptance documented by the Security Champion and Project Manager. See [Release & Deployment](./octoacme-release-and-deployment.md) for the pre-release sign-off checklist.

For full role descriptions, see [Roles & Personas](./octoacme-roles-and-personas.md). For role ownership of risk activities, see the [Roles & Responsibilities RACI](./octoacme-roles-and-responsibilities-raci.md).
