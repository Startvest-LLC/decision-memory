# Decision Memory

A Claude Skill for capturing product decisions with rationale and context.

**The problem**: Teams make product decisions every day, but the reasoning gets lost. Six months later, nobody remembers *why* they rejected that feature or *what* prompted the pivot.

**The solution**: Decision Memory helps Claude recognize decision moments in conversation, prompt for rationale, and build an audit trail.

## What It Does

- **Listens** for decision triggers: "Let's go with...", "We're rejecting...", "Ship it!"
- **Prompts** for the "why" behind decisions
- **Structures** decisions as searchable records
- **Helps** close the loop with stakeholders

## Quick Start

### Claude.ai / Claude Apps

1. Go to **Settings > Capabilities > Skills**
2. Search for "decision-memory"
3. Enable the skill
4. Start making decisions in chat!

### Claude Code

```bash
# Clone to your skills directory
git clone https://github.com/Startvest-LLC/decision-memory.git ~/.claude/skills/decision-memory
```

### API

```python
from anthropic.lib import files_from_dir

skill = client.beta.skills.create(
    display_title="Decision Memory",
    files=files_from_dir("./decision-memory"),
    betas=["skills-2025-10-02"]
)
```

## Example

**You**: We're going to reject the dark mode request for now.

**Claude**: Sounds like a decision! Quick questions:
- Why are we saying no?
- Is this permanent or "not now"?
- Should we notify the requester?

**You**: Low usage data, not worth 3 weeks of dev. It's a "not now" - revisit in Q3. Yes, notify.

**Claude**:
```markdown
## Decision: Defer Dark Mode

**Type**: Deferred
**Rationale**: Low usage data (<5% users). 3 weeks dev effort not justified.
**Revisit**: Q3 2025

### Closure Message (Draft)
Thanks for suggesting dark mode! We're not building this right now,
but we're tracking interest. We'll revisit in Q3.
```

## Enhance with IdeaLift MCP

This skill works standalone, but pairs powerfully with [IdeaLift MCP](https://idealift.startvest.ai/mcp):

| Standalone | With IdeaLift MCP |
|------------|-------------------|
| Markdown output | Persisted to database |
| Manual save | Automatic audit trail |
| No linking | Links decisions to ideas |
| No history | Full decision history |

See [GUIDES/mcp-integration.md](GUIDES/mcp-integration.md) for setup.

## Files

```
decision-memory/
├── SKILL.md                    # Main skill instructions
├── QUICKSTART.md              # 2-minute guide
├── EXAMPLES.md                # Conversation examples
├── TEMPLATES/
│   ├── decision-record.md     # ADR-style template
│   ├── closure-message.md     # Ship notification
│   └── rejection-rationale.md # Saying no constructively
├── GUIDES/
│   ├── decision-triggers.md   # Phrases that trigger capture
│   └── mcp-integration.md     # IdeaLift MCP setup
└── PATTERNS/
    ├── accept.md              # Accepting ideas
    ├── reject.md              # Rejecting ideas
    ├── defer.md               # Deferring ideas
    └── merge.md               # Merging duplicates
```

## Decision Types

| Type | When | Example Trigger |
|------|------|-----------------|
| **Accept** | Moving forward | "Let's do it", "Approved" |
| **Reject** | Saying no | "We're not doing this", "Killed" |
| **Defer** | Not now | "Maybe later", "Park it" |
| **Merge** | Combining | "Same as X", "Duplicate" |
| **Ship** | Launched | "It's live", "Released" |

## Why Decision Memory?

Most tools focus on *what* you're building (tickets, tasks, sprints).

Nobody helps with *why* you decided:
- Why did we reject that feature?
- What was the reasoning behind the pivot?
- When should we revisit this decision?

Decision Memory fills that gap.

## License

MIT

## Contributing

Issues and PRs welcome at [github.com/Startvest-LLC/decision-memory](https://github.com/Startvest-LLC/decision-memory).

---

Built by [Startvest](https://startvest.ai) · Works great with [IdeaLift](https://idealift.startvest.ai)
