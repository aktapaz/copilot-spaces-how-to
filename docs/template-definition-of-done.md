# Definition of Done (DoD) Template

## Purpose
The Definition of Done establishes shared quality standards that must be met before work is considered complete. This ensures consistency, reduces rework, and maintains high-quality deliverables across the team.

## How to Use This Template
1. Customize this template for your project during planning
2. Review and agree on DoD criteria with the entire team
3. Reference this checklist for every work item, PR, and release
4. Update the DoD as your project evolves and you learn what quality means for your context
5. Use as a gate for moving work to "Done" status on your project board

---

## Core DoD Principles

- **Completeness**: All acceptance criteria are met
- **Quality**: Code meets standards and is maintainable
- **Testability**: Changes are verified and won't break existing functionality
- **Deployability**: Work is ready to ship to production
- **Documentation**: Future maintainers can understand the change

---

## DoD Checklist for Individual Work Items

### Requirements & Design
- [ ] All acceptance criteria from the issue/story are met
- [ ] Feature behaves as designed across supported environments
- [ ] Edge cases and error conditions are handled appropriately
- [ ] User experience is intuitive and consistent with design guidelines
- [ ] Accessibility requirements are met (WCAG 2.1 Level AA for web features)

### Code Quality
- [ ] Code follows established style guide and conventions
- [ ] Code is readable, maintainable, and well-structured
- [ ] No unnecessary complexity; YAGNI principle applied
- [ ] No hardcoded values; configuration uses appropriate config files or environment variables
- [ ] Security best practices followed (input validation, authentication, authorization)
- [ ] No secrets, API keys, or sensitive data committed to repository

### Testing
- [ ] Unit tests written for new logic (target: >80% code coverage)
- [ ] Integration tests added for cross-component interactions
- [ ] Existing tests still pass (including regression tests)
- [ ] Manual testing completed for UI changes or critical flows
- [ ] Negative test cases and error handling verified
- [ ] Performance acceptable for expected load

### Code Review
- [ ] Pull request created with clear description and linked issue
- [ ] PR follows team conventions (<400 lines preferred, well-scoped changes)
- [ ] At least one team member has approved the PR
- [ ] All review comments addressed or discussed
- [ ] No unresolved conflicts or merge issues

### CI/CD & Automation
- [ ] All CI checks pass (build, lint, tests, security scans)
- [ ] No new high-severity security vulnerabilities introduced
- [ ] Code builds successfully in all target environments
- [ ] Automated tests run and pass in CI pipeline

### Documentation
- [ ] Inline code comments added for complex logic
- [ ] README or technical docs updated if public APIs or architecture changed
- [ ] User-facing documentation updated (if applicable)
- [ ] Runbook or operational docs updated for deployment/configuration changes
- [ ] CHANGELOG or release notes entry added (if applicable)

### Deployment Readiness
- [ ] Feature flags or toggles configured appropriately
- [ ] Database migrations tested and reversible (if applicable)
- [ ] Rollback plan documented
- [ ] Monitoring and alerting configured for new functionality
- [ ] Logging includes appropriate context for debugging

### Team Alignment
- [ ] Demo prepared (if demoing in sprint review)
- [ ] Product Owner or stakeholder has reviewed and accepted the work
- [ ] Known limitations or follow-up work documented as new issues
- [ ] Work item moved to "Done" column on project board

---

## DoD Checklist for Sprint/Iteration

### Sprint Goals
- [ ] All committed work items meet individual DoD criteria
- [ ] Sprint goal achieved or explicitly adjusted with stakeholder agreement
- [ ] No critical bugs introduced during the sprint

### Quality Gates
- [ ] Overall code coverage remains above threshold (e.g., 80%)
- [ ] No increase in high-severity tech debt items
- [ ] Performance benchmarks met
- [ ] Security scan results reviewed and critical issues resolved

### Team Health
- [ ] Retrospective held and action items captured
- [ ] Team velocity and burndown reviewed
- [ ] Blockers identified and escalated if needed
- [ ] Sprint demo conducted with stakeholders

### Documentation & Communication
- [ ] Sprint summary shared with stakeholders
- [ ] Release notes updated with completed features
- [ ] Project board reflects accurate status
- [ ] Stakeholders notified of any scope or timeline changes

---

## DoD Checklist for Release

### Pre-Release
- [ ] All features meet individual and sprint DoD criteria
- [ ] Release notes finalized and reviewed
- [ ] User-facing documentation complete and published
- [ ] Security review completed (if required)
- [ ] Accessibility audit passed (if required)
- [ ] Performance testing completed under expected load
- [ ] Smoke tests prepared and ready to run
- [ ] Rollback procedure documented and tested
- [ ] Support and customer-facing teams trained on new features

### Deployment
- [ ] Deployment plan reviewed and approved
- [ ] Deployed to staging environment successfully
- [ ] Smoke tests pass on staging
- [ ] Deployed to production successfully
- [ ] Smoke tests pass on production
- [ ] Monitoring confirms system health post-deployment

### Post-Release
- [ ] Release announcement sent to stakeholders and users
- [ ] Success metrics tracked and reported
- [ ] No critical production issues (P0/P1 bugs)
- [ ] Support tickets monitored for release-related issues
- [ ] Post-release retrospective scheduled

---

## Customization Guide

### For Different Work Types

**Feature Development**:
- Emphasize user testing and acceptance criteria
- Include UI/UX review in DoD

**Bug Fixes**:
- Include regression test to prevent recurrence
- Verify fix in environment where bug was reported
- Document root cause in bug ticket

**Technical Debt / Refactoring**:
- Performance metrics show improvement or no regression
- Test coverage maintained or improved
- Architecture documentation updated

**Infrastructure / DevOps**:
- Runbooks updated with new procedures
- Rollback tested
- Monitoring and alerting verified
- Cost impact documented

**Documentation**:
- Technical accuracy verified by engineer
- Spelling and grammar checked
- Examples tested and working
- Links verified

### For Different Project Phases

**Early Project (MVP)**:
- May accept lower test coverage initially
- Focus on core functionality over edge cases
- Prioritize speed of learning over perfection

**Growth Phase**:
- Standard DoD fully enforced
- Balance velocity with quality

**Mature/Production**:
- Stricter quality gates
- More comprehensive testing
- Thorough documentation required

---

## Common DoD Pitfalls to Avoid

❌ **Too Vague**: "Code is good quality"
✅ **Specific**: "Code passes linter, has >80% coverage, and follows style guide"

❌ **Too Burdensome**: 50+ checklist items that slow down every small change
✅ **Right-Sized**: 10-20 essential criteria that ensure quality without bureaucracy

❌ **Ignored in Practice**: DoD defined but never referenced or enforced
✅ **Living Document**: Team reviews and updates DoD quarterly, uses it in daily work

❌ **One Size Fits All**: Same DoD for every work item type
✅ **Context-Aware**: Base DoD with reasonable exceptions for different work types

❌ **Not Team-Owned**: DoD imposed by management without team input
✅ **Collaborative**: Entire team agrees on and commits to the DoD

---

## Example DoD for Different Scenarios

### Example 1: Simple UI Component

**Acceptance Criteria Met**:
- ✅ Button renders correctly on desktop and mobile
- ✅ Clicking button triggers expected action
- ✅ Loading state displays during async operations
- ✅ Error state displays if action fails

**Code Quality**:
- ✅ Component follows React best practices
- ✅ PropTypes defined or TypeScript types used
- ✅ No console warnings in browser

**Testing**:
- ✅ Unit tests cover happy path and error state
- ✅ Manual testing in Chrome, Firefox, Safari
- ✅ Accessibility tested with screen reader

**Documentation**:
- ✅ Storybook story added for component
- ✅ Usage example in component documentation

**Result**: Work item moves to "Done" ✅

### Example 2: API Endpoint Development

**Acceptance Criteria Met**:
- ✅ Endpoint returns correct data format
- ✅ Handles authentication and authorization
- ✅ Validates input parameters
- ✅ Returns appropriate HTTP status codes

**Code Quality**:
- ✅ Follows REST or GraphQL conventions
- ✅ Error handling for all failure modes
- ✅ Database queries optimized

**Testing**:
- ✅ Unit tests for business logic (90% coverage)
- ✅ Integration tests for API endpoints
- ✅ Load testing shows acceptable performance
- ✅ Security scan passes (no SQL injection, XSS, etc.)

**Documentation**:
- ✅ OpenAPI/Swagger spec updated
- ✅ Example request/response documented
- ✅ Error codes and handling documented

**Deployment Readiness**:
- ✅ Logging includes request ID for tracing
- ✅ Metrics tracked for latency and error rate
- ✅ Database migration tested and reversible

**Result**: Work item moves to "Done" ✅

---

## DoD Review Cadence

- **Monthly**: Review DoD with team, identify improvements
- **Quarterly**: Update DoD based on lessons learned
- **After Major Incidents**: Assess if DoD gaps contributed to the issue
- **Onboarding**: Review DoD with new team members

---

## Related Resources
- [Execution & Tracking](octoacme-execution-and-tracking.md)
- [Project Planning](octoacme-project-planning.md)
- [Release & Deployment Guide](octoacme-release-and-deployment.md)

---

## DoD Quick Reference Card

Print or bookmark this section for daily use:

### Every Work Item Must Have:
1. ✅ Acceptance criteria met
2. ✅ Tests written and passing
3. ✅ Code reviewed and approved
4. ✅ CI/CD checks green
5. ✅ Documentation updated
6. ✅ Ready to deploy

### Red Flags (Don't Mark Done):
- ❌ "Works on my machine" but CI fails
- ❌ Tests commented out or skipped
- ❌ TODO comments for core functionality
- ❌ Merge conflicts unresolved
- ❌ Reviewer requested changes not addressed

---

**Remember**: The Definition of Done protects quality and reduces technical debt. When in doubt, don't mark it done—address the gap or add a follow-up task.
