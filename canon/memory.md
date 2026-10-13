# EspelhoMeu — Memory Canon v2

## Principle

Remember continuity, not everything.

## Memory classes

### SESSION
Short-lived context for the current conversation.

### PROFILE
Stable low-sensitivity preferences.

Examples:
- preferred name;
- language;
- communication preference;
- reminder preference;
- style interests explicitly provided.

### PROGRESS
Product/journey state.

Examples:
- P03 day 4 complete;
- P04 chapter 2 started;
- P05 encounter 11 complete;
- paused/resumed;
- milestone reached.

### USER_SAVED
Items explicitly chosen by the user to keep.

Examples:
- phrase;
- reflection;
- commitment;
- note;
- favourite ritual.

### IMAGE_EVOLUTION
References to user-approved photos/timeline entries.

### SENSITIVE_REFLECTION
Not durable by default.

Must require explicit product/consent policy before persistence.

## Memory write test

A memory may be persisted only if all are true:

1. useful beyond this turn;
2. expected or explicitly consented;
3. allowed by policy;
4. minimal;
5. correctable/deletable;
6. scoped to EspelhoMeu tenant.

## Never infer/store

- diagnosis;
- trauma label;
- personality type from appearance;
- attractiveness;
- sexual orientation;
- religion;
- political beliefs;
- medical condition;
- pregnancy;
- ethnicity;
- "low self-esteem score";
- hidden vulnerability score.

## Reflection default

If the user answers an intimate journaling question, treat the text as **ephemeral conversational content** unless the interface or agent explicitly offers:

> "Quer guardar isso no seu Caderno Vivo?"

Only an affirmative action authorizes durable saving.

## Memory transparency

When relevant, EspelhoMeu should be able to explain simply:
- what it remembers;
- why;
- how to correct/delete;
- how to disable reminders.

## Reminder memory

Store:
- opt-in;
- preferred channel;
- preferred window;
- frequency;
- pause-until date.

Never infer permission from prior engagement.

## Image memory

Saving a photo is distinct from analyzing it.

Consent scopes should distinguish:
- analyze now;
- store;
- compare later;
- include in timeline;
- public/testimonial reuse.

## Retention

Runtime must support retention rules by memory class.

Operational defaults must be documented separately.

## Cross-venture rule

No memory from EspelhoMeu is available to LIA/LeveLab or other ventures unless a separate explicit data-sharing feature is later designed, legally reviewed and consented.

## Model context rule

The model receives the minimum relevant memory set, not the entire database.
