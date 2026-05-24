---
name: surplus-hello
description: Call Surplus AI and echo the response
tags: ["test"]
enabled: true
schedule: "workflow_dispatch"
---
# Surplus Hello World
Run the following command to test the Surplus API:
```bash
curl -s https://www.surplusintelligence.ai/api/inference/v1/chat/completions \
  -H "Authorization: Bearer $SURPLUS_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "claude-opus-4.6",
    "messages": [{"role": "user", "content": "Say hello and confirm you are working as part of AEON."}],
    "stream": false
  }' | jq -r '.choices[0].message.content'
