# OctoAcme — Release & Deployment Guide

## Purpose
Standardize how OctoAcme releases features to production to reduce risk and improve observability.

## Release Types
- Patch: hotfixes addressing critical production issues
- Minor: incremental features and improvements
- Major: significant functionality or breaking changes

## Pre-release requirements
- All acceptance criteria met and PRs merged
- Passing CI and security scans
- Release notes drafted
- Rollback / mitigation plan documented
- Smoke tests prepared

## Release Coordination
The **Project Manager** is the DRI for release coordination. The following roles must provide explicit sign-off before a production deployment proceeds:

| Sign-off Owner | Area |
|----------------|------|
| **QA Lead** | All acceptance criteria validated; no open critical/high defects |
| **DevOps Engineer** | Deployment pipeline ready; environment confirmed; rollback procedure tested |
| **Security Champion** | Security scan results reviewed; no unacceptable open vulnerabilities |
| **Product Manager** | Feature scope confirmed; release notes reviewed and approved |

The Project Manager collects sign-offs and documents them in the release record or project board before giving the go-ahead for deployment.

## Pre-Release Sign-Off Checklist
- [ ] QA Lead: all acceptance criteria validated and sign-off recorded
- [ ] QA Lead: no open critical or high severity defects
- [ ] DevOps Engineer: staging deployment successful and smoke tests passing
- [ ] DevOps Engineer: rollback procedure documented and tested
- [ ] Security Champion: security scans reviewed; findings triaged and accepted or remediated
- [ ] Product Manager: release notes reviewed and approved
- [ ] Product Manager: feature scope confirmed (no unmerged scope)
- [ ] Customer Success Manager: customer-facing communication prepared (if applicable)
- [ ] Project Manager: all sign-offs collected; deployment window confirmed

## Deployment Checklist
- [ ] Deployment window scheduled (if needed)
- [ ] Backup or snapshot (if applicable)
- [ ] Deploy to staging and run smoke tests
- [ ] Deploy to production (automated pipeline preferred)
- [ ] Run post-deploy verifications
- [ ] Announce release to stakeholders and support

For role ownership of release activities, see the [Roles & Responsibilities RACI](./octoacme-roles-and-responsibilities-raci.md).

## Rollback & Incident Playbook
- If a deployment fails or causes a critical issue:
  - Trigger incident response and notify on-call
  - Rollback to last known-good release if necessary
  - Triage root cause and capture action items

## Release Notes Template
- Release name / number:
- Date:
- Summary:
- Notable changes:
- Migration steps (if any):
- Known issues:
