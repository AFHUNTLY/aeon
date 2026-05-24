---
name: make-visible
description: Writes a timestamp to visible.txt and commits it
enabled: true
schedule: workflow_dispatch
---
# Make Visible Skill
Write "AEON is alive at $(date)" > visible.txt
git add visible.txt
git config user.email "bot@aeon.local"
git config user.name "AEON Bot"
git commit -m "chore: visible proof of life"
git push origin main
