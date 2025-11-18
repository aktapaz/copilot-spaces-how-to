# OctoAcme Project Management Overview

## Purpose
Provide a concise, shareable introduction to how OctoAcme runs projects so new teammates can quickly understand our approach, roles, and key artifacts.

## Scope
Applies to all cross-functional projects that deliver product features, services, or integrations.

## Principles
- Customer-first: prioritize customer value and usability.
- Iterative delivery: deliver small, testable increments.
- Clear ownership: each project has a named Project Manager (PM) and Product Lead.
- Data-informed decisions: measure impact and iterate based on evidence.
- Psychological safety: encourage feedback and learning.

## Core Roles
- Project Manager (PM): coordinates delivery, schedules, risk, communications.
- Product Manager (PdM): defines outcomes, prioritizes backlog, and measures success.
- Developers: implement features, collaborate on design and testability.
- QA/Testing: validate quality and acceptance criteria.
- Stakeholders: provide inputs and approvals.

## Key Artifacts
Essential documents that support project transparency and execution:
- **Project Charter / One-pager**: Problem, goals, stakeholders, timeline (see [Project Initiation Guide](octoacme-project-initiation.md))
- **Roadmap and Release Plan**: Feature priorities and target milestones
- **Sprint/Iteration Backlog**: Prioritized work items with acceptance criteria
- **Acceptance Criteria & Definition of Done**: Quality standards for completion (see [Definition of Done Template](template-definition-of-done.md))
- **Risk Register**: Active risks, mitigation plans, and status tracking (see [Risk Register Template](template-risk-register.md))
- **Stakeholder Communication Plan**: Who to inform, when, and how (see [Stakeholder Communication Checklist](template-stakeholder-communication-checklist.md))
- **Retrospective notes and action items**: Lessons learned and improvement commitments

## Lifecycle (high-level)
1. Initiation: problem statement, stakeholders, high-level timeline.
2. Planning: scope, resources, milestones, dependencies.
3. Execution: build, test, review, iterate.
4. Release: deploy, verify, announce.
5. Close & Retrospective: capture learnings and next steps.

## Communication Cadence
Establish regular touchpoints to maintain alignment and transparency:
- **Daily standups** (15 min) — team-level progress, blockers, and coordination
- **Weekly PM + PdM sync** — alignment on priorities, risks, and stakeholder needs
- **Twice-weekly team syncs** (or as agreed) — deeper technical discussions and planning
- **Sprint/milestone reviews** — demo completed work and gather feedback
- **Monthly stakeholder updates** — progress summary, upcoming milestones, and key metrics
- **Ad-hoc escalations** as needed for urgent issues or decisions

**Best Practice**: Use consistent formats (see templates in [Risk Management & Communication](octoacme-risks-and-communication.md)) to make updates efficient and scannable.

## How to use these docs
- **Keep the Project Charter updated** in the project repo with current status and key decisions
- **Add process-specific docs** into `.copilot/` if you want Copilot Spaces to use them as context for project-specific assistance
- **Reference templates** from the docs/ directory for consistent practices across projects:
  - [Stakeholder Communication Checklist](template-stakeholder-communication-checklist.md)
  - [Risk Register Template](template-risk-register.md)
  - [Definition of Done Template](template-definition-of-done.md)
- **Adapt to your context**: These are guidelines, not rigid rules—tailor them to your project's size and complexity
- **Share learnings**: Update these docs with improvements discovered during retrospectives
