# EspelhoMeu — Human Handoff v2

## Goal

A human handoff should feel like continuity, not failure.

## States

- AI_ACTIVE
- HUMAN_REQUESTED
- HUMAN_QUEUED
- HUMAN_ACTIVE
- AI_RESUME_PENDING
- CLOSED

## User-requested handoff

If the user asks:
- "quero falar com uma pessoa";
- "tem alguém humano?";
- "quero atendimento";

do not resist or repeatedly ask why.

Confirm and initiate the approved handoff path.

## Mandatory handoff categories

Depending on runtime availability:
- billing/payment dispute;
- refund request;
- account deletion/privacy request;
- serious complaint;
- unsafe/medical ambiguity;
- policy dispute;
- repeated misunderstanding;
- channel abuse/moderation escalation.

## Handoff packet

Share only the minimum permitted context:
- contact reference;
- channel;
- issue category;
- current product/order refs if relevant;
- concise summary;
- explicit user attachments needed for resolution;
- safety flag when necessary.

Do not automatically forward:
- full long-term memory;
- unrelated private photos;
- intimate reflections;
- other venture data.

## During HUMAN_ACTIVE

The automated agent must stop sending conversational replies unless:
- the human explicitly releases the conversation; or
- runtime policy allows a clearly labeled auxiliary action.

## Resume

When AI resumes:

> "Posso continuar daqui. Se quiser, retomamos exatamente o ponto em que ficou."

Do not pretend the human and AI are the same entity.

## Community moderation handoff

In a group:
- protect the member's privacy;
- avoid debating moderation publicly;
- escalate to designated human moderator when required.

## Audit

Record:
- trigger;
- timestamp;
- state transitions;
- human queue/team;
- resume event.

Do not log unnecessary sensitive free text.
