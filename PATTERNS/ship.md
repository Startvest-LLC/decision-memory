# Ship Pattern

How to capture decisions when features launch and close the loop.

## Triggers

- "It's live"
- "We shipped"
- "Released in v2.3"
- "Launched yesterday"
- "Now available"
- "Deployed to production"

## Prompts to Ask

1. **What shipped**: Brief description of what went live
2. **Requesters**: Who originally asked for this?
3. **Notify**: Should we send announcements?
4. **Follow-up**: Any post-launch tracking needed?

## Example Flow

**User**: The API rate limiting feature is live!

**Claude**: Congrats on shipping! Let's close the loop:
- Who originally requested this?
- Should we send notifications?
- Any follow-up needed post-launch?

**User**: Three enterprise customers asked - Acme, Globex, and Initech. Yes, notify all of them. We should check adoption in 2 weeks.

**Claude**:
```markdown
## Decision: Ship API Rate Limiting

**Date**: 2025-01-27
**Type**: Shipped
**Decider**: Product Team

### What Shipped
API rate limiting with custom limits per API key.
- Configurable limits (requests/minute)
- Real-time usage dashboard
- Alert notifications

### Original Requesters
- Acme Corp (Sarah)
- Globex (Mike)
- Initech (Linda)

### Closure Messages

**To Acme Corp:**
Hey Sarah! Great news - the API rate limiting feature you requested is now live.

**Where to find it**: Settings > API > Rate Limits

You can now set custom limits per API key and monitor usage in real-time. Let us know how it works for your team!

**To Globex:**
[Similar message]

**To Initech:**
[Similar message]

### Follow-up
- [ ] Check adoption metrics in 2 weeks
- [ ] Gather feedback from requesters
- [ ] Document in release notes
```

## Tips

- Always identify original requesters
- Send personalized closure messages
- Set follow-up checkpoints
- Celebrate the team! (They shipped something)
