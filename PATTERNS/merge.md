# Merge Pattern

How to capture decisions when combining similar ideas.

## Triggers

- "Same as X"
- "Duplicate of..."
- "Combine with..."
- "Merge into..."
- "That's basically..."

## Prompts to Ask

1. **Primary**: Which idea becomes the canonical one?
2. **Unique**: What's unique about each that should be preserved?
3. **Notify**: Should we tell requesters their idea was merged?
4. **Attribution**: How do we credit all contributors?

## Example Flow

**User**: The "export to PDF" request is basically the same as "download reports".

**Claude**: Merging these ideas. Quick questions:
- Which one becomes the primary?
- Anything unique in the other that should be noted?
- Should we notify both requesters?

**User**: Make "download reports" the primary - it's more general. The PDF request specifically mentioned styling, so note that. Yes, notify both.

**Claude**:
```markdown
## Decision: Merge Export Ideas

**Date**: 2025-01-27
**Type**: Merged
**Decider**: Product Team

### Ideas Merged
- **Primary**: #142 "Download Reports"
- **Merged**: #156 "Export to PDF"

### Decision
Consolidating into single feature request for report exports.

### Preserved Details
From #156: Users want styled PDFs, not just raw data dumps. Include formatting options.

### Attribution
Both requesters credited on primary idea.

### Notifications

**To requester of #156:**
Thanks for the PDF export suggestion! We've combined this with a broader "Download Reports" feature we're planning. Your input about styling and formatting has been noted - we'll make sure exports look polished, not just raw data dumps.

**To requester of #142:**
FYI - we've merged another request into your Download Reports idea. Added requirement: exports should be well-formatted (PDF styling).
```

## Tips

- Preserve unique requirements from merged ideas
- Credit all contributors
- Notify requesters so they don't feel ignored
- Document what was combined for future reference
