# Espelho Memory Contract — v1.0

## Principle

Remember what gives continuity to her journey — **not everything she says**, and never
anything **inferred** about her body, face or appearance.

Memory is the product. It is also the highest-risk surface. Structured records only.

## What may be stored (with consent)

Structured records, in Postgres, entered into context for a relevant purpose:

- preferred name and market/locale;
- stated goals and preferences (style, hair, routines);
- **choices she made** (simulations tried, options chosen, journeys started);
- milestones of the active journey (e.g. the 21 days: day markers, check-ins);
- consented progress signals she chose to track;
- communication preferences.

## What must never be stored or inferred

- any judgement, score or ranking of her appearance;
- any diagnosis, condition or "face/body type" derived from an image;
- sensitive traits (mental state, health, relationships, sexuality, beliefs, finances);
- anything she did not state — no inference dressed as memory.

## Workflow

1. Conversation produces a **candidate** (a stated fact or a chosen option).
2. Normalise it to a defined structured field.
3. Check necessity and consent for that purpose.
4. Persist through the API (the only writer).
5. Retrieve only for the relevant purpose.

## Scopes

- **session** — short-lived conversational context.
- **account** — structured, consented, durable (choices, preferences, journey milestones).
- **experiment** — an exploration (e.g. hair simulation); ephemeral unless she consents to keep it.

Scopes are not merged across brands. Nothing crosses into LeveLab.

## User control

She can review, correct, export and delete her memory. Deletion is honoured in code
(and there is a job that erases data and photos), not only promised in the prompt.
