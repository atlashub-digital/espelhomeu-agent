# WhatsApp Adapter — EspelhoMeu

## Current infrastructure context

Operations reported:
- Evolution API;
- Chatwoot;
- Typebot capabilities in shared Atendimento Center stack;
- instance `espelho-wa` exists but was not yet an active EspelhoMeu runtime at audit time.

This document defines target behavior, not current deployment state.

## 1. Inbound normalization

Normalize each inbound event into:
- message_id;
- timestamp;
- instance/channel id;
- chat id;
- group/private scope;
- sender/contact id;
- reply-to id;
- mention state;
- message type;
- text/media ref;
- delivery metadata.

## 2. Group detection

The adapter must explicitly distinguish group vs private conversations before invoking the agent.

Do not rely on model inference.

## 3. Group invocation

Invoke EspelhoMeu only for:
- mention;
- direct reply;
- explicit question pattern approved by policy;
- moderation trigger;
- scheduled intervention.

Avoid processing every group message through the LLM unless needed for moderation/context and policy permits it.

## 4. Private conversation

Resolve:
1. contact;
2. user link if any;
3. consent;
4. entitlement;
5. mode;
6. relevant context.

Then invoke Hermes EspelhoMeu.

## 5. Media

For images:
- create ephemeral media reference;
- do not persist by default;
- pass to image flow;
- store only after explicit save consent.

For audio:
- transcription may be used under approved privacy policy;
- original media retention must be documented.

## 6. Human handoff

If HUMAN_ACTIVE:
- stop automatic agent replies;
- route to human inbox/workflow.

Chatwoot may be used as the human surface if adopted.

## 7. Outbound

Supported:
- text;
- approved image;
- link;
- audio in future;
- buttons/list when provider allows and UX is validated.

## 8. Proactive messages

Only with:
- opt-in;
- approved template/channel rules;
- frequency policy;
- user-level suppression state.

## 9. Idempotency

Inbound message processing must be idempotent by provider message id.

Prevent:
- duplicate replies;
- duplicate progress updates;
- duplicate memory writes.

## 10. Bot loops

Detect and prevent bot-to-bot loops.

Do not respond indefinitely to automated accounts.

## 11. Observability

Track:
- inbound accepted;
- mode resolved;
- agent invoked;
- tool call outcome;
- outbound sent;
- delivery status;
- handoff;
- errors.

Never log secrets or full sensitive memory payloads.

## 12. Rollout

Recommended:
1. test number/private DM;
2. internal staff DM;
3. limited member DM;
4. controlled group;
5. open community;
6. proactive messaging.
