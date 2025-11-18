# OctoAcme — Risk Management & Communication

## Purpose
Explain how to identify, manage, and communicate risks and dependencies.

## Risk Register
Maintain a comprehensive risk register to track and manage project risks. For a detailed template and best practices, see **[Risk Register Template](template-risk-register.md)**.

At minimum, your risk register should include:
- ID
- Description
- Category (Technical, Dependency, Resource, Scope, Timeline, External, Quality, Communication)
- Impact (High/Med/Low)
- Likelihood (High/Med/Low)
- Priority (calculated from Impact × Likelihood)
- Owner
- Mitigation plan
- Status (Open, Monitoring, Resolved, Accepted)
- Last updated date

## Risk Lifecycle
- Identify: during planning and ongoing execution
- Assess: estimate impact and likelihood
- Mitigate: reduced via actions, contingency plans
- Monitor: review at weekly syncs and update status

## Stakeholder Communication
Effective stakeholder communication is critical to project success. For a comprehensive guide, see **[Stakeholder Communication Checklist](template-stakeholder-communication-checklist.md)**.

### Key Practices
- **Identify stakeholder groups** and their communication needs (e.g., engineering, sales, support, executives)
- **Provide regular updates** (weekly or milestone-based) using a consistent format
- **Use a single source of truth** (project README or release doc) for status
- **Be proactive**: Don't wait for stakeholders to ask—share updates consistently
- **Escalate early**: Alert stakeholders to high-impact risks within 24 hours
- **Maintain a stakeholder matrix** documenting contact info, preferences, and information needs

### Stakeholder Matrix Example
Create a table documenting key stakeholders:

| Stakeholder Group | Primary Contact | Communication Frequency | Preferred Channel | Key Information Needs |
|-------------------|----------------|------------------------|-------------------|----------------------|
| Executive Sponsor | [Name] | Bi-weekly | Email summary | ROI, timeline, major risks |
| Product Team | [Name] | Weekly | Slack + standup | Feature progress, dependencies |
| Engineering | [Name] | Daily | Standup + GitHub | Technical blockers, PRs |
| Support | [Name] | Pre/post-release | Email + training | New features, known issues |

## Communication Templates
### Weekly Status Template:
- **Progress this week**: [Key accomplishments and completed work items]
- **Next steps**: [Planned work for upcoming week]
- **Risks & blockers**: [Active risks with mitigation status, any blockers requiring attention]
- **Metrics**: [Relevant KPIs, velocity, or success metrics]
- **Ask / decisions needed**: [Specific questions or approvals needed from stakeholders]

### Incident Communication Template:
- **Summary**: [Brief description of the incident]
- **Impact**: [Affected systems, users, or business operations]
- **Status**: [Current state: investigating, mitigating, resolved]
- **Actions being taken**: [Immediate response and mitigation steps]
- **Expected timeline**: [When resolution is expected]
- **Next update**: [When next communication will be sent]
- **Post-incident follow-up**: [Retrospective scheduled, root cause analysis planned]

## Escalation Paths
- Team-level -> PM -> Product Lead -> Sponsor
- For security incidents, follow the security incident runbook and notify Security on-call
