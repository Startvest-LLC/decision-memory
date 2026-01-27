# Reject Pattern

How to capture decisions when saying no to an idea.

## Triggers

- "We're not doing this"
- "That's a no"
- "Rejected"
- "Killing it"
- "Not happening"

## Prompts to Ask

1. **Reason**: Why are we saying no? (Be specific)
2. **Permanence**: Is this forever or circumstantial?
3. **Alternative**: Is there a workaround or alternative?
4. **Notify**: Should we tell the requester? Draft message?

## Example Flow

**User**: We need to reject the mobile app request.

**Claude**: Got it - rejecting mobile app. Quick questions:
- Why are we saying no?
- Is this permanent or could it change?
- Should we notify the requester with an explanation?

**User**: We don't have mobile dev capacity, and our analytics show 95% of usage is desktop. It's not permanent - maybe in 2026 if mobile usage grows. Yes, draft a message.

**Claude**:
```markdown
## Decision: Reject Mobile App

**Date**: 2025-01-27
**Type**: Rejected
**Decider**: Product Team

### Context
Multiple users requested native mobile apps (iOS/Android).

### Decision
Not building mobile apps.

### Rationale
Two factors:
1. No mobile dev capacity on current team
2. Analytics show 95% desktop usage - demand doesn't justify investment

### Revisit
2026 planning, if mobile usage exceeds 20% of sessions.

### Closure Message (Draft)
Thanks for suggesting mobile apps! We've decided not to build native apps right now because 95% of our usage is on desktop. We're focusing our dev resources where they'll have the most impact. If mobile usage grows significantly, we'll revisit this in 2026. In the meantime, our web app works on mobile browsers.
```

## Tips

- Be honest about the real reason
- Distinguish "never" from "not now"
- Always offer closure communication
- Set concrete revisit conditions
