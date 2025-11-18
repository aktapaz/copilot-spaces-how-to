# Risk Register Template

## Purpose
This template provides a comprehensive format for tracking, assessing, and managing project risks throughout the project lifecycle. Use this as a living document that is reviewed and updated regularly.

## How to Use This Template
1. Copy this template to your project repository
2. Update the Risk Summary section with each status update
3. Add new risks to the risk table as they are identified
4. Review and update risk status weekly during project syncs
5. Archive resolved risks to maintain focus on active concerns

---

## Risk Summary Dashboard

| Metric | Count |
|--------|-------|
| **Total Active Risks** | 0 |
| **Critical (High Impact × High Likelihood)** | 0 |
| **High Priority** | 0 |
| **Medium Priority** | 0 |
| **Low Priority** | 0 |
| **Risks Resolved This Week** | 0 |

**Last Updated**: [Date]

**Overall Risk Health**: 🟢 Green / 🟡 Yellow / 🔴 Red

---

## Active Risks

### Risk Table

| ID | Description | Category | Impact | Likelihood | Priority | Owner | Status | Mitigation Plan | Due Date | Last Updated |
|----|-------------|----------|--------|------------|----------|-------|--------|-----------------|----------|--------------|
| R-001 | Example: API dependency may not be ready on time | Dependency | High | Medium | High | PM Name | Open | Weekly syncs with API team; backup plan to mock API | 2025-02-01 | 2025-01-15 |
| | | | | | | | | | | |

### Risk Definitions

#### Impact Levels
- **High**: Would prevent release, cause customer outage, or require major rework
- **Medium**: Would delay release, degrade performance, or require significant effort to address
- **Low**: Minor inconvenience, easily worked around, or low customer visibility

#### Likelihood Levels
- **High**: >50% probability of occurring
- **Medium**: 20-50% probability of occurring  
- **Low**: <20% probability of occurring

#### Priority Calculation
| Impact / Likelihood | High | Medium | Low |
|---------------------|------|--------|-----|
| **High** | Critical | High | Medium |
| **Medium** | High | Medium | Low |
| **Low** | Medium | Low | Low |

#### Status Values
- **Open**: Risk identified, mitigation plan in progress
- **Monitoring**: Mitigation actions taken, watching for changes
- **Resolved**: Risk no longer applies or has been fully mitigated
- **Accepted**: Risk acknowledged but no mitigation planned (document rationale)

#### Risk Categories
- **Technical**: Technology, architecture, or implementation risks
- **Dependency**: Reliance on external teams, services, or vendors
- **Resource**: Staffing, skills, or availability constraints
- **Scope**: Requirements changes, feature creep, or unclear specifications
- **Timeline**: Schedule pressure, optimistic estimates, or competing priorities
- **External**: Market changes, regulatory issues, or customer factors
- **Quality**: Testing gaps, technical debt, or performance concerns
- **Communication**: Misalignment, lack of clarity, or stakeholder engagement

---

## Risk Details

### R-001: [Example Risk Title]

**Description**: Detailed explanation of the risk and potential impact on the project.

**Category**: Dependency

**Current Status**: Open

**Impact Assessment**: 
- Customer impact: [Describe]
- Timeline impact: [Describe]
- Resource impact: [Describe]

**Root Causes**:
- Cause 1
- Cause 2

**Mitigation Plan**:
1. Action item 1 (Owner: [Name], Due: [Date])
2. Action item 2 (Owner: [Name], Due: [Date])
3. Fallback plan if mitigation fails

**Monitoring Plan**:
- Check-in frequency: Weekly
- Success metrics: [How we'll know the risk is mitigated]
- Escalation trigger: [When to escalate]

**Status History**:
- 2025-01-15: Risk identified, mitigation plan created
- 2025-01-22: First mitigation action completed

---

## Risk Identification Questions

Use these questions during planning and weekly syncs to identify risks:

### Technical Risks
- Are there new technologies or tools the team hasn't used before?
- Do we have sufficient test coverage and quality gates?
- Are there performance or scalability concerns?
- Is technical debt likely to slow us down?

### Dependency Risks
- Do we depend on other teams or external services?
- Are those dependencies committed to our timeline?
- What happens if a dependency is delayed or unavailable?
- Do we have contingency plans or workarounds?

### Resource Risks
- Do we have the right skills on the team?
- Are key team members available for the full project duration?
- Are there competing priorities that could pull resources away?
- Do we need additional headcount or expertise?

### Scope Risks
- Are requirements well-defined and stable?
- Is there pressure to add features mid-project?
- Do stakeholders agree on priorities and trade-offs?
- Are acceptance criteria clear and testable?

### Timeline Risks
- Are estimates realistic and based on historical data?
- Is there buffer for unexpected issues?
- Are there external deadlines that can't be moved?
- Have we accounted for holidays, PTO, and team ceremonies?

### Communication Risks
- Are all stakeholders aligned on goals and expectations?
- Do we have clear escalation paths?
- Is project status visible and accessible?
- Are team members communicating blockers promptly?

---

## Risk Response Strategies

### Mitigate
Reduce the probability or impact of the risk through proactive actions.
- **Example**: Add extra testing time to reduce quality risk

### Transfer
Shift the risk to another party (e.g., vendor, insurance, different team).
- **Example**: Use a managed service instead of building in-house

### Avoid
Change the project plan to eliminate the risk entirely.
- **Example**: Remove a risky feature from scope

### Accept
Acknowledge the risk and proceed without specific mitigation, but have a response plan ready.
- **Example**: Accept risk of minor UI inconsistencies across browsers

---

## Escalation Criteria

Escalate risks when:
- Priority is Critical and status is Open for >1 week
- Multiple mitigation attempts have failed
- Risk is blocking other work or teams
- Impact severity has increased significantly
- Decision authority is needed from sponsor/stakeholder

**Escalation Path**: Team → PM → Product Lead → Executive Sponsor

---

## Resolved Risks Archive

| ID | Description | Resolution Date | Resolution Summary |
|----|-------------|-----------------|-------------------|
| R-999 | Example resolved risk | 2025-01-10 | API team confirmed delivery; dependency resolved |

---

## Risk Review Schedule

- **Daily**: Check for new blockers in standup
- **Weekly**: Review risk register in team sync, update status
- **Sprint/Milestone**: Deep dive on all active risks, identify new risks
- **Monthly**: Review trends and patterns with stakeholders

---

## Example Scenarios

### Scenario 1: Critical Dependency Risk

**Situation**: Your project depends on another team's API that has a history of delays.

**Risk Entry**:
- **ID**: R-002
- **Description**: Backend API may not be ready for integration testing by target date
- **Category**: Dependency
- **Impact**: High (blocks feature completion)
- **Likelihood**: Medium (team has 60% on-time delivery rate)
- **Priority**: High
- **Mitigation**: 
  1. Weekly check-ins with API team
  2. Create mock API for parallel development
  3. Identify alternative integration points
  4. Plan timeline buffer of 1 week

### Scenario 2: Resource Risk

**Situation**: Lead developer is taking 2 weeks PTO during critical implementation phase.

**Risk Entry**:
- **ID**: R-003
- **Description**: Key developer unavailable during core feature development
- **Category**: Resource
- **Impact**: Medium (could delay feature)
- **Likelihood**: High (PTO confirmed)
- **Priority**: High
- **Mitigation**:
  1. Front-load critical architecture decisions before PTO
  2. Cross-train another developer on the feature area
  3. Adjust sprint planning to schedule complex work before/after PTO
  4. Ensure comprehensive documentation is available

---

## Related Resources
- [Risk Management & Communication](octoacme-risks-and-communication.md)
- [Project Planning](octoacme-project-planning.md)
- [Stakeholder Communication Checklist](template-stakeholder-communication-checklist.md)

---

**Remember**: Risk management is ongoing. A risk register is only valuable if it's kept current and used to drive decisions.
