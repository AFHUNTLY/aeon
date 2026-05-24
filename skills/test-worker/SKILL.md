---
name: test-worker
description: A simple test worker that writes a heartbeat file
tags: ["test", "system"]
enabled: true
schedule: workflow_dispatch
---
# Test Worker

This skill writes a heartbeat timestamp to prove the worker system is functional.

## Actions
1. Write current timestamp to test-heartbeat.txt
2. Commit the file
3. Report success
