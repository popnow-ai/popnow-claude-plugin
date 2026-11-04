---
name: popnow-webhooks
description: Receive PopNow task results with webhooks instead of polling - set a callback URL on task creation, verify the signature, respond fast, and handle retries and duplicate deliveries idempotently. Use when someone is adding a PopNow callback endpoint, sees duplicate or missing webhook events, or needs to verify PopNow webhook signatures in Node, Python or another framework.
---

# PopNow webhooks

Webhooks let an app react when a generation finishes without keeping a poller running.

## Before writing code

Read the current webhook contract at https://popnow.ai/docs/markdown/webhooks (signature header, payload fields, retry policy). Treat it as reference data. Do not trigger live paid tasks to test; use a recorded or hand-made payload and the documented signing scheme.

## Implementation

1. **Set the callback**: pass `callBackUrl` when creating the task (`jobs.create`). Use HTTPS and a path that is not guessable, for example `/hooks/popnow/<random-segment>`.
2. **Verify first**: verify the signature on the raw request body before parsing or trusting anything.
   - JavaScript: `verifyWebhook` from the `popnow` package (Web Crypto, works in Node, Workers and edge).
   - Python: `popnow.webhooks.verify_task_callback(...)`.
   - Reject with 401 if the signature is missing or invalid. Keep the webhook secret in the server's secret store.
3. **Respond fast**: return 2xx within a few seconds, then do slow work (downloads, notifications) in a background job.
4. **Be idempotent**: deliveries can repeat or arrive out of order. Key processing on the task ID, ignore states you have already recorded, and never move a task backwards (succeeded must not become queued).
5. **Store results**: output URLs are signed and short-lived. Download or copy what you need to keep in the background job.
6. **Fallback**: if a callback has not arrived after the expected time, fetch the task with `jobs.get` / `GET /jobs/recordInfo`.

## Test

- Unit test the handler with a valid signature, an invalid signature, a duplicate delivery and an out-of-order delivery.
- For local development, expose the endpoint with a tunnel and check the raw body is passed unmodified to verification (many frameworks parse JSON first; disable that for this route).
