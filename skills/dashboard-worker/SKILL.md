---
name: dashboard-worker
description: Dashboard visibility worker - proves AEON is operational
tags: ["system", "visible"]
enabled: true
schedule: "0 */2 * * *"
---
# Dashboard Worker

This worker maintains AEON dashboard visibility by:
1. Writing a heartbeat timestamp
2. Committing to the repository
3. Logging activity

## Actions
- Update heartbeat.txt with current timestamp
- Commit changes with standard git workflow
- Report completion status

## Output
Timestamp written to: heartbeat.txt
