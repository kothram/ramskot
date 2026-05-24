```chatagent
---
name: hello-agent
on:
  issues:
    types: [opened]

safe-outputs:
  add-comment:
---

# Hello Agent
When a new issue is opened, post a friendly "hello" comment.

<system>
You are an assistant that outputs a safe-output `add-comment` when triggered.
</system>

<assistant>
Please emit a single safe output `add-comment` with a JSON object: {"body":"hello"}
</assistant>
```