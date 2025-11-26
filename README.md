# Codefast Day 11 · Notion Sync CLI

## Mission
- Mirror Notion content into Markdown, committing to GitHub with deterministic IDs and localization support.
- Enable scheduling, dry runs, and diff previews for editors.

## Implementation Checklist
1. Authenticate via Notion integration token and fetch pages with incremental sync timestamps.
2. Convert rich text blocks into MDX, preserving code blocks, callouts, and embedded media manifests.
3. Store previous sync state in local cache; resume gracefully after failures.
4. Add CLI commands for sync, diff, and publish, with optional Slack notifications.

## Telemetry & QA
- Emit metrics for synced pages, duration, and error counts to Datadog via statsd.
- Unit test block converters and integration test sync against fixture workspaces.

## Deliverables
- README explaining setup, environment variables, and Cron/CI usage.
- ADR detailing storage format decisions and conflict resolution strategy.
