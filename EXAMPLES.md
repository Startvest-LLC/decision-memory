# Examples

Real conversation examples showing Decision Memory in action.

## Example 1: Rejecting a Feature Request

**User**: We got another request for Excel export. I think we need to say no.

**Claude**: Got it - rejecting Excel export. Quick questions:
- Why are we saying no?
- Is this permanent or "not now"?
- Should I draft a message for the requester?

**User**: Only 3 people have asked for it out of 500 customers. CSV works fine. It's a "not now" - if 20 people ask, we'll reconsider. Yes, draft something nice.

**Claude**: Here's the decision record:

```markdown
## Decision: Defer Excel Export

**Date**: 2025-01-27
**Type**: Deferred
**Decider**: Product Team

### Context
3 of 500 customers requested native Excel export.

### Decision
Not building Excel export now. Revisit at 20 requests.

### Rationale
Low demand (<1% of customers). CSV export covers the use case.
Dev effort (~2 weeks) doesn't justify reach.

### Revisit
When request count hits 20.

### Closure Message (Draft)

Hi [Name],

Thanks for suggesting Excel export! We've decided not to build this right now - our CSV export works well with Excel, and only a small number of customers have requested native support.

If demand grows, we'll prioritize it. In the meantime, here's a quick tip: you can open our CSV exports directly in Excel and use "Save As" to convert to .xlsx format.

Keep the feedback coming!
```

---

## Example 2: Approving with Conditions

**User**: Let's green light the SSO integration.

**Claude**: Approving SSO integration. Quick questions:
- What's driving this decision?
- Any conditions or constraints?
- Target timeline?

**User**: Acme Corp deal is blocked on it - $100K ARR. They need SAML specifically, not just OAuth. Need it in 6 weeks.

**Claude**: Here's the decision record:

```markdown
## Decision: Build SSO Integration (SAML)

**Date**: 2025-01-27
**Type**: Accepted
**Decider**: Product Team

### Context
Acme Corp ($100K ARR) deal blocked on SSO support.

### Decision
Building SAML SSO integration.

### Rationale
Direct revenue impact - $100K deal on the line.
Multiple enterprise prospects have asked, Acme just has the tightest deadline.

### Constraints
- Must be SAML (not just OAuth)
- 6-week deadline (Acme contract deadline)
- Need Okta and Azure AD support at minimum

### Next Steps
- [ ] Create JIRA epic with 6-week timeline
- [ ] Confirm scope with Acme
- [ ] Assign to authentication team
```

---

## Example 3: Shipping and Closing the Loop

**User**: The new dashboard redesign went live this morning!

**Claude**: Congrats on shipping! Let's close the loop:
- Who originally requested the redesign?
- Should we send announcements?
- Any follow-up needed?

**User**: It came from the NPS survey feedback - about 20 people mentioned the old dashboard was confusing. Yes, let's do an in-app announcement and email the loudest complainers directly. Track adoption for a week.

**Claude**: Here's the ship record:

```markdown
## Decision: Ship Dashboard Redesign

**Date**: 2025-01-27
**Type**: Shipped

### What Shipped
Complete dashboard redesign with:
- Simplified navigation
- Customizable widgets
- Mobile-responsive layout

### Original Feedback
~20 NPS respondents mentioned dashboard confusion.

### Announcements

**In-App Banner:**
New dashboard is live! We simplified navigation and added customizable widgets based on your feedback.

**Email to Vocal Requesters:**
Hi [Name],

Remember when you told us the dashboard was confusing? We listened.

The new dashboard is live with simplified navigation and customizable widgets. Check it out at [link].

Thanks for the feedback - it made our product better.

### Follow-up
- [ ] Track widget customization rate (1 week)
- [ ] Monitor support tickets for confusion
- [ ] Run NPS again in 30 days
```

---

## Example 4: Merging Duplicate Ideas

**User**: These two requests are basically the same thing - "keyboard shortcuts" and "power user mode".

**Claude**: Merging these ideas. Quick questions:
- Which becomes the primary?
- Anything unique in the other to preserve?
- Notify both requesters?

**User**: Make "keyboard shortcuts" the primary - it's more specific. The "power user mode" one mentioned wanting a command palette too, so note that. Notify both.

**Claude**: Here's the merge record:

```markdown
## Decision: Merge Power User Requests

**Date**: 2025-01-27
**Type**: Merged

### Ideas Merged
- **Primary**: #89 "Keyboard shortcuts"
- **Merged**: #112 "Power user mode"

### Preserved from #112
- Command palette (Cmd+K style) in addition to shortcuts
- Quick actions menu

### Notifications

**To #89 requester:**
FYI - we merged another related request into yours. Added to scope: command palette for quick actions.

**To #112 requester:**
Thanks for the power user mode idea! We've combined this with our keyboard shortcuts feature. Your command palette suggestion is included - we'll build a Cmd+K style launcher.
```

---

## Example 5: Deferring with Clear Trigger

**User**: We should probably defer the mobile app until next year.

**Claude**: Deferring mobile app. Quick questions:
- What's blocking this now?
- What would make us prioritize it sooner?
- When should we revisit?

**User**: No mobile devs on the team and 90% of usage is desktop. If mobile usage hits 25% or we hire mobile devs, reconsider. Check at Q1 2026 planning.

**Claude**: Here's the deferral record:

```markdown
## Decision: Defer Mobile App

**Date**: 2025-01-27
**Type**: Deferred
**Decider**: Product Team

### Context
Users have requested native iOS/Android apps.

### Decision
Deferring mobile app development to 2026 at earliest.

### Rationale
1. No mobile development capacity (would need to hire)
2. 90% of current usage is desktop
3. Web app works on mobile browsers as interim solution

### Revisit Triggers
Reprioritize if:
- Mobile usage exceeds 25% of sessions
- We hire mobile developers
- Major competitor launches mobile app

### Timeline
Formal revisit at Q1 2026 planning.

### Tracking
- Monitor mobile browser usage monthly
- Flag if competitor mobile app launches
```

---

## Tips from These Examples

1. **Be specific**: Numbers and names, not vague language
2. **Set triggers**: What would change the decision?
3. **Close the loop**: Notify requesters
4. **Track follow-ups**: What to monitor after deciding
