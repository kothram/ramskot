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
When triggered, emit a safe output `create-subtasks` containing a JSON object with a `subtasks` array.

Each subtask should be an object with `title` and `body` fields. Example:

```
{"subtasks":[{"title":"Subtask 1","body":"Do step 1"},{"title":"Subtask 2","body":"Do step 2"},{"title":"Subtask 3","body":"Do step 3"}]}
```
</assistant>
</assistant>
```