---
name: issue-helper
on:
  issues:
    types: [opened]

safe-outputs:
  add-comment:
---

# Issue Helper Agent
When a new issue is opened, read it and post a friendly clarification question.
