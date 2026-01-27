# MCP Integration with IdeaLift

Enhance Decision Memory with automatic persistence via IdeaLift MCP.

## Why Integrate?

| Standalone | With IdeaLift MCP |
|------------|-------------------|
| Outputs markdown | Persists to database |
| Manual save | Automatic audit trail |
| No linking | Links decisions to ideas |
| No history | Searchable decision history |
| Session-only | Permanent memory |

## Setup

### 1. Get an API Key

1. Go to [idealift.startvest.ai/mcp](https://idealift.startvest.ai/mcp)
2. Sign in or create account
3. Navigate to Settings > API Keys
4. Generate a new key (starts with `il_live_`)

### 2. Install mcp-remote

```bash
npm install -g mcp-remote
```

### 3. Configure Claude Desktop

Add to `claude_desktop_config.json`:

**macOS**: `~/Library/Application Support/Claude/claude_desktop_config.json`
**Windows**: `%APPDATA%\Claude\claude_desktop_config.json`

```json
{
  "mcpServers": {
    "idealift": {
      "command": "mcp-remote",
      "args": [
        "https://idealift.startvest.ai/api/mcp",
        "--header",
        "Authorization: Bearer YOUR_API_KEY"
      ]
    }
  }
}
```

### 4. Restart Claude Desktop

Fully quit (not just close window) and reopen.

Check Settings > Developer - IdeaLift should show as "running".

## Combined Workflow

With both Skill + MCP connected:

### Example: Rejecting an Idea

**You**: We're not doing the Excel export feature.

**Claude** (using Decision Memory skill):
> Got it - rejecting Excel export. Quick questions:
> - Why are we saying no?
> - Is this permanent or "not now"?
> - Should we notify the requester?

**You**: Low demand, only 3 customers asked. Not now - revisit at 10 requests. Yes notify.

**Claude** (using IdeaLift MCP):
> Decision logged to IdeaLift:
> - Decision: Defer Excel Export
> - Linked to idea #142
> - Revisit trigger set: 10 requests
>
> Draft closure message ready. Want me to send it?

## Available MCP Tools

When IdeaLift MCP is connected, Claude can use:

| Tool | Purpose |
|------|---------|
| `log_decision` | Record decision with rationale |
| `get_decision_history` | View all decisions for an idea |
| `list_ideas` | Find ideas to link decisions to |
| `update_idea` | Change idea status based on decision |

## What Gets Logged

Each decision logged includes:
- Decision type (accept/reject/defer/merge/ship)
- Rationale (the "why")
- Timestamp
- Link to related idea (if applicable)
- Revisit conditions
- Closure notification status

## Fallback Behavior

If MCP connection fails:
- Skill still works
- Outputs markdown instead
- Prompts user to save manually
- No automatic persistence

## Troubleshooting

**MCP not connecting?**
- Check API key is valid
- Verify mcp-remote is installed globally
- Restart Claude Desktop completely

**Decisions not persisting?**
- Check MCP shows "running" in Settings
- Verify you have workspace access
- Check rate limits haven't been exceeded

**Can't find idea to link?**
- Use `list_ideas` to search
- Decision can be logged without link
- Link manually later in IdeaLift UI
