# OctoAcme — Retrospective & Continuous Improvement

## Purpose
Capture learnings and convert them into actionable improvements.

## When
After each sprint, release, or important milestone. Also after incidents.

## Structure
A successful retrospective includes:
- **What went well** — Celebrate successes and effective practices
- **What could be improved** — Identify challenges and pain points (blameless)
- **Action items** — Convert insights into specific, actionable improvements (owner, due date)
- **Follow-up on previous action items** — Review progress on commitments from last retrospective

### Example Retrospective Agenda (60 minutes)
1. **Set the stage** (5 min): Review purpose, ground rules, psychological safety reminder
2. **Gather data** (15 min): Silent reflection, then share what went well and what could improve
3. **Generate insights** (15 min): Identify patterns and themes
4. **Decide what to do** (15 min): Prioritize 2-3 action items with owners and due dates
5. **Close** (10 min): Review previous action items, summarize new commitments, thank participants

## Running a Retrospective
- **Timebox**: 45–75 minutes depending on team size
- **Facilitate neutrally**: PM or rotating facilitator; focus on listening, not defending
- **Use an anonymous idea board** if needed to encourage candor (e.g., Miro, Retrium, sticky notes)
- **Prioritize 2–3 top action items** to avoid overload; focus on impact
- **Make it safe**: Emphasize blameless culture—focus on systems and processes, not individuals
- **Rotate formats**: Try different retrospective formats to keep engagement high (e.g., Start/Stop/Continue, 4 Ls: Liked/Learned/Lacked/Longed For, Sailboat)

### Ground Rules for Psychological Safety
- What's said in the retro stays in the retro (unless action items)
- Focus on processes and systems, not people
- All feedback is valuable; no judgment
- Be specific with examples, but avoid finger-pointing
- Listen to understand, not to respond

## Tracking Improvements
- Add action items to the project backlog or issues with clear owners and timelines
- Review outstanding actions in the weekly PM sync

## Example Action Item Template
- **Title**: [Clear, actionable description]
- **Description**: [Detailed explanation of the improvement and its expected benefit]
- **Owner**: [Specific person responsible for driving this forward]
- **Due date**: [Realistic completion date]
- **Success criteria**: [How we'll know this is complete and effective]

### Example Action Items

**Action Item 1**:
- **Title**: Add automated linting to PR checks
- **Description**: Currently code style issues are caught late in review. Add ESLint to CI pipeline to catch issues before human review.
- **Owner**: DevOps Lead (Jordan)
- **Due date**: 2025-02-15
- **Success criteria**: All PRs automatically run ESLint; 0 style-related review comments in following sprint

**Action Item 2**:
- **Title**: Create PR size guideline and educate team
- **Description**: Large PRs (>500 lines) are difficult to review and delay feedback. Document guideline and share in team meeting.
- **Owner**: PM (Alex)
- **Due date**: 2025-02-08
- **Success criteria**: 80%+ of PRs under 400 lines; average review time < 4 hours

## Continuous Improvement Culture
- **Measure impact of action items**: Track whether changes lead to desired outcomes
- **Celebrate improvements**: Recognize when action items deliver value
- **Make small, iterative changes**: Avoid trying to fix everything at once
- **Share learnings across teams**: What worked for your project may help others
- **Revisit and refine**: Not all action items will succeed—learn and adjust

### Anti-Patterns to Avoid
❌ **Action item graveyard**: Creating action items that are never completed
✅ **Commit to 2-3 high-impact items** you'll actually complete

❌ **Same issues every retro**: Identifying problems but never addressing root causes
✅ **Track themes over time** and escalate systemic issues

❌ **Blame-focused feedback**: "Person X always does Y"
✅ **System-focused feedback**: "Our deployment process lacks verification steps"

❌ **Skipping retros when busy**: "We'll do one next sprint"
✅ **Protect retro time** as essential investment in continuous improvement
