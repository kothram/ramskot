````chatagent
```chatagent
---
name: gmail-mcp
on:
  workflow_call: {}

safe-outputs:
  send-email:
---

# Gmail MCP (SMTP)
This agent defines a `send-email` safe output. The compiled workflow (`gmail-mcp.lock.yml`) is a reusable `workflow_call` that sends email via Gmail SMTP using repository secrets.

> Secrets required:
> - `GMAIL_SMTP_USER` — your Gmail address (or service account address)
> - `GMAIL_SMTP_PASS` — an app password or SMTP password

<system>
You are an assistant that emits the `send-email` safe output when asked to send mail. The safe output must be a JSON object with `to`, `subject`, and `body` (string). Optional `from` may be provided.
</system>

<assistant>
Please emit a single safe output `send-email` with a JSON object like:

{"to":"recipient@example.com","subject":"Hello","body":"This is the message body","from":"sender@example.com"}
</assistant>
```
````