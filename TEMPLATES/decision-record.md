# Decision Record Template

Use this structure when capturing decisions.

```markdown
## Decision: [Short Title]

**Date**: [YYYY-MM-DD]
**Type**: [Accepted | Rejected | Deferred | Merged | Shipped]
**Decider**: [Name or Role]

### Context
[What prompted this decision? What's the background?]

### Decision
[What we decided - one clear sentence]

### Rationale
[Why we decided this way - be specific, not vague]

### Consequences
[What happens as a result of this decision?]

### Revisit
[When to reconsider: Never | Specific date | Trigger condition]
```

## Example: Filled Out

```markdown
## Decision: Defer Dark Mode

**Date**: 2025-01-27
**Type**: Deferred
**Decider**: Product Team

### Context
15 users requested dark mode over the past quarter. We evaluated during Q1 planning.

### Decision
Not building dark mode now. Will revisit in Q3 2025.

### Rationale
Usage analytics show <5% of users work in low-light environments.
3 weeks of dev effort doesn't justify the reach at current demand levels.
If request volume triples, the calculus changes.

### Consequences
- Notify requesters with honest explanation
- Track request volume in Q2
- Re-evaluate if we hit 50 requests

### Revisit
Q3 2025, or sooner if request volume hits 50.
```

## Tips

- **Be specific**: "Low demand" → "15 requests vs 10,000 MAU"
- **Be honest**: Real reasons, not PR-speak
- **Set triggers**: What would change your mind?
