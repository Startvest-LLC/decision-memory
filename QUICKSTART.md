# Quick Start

Get decision memory working in 2 minutes.

## 1. Enable the Skill

**Claude Apps**: Settings > Capabilities > Skills > Search "decision-memory" > Enable

**Claude Code**: `git clone https://github.com/Startvest-LLC/decision-memory.git ~/.claude/skills/decision-memory`

## 2. Make a Decision

Just talk naturally. Say something like:

> "We're going to reject the mobile app idea."

or

> "Let's ship the dashboard redesign."

## 3. Answer the Prompts

Claude will ask 2-3 quick questions:
- Why are we deciding this?
- Any conditions or follow-ups?
- Who should we notify?

## 4. Get Your Decision Record

Claude outputs a structured record you can save or (with IdeaLift MCP) auto-logs.

## That's It

Decision Memory runs in the background. No special commands needed - just make decisions and Claude will help capture them.

## Optional: Add IdeaLift MCP

For auto-persistence and full audit trails, connect IdeaLift MCP:

1. Get API key: [idealift.startvest.ai/mcp](https://idealift.startvest.ai/mcp)
2. Configure Claude Desktop (see [GUIDES/mcp-integration.md](GUIDES/mcp-integration.md))
3. Decisions now auto-log!
