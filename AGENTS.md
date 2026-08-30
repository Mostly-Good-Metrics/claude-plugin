# Agent instructions

The canonical MGM skill source is `Mostly-Good-Metrics/skills`. This repository
packages a synchronized mirror for Claude Code together with `.mcp.json`.

Make skill behavior changes in the portable skills repository first, then copy
the complete `skills/` tree here. Do not add private Support MCP or admin-only
workflows to this public customer plugin. Keep plugin setup in `README.md` and
portable usage in the canonical skills repository.

Run the skill-sync workflow or compare this `skills/` directory with the
canonical repository before release. Do not publish or change the production
MCP endpoint unless explicitly requested.
