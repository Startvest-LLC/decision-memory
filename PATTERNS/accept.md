# Accept Pattern

How to capture decisions when moving forward with an idea.

## Triggers

- "Let's do it"
- "Approved"
- "Ship it"
- "Green light"
- "We're going with..."

## Prompts to Ask

1. **Core driver**: What's the main reason we're doing this?
2. **Conditions**: Any constraints, dependencies, or must-haves?
3. **Timeline**: When does this need to ship?
4. **Notify**: Who should know about this decision?

## Example Flow

**User**: Let's build the API rate limiting feature.

**Claude**: Great - approving API rate limiting. Quick questions:
- What's driving this decision?
- Any conditions or constraints?
- Target timeline?

**User**: Three enterprise customers requested it, and it's blocking a big deal. Ship in 6 weeks, needs to support custom limits per API key.

**Claude**:
```markdown
## Decision: Build API Rate Limiting

**Date**: 2025-01-27
**Type**: Accepted
**Decider**: Product Team

### Context
Three enterprise customers requested this feature. Blocking $50K deal with Acme Corp.

### Decision
Building API rate limiting with custom limits per API key.

### Rationale
Strong customer demand + revenue impact. Three requests from paying enterprise customers, one blocking active deal.

### Constraints
- Must support per-key custom limits
- Target: 6 weeks (Q1 deadline)

### Next Steps
- [ ] Create JIRA epic
- [ ] Assign to backend team
- [ ] Notify sales about timeline
```

## Tips

- Capture the business driver (revenue, retention, competitive)
- Note any constraints that shaped the decision
- Include who needs to be notified
