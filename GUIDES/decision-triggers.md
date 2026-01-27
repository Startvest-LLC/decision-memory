# Decision Triggers

Phrases and patterns that signal a decision is being made.

## Accept Triggers

Signals that something is being approved or moving forward.

| Phrase | Confidence |
|--------|------------|
| "Let's do it" | High |
| "Approved" | High |
| "Ship it" | High |
| "Green light" | High |
| "We're going with..." | High |
| "Moving forward with..." | High |
| "I like option A" | Medium |
| "That sounds good" | Medium |
| "Let's build..." | Medium |

## Reject Triggers

Signals that something is being declined.

| Phrase | Confidence |
|--------|------------|
| "We're not doing this" | High |
| "That's a no" | High |
| "Rejected" | High |
| "Killing it" | High |
| "Not happening" | High |
| "We decided against..." | High |
| "I don't think we should..." | Medium |
| "That's not going to work" | Medium |
| "Pass on this one" | Medium |

## Defer Triggers

Signals that something is being postponed, not rejected.

| Phrase | Confidence |
|--------|------------|
| "Not now" | High |
| "Maybe later" | High |
| "Defer to Q3" | High |
| "Backlog it" | High |
| "Park it" | High |
| "Put it on the back burner" | High |
| "Not a priority right now" | Medium |
| "Revisit in..." | Medium |
| "Let's wait until..." | Medium |

## Merge Triggers

Signals that ideas are being combined.

| Phrase | Confidence |
|--------|------------|
| "Same as X" | High |
| "Duplicate of..." | High |
| "Combine with..." | High |
| "Merge into..." | High |
| "That's basically..." | Medium |
| "Similar to what we're doing with..." | Medium |

## Ship Triggers

Signals that something has launched.

| Phrase | Confidence |
|--------|------------|
| "It's live" | High |
| "We shipped" | High |
| "Released in v2.3" | High |
| "Launched yesterday" | High |
| "Now available" | High |
| "Deployed to production" | High |
| "Customers can now..." | Medium |
| "Rolled out to..." | Medium |

## Prompting Behavior

**High confidence triggers**: Immediately prompt for rationale capture.

**Medium confidence triggers**: Ask for confirmation first:
> "That sounds like a decision. Want me to capture the rationale?"

## Context Matters

Some phrases need context:
- "We're not doing this" in a planning meeting = rejection
- "We're not doing this" referring to a bug = might just be clarification

When uncertain, ask:
> "Is that a product decision you'd like me to capture?"
