# Mostly Good Metrics — Claude Code Plugin

The official [Mostly Good Metrics](https://mostlygoodmetrics.com) plugin for [Claude Code](https://claude.com/claude-code). It connects Claude to your MGM projects via MCP and bundles the complete portable MGM skill set.

## Install

```
/plugin marketplace add Mostly-Good-Metrics/claude-plugin
/plugin install mostly-good-metrics@mostly-good-metrics
```

**First run:** the first time Claude calls an MGM tool, Claude Code opens your browser to sign in to Mostly Good Metrics (OAuth). No API keys or manual configuration needed — approve once and you're connected.

## What you get

The plugin connects the MGM MCP server (`https://app.mostlygoodmetrics.com/mcp`), giving Claude tools to query events, run and save queries, build funnels, measure retention, manage experiments, and read your dashboard.

### Skills

- **analyze-metrics** — Claude uses this automatically when you ask how something is doing.
  - "How are signups trending this month?"
  - "Which platform drives the most sessions?"
- **funnel-doctor** — Claude uses this automatically for conversion questions.
  - "Where do users drop off during onboarding?"
  - "Build a checkout funnel and tell me what to fix first."
- **weekly-review** — produce a compact WoW report: WAU, signups, top-event deltas, notable movers, and one suggested action.
- **instrument-my-app** — Claude uses this automatically when you want to add analytics to code.
  - "Add MGM tracking to my Flutter app."
  - "What events should I track for this signup flow?"
- **audit-instrumentation** — verify event quality and debug missing or misleading data.
- **build-dashboard** — create saved queries and decision-focused dashboard widgets.
- **retention-cohorts** — build and interpret mature retention cohorts.
- **run-experiment** — plan, launch, monitor, and conclude MGM experiments.

MGM SDKs are available for Swift, Android, Flutter, JavaScript/TypeScript, React Native, and Capacitor.

The canonical skill source is
[`Mostly-Good-Metrics/skills`](https://github.com/Mostly-Good-Metrics/skills).
Those same skills can be installed directly into Codex, Claude Code, and other
compatible agents. This plugin mirrors them so Claude users receive the MCP
connection and skills in one install; changes should be made in the portable
skills repository first and then synchronized here.

## Codex and other agents

This plugin package is Claude-specific, but its skill content is not. Install
the portable repository for Codex:

```bash
npx skills add Mostly-Good-Metrics/skills --agent codex --global --yes
```

Then connect the MGM MCP endpoint in Codex and complete browser OAuth on the
first tool call. Full setup: [docs.mostlygoodmetrics.com/integrations/agent-skills](https://docs.mostlygoodmetrics.com/integrations/agent-skills).

## Docs

Full documentation: [docs.mostlygoodmetrics.com](https://docs.mostlygoodmetrics.com)

## License

MIT — see [LICENSE](./LICENSE).
