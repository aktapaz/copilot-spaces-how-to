# OctoAcme — Release & Deployment Guide

## Purpose
Standardize how OctoAcme releases features to production to reduce risk and improve observability.

## Release Types
- Patch: hotfixes addressing critical production issues
- Minor: incremental features and improvements
- Major: significant functionality or breaking changes

## Pre-release requirements
Ensure quality and readiness before deploying to production:
- [ ] All acceptance criteria met and PRs merged
- [ ] All items meet the **[Definition of Done](template-definition-of-done.md)**
- [ ] Passing CI and security scans (0 high-severity vulnerabilities)
- [ ] Release notes drafted and reviewed by stakeholders
- [ ] Rollback / mitigation plan documented and tested
- [ ] Smoke tests prepared and validated in staging
- [ ] Performance testing completed (if applicable)
- [ ] Database migrations tested and reversible (if applicable)
- [ ] Support and customer-facing teams trained on new features
- [ ] Monitoring and alerting configured for new functionality

## Deployment Checklist
- [ ] Deployment window scheduled (if needed) and communicated to stakeholders
- [ ] Backup or snapshot created (if applicable)
- [ ] Deploy to staging environment successfully
- [ ] Run smoke tests on staging (all critical paths verified)
- [ ] Deploy to production (automated pipeline preferred)
- [ ] Run post-deploy verifications and smoke tests on production
- [ ] Monitor error rates, latency, and key metrics for 30+ minutes
- [ ] Announce release to stakeholders, support, and end users
- [ ] Update status page or changelog (if public-facing)

### Example: Smoke Test Checklist for Dashboard Release
- [ ] User can log in successfully
- [ ] Dashboard loads within 3 seconds
- [ ] Real-time data updates every 5 seconds
- [ ] Charts render correctly on desktop and mobile
- [ ] Export to CSV functionality works
- [ ] API error handling displays appropriate messages
- [ ] No console errors or warnings in browser

## Rollback & Incident Playbook
If a deployment fails or causes a critical issue:
- **Assess impact**: Is it affecting users? What's the severity?
- **Trigger incident response**: Page on-call engineer if P0/P1
- **Notify stakeholders**: Alert PM, Product Lead, and relevant teams within 15 minutes
- **Decision**: Rollback or fix-forward?
  - Rollback if: Issue is widespread, fix is not immediately available, or user impact is severe
  - Fix-forward if: Issue is isolated, fix is ready and tested, or rollback would cause data loss
- **Execute rollback** to last known-good release if necessary (use automated process)
- **Verify rollback**: Confirm issue is resolved and system is stable
- **Triage root cause**: Assemble team for incident analysis
- **Capture action items**: Document learnings and preventive measures
- **Post-incident retrospective**: Schedule blameless retro within 48 hours

### Example Incident Timeline
**2025-02-01 14:00**: Dashboard v2 deployed to production
**2025-02-01 14:15**: Monitoring alerts: API error rate increased to 15%
**2025-02-01 14:18**: On-call paged, stakeholders notified
**2025-02-01 14:22**: Decision made to rollback (root cause unclear, user impact high)
**2025-02-01 14:30**: Rollback completed, error rate returned to 0.2%
**2025-02-01 14:45**: Post-mortem investigation begins
**2025-02-01 17:00**: Root cause identified: database connection pool exhaustion
**2025-02-02 10:00**: Fix implemented and tested, redeployment successful
**2025-02-03 14:00**: Blameless retrospective held, action items created

## Release Notes Template
- **Release name / number**: [e.g., Dashboard v2.0 or Release 2025.02.01]
- **Date**: [Deployment date]
- **Summary**: [Brief overview of release purpose and key highlights]
- **Notable changes**:
  - **New features**: [User-facing feature descriptions]
  - **Improvements**: [Enhancements to existing functionality]
  - **Bug fixes**: [Resolved issues]
  - **Performance**: [Speed or efficiency improvements]
- **Breaking changes**: [API changes, deprecations, or incompatibilities]
- **Migration steps** (if any): [Steps users or operators must take]
- **Known issues**: [Any limitations or bugs still being addressed]
- **Documentation**: [Links to updated docs, tutorials, or guides]

### Example Release Notes

**Release: Dashboard v2.0**
**Date**: February 1, 2025

**Summary**: 
Redesigned customer dashboard with real-time data updates, improved performance, and modern UX.

**Notable Changes**:
- ✨ **New**: Real-time data updates every 5 seconds (no page refresh needed)
- ✨ **New**: Export dashboard data to CSV
- 🚀 **Improvement**: Dashboard load time reduced from 8s to 2s
- 🐛 **Fix**: Resolved timezone display issues for international customers
- 🐛 **Fix**: Charts now render correctly on mobile devices

**Breaking Changes**: None

**Migration Steps**: No action required. All users will automatically see the new dashboard on next login.

**Known Issues**:
- Export to PDF is not yet available (planned for v2.1)
- Safari users may experience minor chart rendering delays

**Documentation**: [Dashboard User Guide](https://docs.example.com/dashboard-v2)
