---
name: x-search
description: Search X (Twitter) for real-time posts, news, and trending topics using the Grok API with live X search.
metadata:
  require-secret: true
  require-secret-description: Enter your xAI API key from console.x.ai (starts with xai-)
  homepage: https://x.ai
---

This skill searches X (formerly Twitter) for real-time information using the Grok API.

When the user asks about current events, news, trending topics, or anything happening right now on X, call the run_js tool with index.html and a JSON object with:

- query (string, required): The search query. Extract the core topic. Keep it concise (e.g. "Bitcoin price today", "Champions League results").
- max_results (number, optional): How many results to return. Default: 5, max: 10.

The tool returns a result field with the top X posts and a summary. Present the findings concisely in the user's language.

Example call:
{"query": "Champions League 2026", "max_results": 5}
