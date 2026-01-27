# Defer Pattern

How to capture decisions when postponing, not rejecting.

## Triggers

- "Not now"
- "Maybe later"
- "Defer to Q3"
- "Backlog it"
- "Park it"
- "Put it on the back burner"

## Prompts to Ask

1. **Blocker**: What's preventing us from doing this now?
2. **Trigger**: What would need to change to prioritize this?
3. **Timeline**: When should we revisit?
4. **Track**: How do we remember to reconsider?

## Example Flow

**User**: Let's defer the dark mode feature.

**Claude**: Deferring dark mode. Quick questions:
- What's blocking this now?
- What would make us prioritize it?
- When should we revisit?

**User**: We're focused on enterprise features this quarter. If we get 50 requests or a big customer asks, we'd reprioritize. Revisit at Q2 planning.

**Claude**:
```markdown
## Decision: Defer Dark Mode

**Date**: 2025-01-27
**Type**: Deferred
**Decider**: Product Team

### Context
~15 users requested dark mode. Evaluated during Q1 planning.

### Decision
Deferring to Q2 at earliest.

### Rationale
Current quarter focused on enterprise features (API, SSO, audit logs).
Dark mode is a nice-to-have that doesn't move enterprise deals.

### Revisit Triggers
Reprioritize if:
- Request count hits 50
- Enterprise customer requests it
- Q2 has capacity

### Timeline
Revisit at Q2 planning (April 2025)

### Tracking
- Set calendar reminder for Q2 planning
- Monitor request count in feedback tool
```

## Defer vs Reject

| Defer | Reject |
|-------|--------|
| "Not now" | "Not ever" (or not foreseeable) |
| Has revisit conditions | No path to reconsideration |
| Communicates "we hear you" | Communicates "this isn't for us" |

## Tips

- Set specific revisit triggers, not vague "later"
- Track conditions that would change the decision
- Communicate the "why" to requesters
