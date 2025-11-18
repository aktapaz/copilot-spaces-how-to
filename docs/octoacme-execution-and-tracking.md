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

## Quality & Testing
Quality is built in throughout execution, not just at the end. Reference the **[Definition of Done Template](template-definition-of-done.md)** for comprehensive quality standards.

### Testing Standards
- **Unit tests** for new logic (target: >80% code coverage)
- **Integration tests** where components interact
- **End-to-end smoke tests** for critical user flows before release
- **Security scanning** in CI (no high-severity vulnerabilities)
- **Performance testing** for features with scale requirements
- **Manual QA** for feature acceptance when needed, especially for UI changes

### Code Review Standards
- Small PRs (<= 400 lines when possible) for easier review
- Include issue link and acceptance criteria in PR description
- Run automated tests and linting in CI before requesting review
- Require at least one approval before merging (or team-defined policy)
- Address all review comments or discuss rationale

### Example: PR Description Template
```markdown
## What
Brief description of the change

## Why
Link to issue or explanation of need

## How
Technical approach taken

## Testing
- Unit tests: ✅ Added for new functions
- Integration tests: ✅ Updated for API changes
- Manual testing: ✅ Verified in Chrome, Firefox, Safari

## Screenshots (if UI change)
[Include before/after screenshots]

## Acceptance Criteria
- [x] Criterion 1
- [x] Criterion 2
- [x] Criterion 3
```

## Reporting & Metrics
Track quantitative data to inform decisions and demonstrate progress.

### Key Metrics to Monitor
- **Velocity**: Story points or tickets completed per sprint
- **Burndown**: Work remaining vs. time, updated daily
- **Success metrics**: KPIs identified in the Project One-pager (e.g., adoption rate, latency, error rate)
- **Quality metrics**: Test coverage, defect rates, security vulnerabilities
- **Health metrics**: Team morale, blockers resolved, dependencies on track

### Dashboard Best Practices
- Use visual dashboards for key signals (errors, latency, usage)
- Update metrics daily or weekly depending on project phase
- Share dashboard access with all stakeholders
- Review trends, not just point-in-time values

### Example: Sprint Metrics Report
```
Sprint 5 Summary (Jan 15 - Jan 29, 2025)

Velocity: 34 points (target: 30-35)
Burndown: On track, 2 points remaining
Success Metrics:
  - API latency: p95 < 200ms ✅
  - Error rate: 0.2% (target: <0.5%) ✅
  - Test coverage: 87% (+2% from last sprint) ✅

Quality:
  - PRs merged: 12
  - Average PR size: 285 lines
  - Security scan: 0 high-severity issues ✅

Risks:
  - Dependency on Team X API (Medium priority, mitigation in progress)
```

## Blocker Escalation
- Level 1: Team-level triage in daily standup
- Level 2: PM escalates to Product Lead and dependent teams
- Level 3: Sponsor-level escalation for business-impacting issues

## Execution Checklist
- [ ] Branching and PR conventions documented in repo
- [ ] CI configured for tests and lint
- [ ] Regular demos scheduled
- [ ] Risk register updated weekly
- [ ] Definition of Done established and enforced

---

## Example Scenario: Mid-Sprint Blocker

**Situation**: On day 3 of a 2-week sprint, the team discovers that a critical API they depend on has changed unexpectedly, breaking their integration.

**Response**:
1. **Immediate** (Same day):
   - Developer raises blocker in standup
   - PM creates risk entry (R-005: API breaking change)
   - PM reaches out to API team for clarification and timeline
   
2. **Within 24 hours**:
   - Team identifies workaround: use cached data temporarily
   - Developer implements workaround with feature flag
   - PM updates stakeholders on risk and mitigation plan
   
3. **Within 48 hours**:
   - API team confirms fix timeline: 3 days
   - PM adjusts sprint plan: deprioritize less critical features
   - Workaround tested and deployed to unblock progress
   
4. **After resolution**:
   - API fix deployed, integration verified
   - Workaround code removed or kept as fallback (team decision)
   - Risk marked as "Resolved" in register
   - Retrospective includes discussion on improving dependency monitoring

**Key Takeaways**:
- Early escalation prevented bigger delays
- Workaround maintained momentum
- Transparent communication kept stakeholders informed
- Process improvements identified for future prevention
