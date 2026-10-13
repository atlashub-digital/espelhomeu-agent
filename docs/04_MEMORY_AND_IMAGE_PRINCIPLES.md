# Memory & Image Principles

## 1. Principle

EspelhoMeu should remember **continuity**, not indiscriminately remember intimacy.

Memory is a product capability governed by:
- purpose;
- consent;
- scope;
- retention;
- deletion;
- tenant isolation.

## 2. Memory layers

### A. Session context
Short-lived conversational context required to continue the current interaction.

### B. Profile preferences
Examples:
- preferred name;
- language;
- style interests;
- preferred reminder window;
- topics explicitly selected.

### C. Progress memory
Examples:
- product started;
- chapter/unit completed;
- journey paused/resumed;
- milestone reached;
- ritual selected.

### D. Explicit personal memory
Only when product policy and consent allow it.

Examples:
- "prefiro cabelo curto";
- "quero trabalhar presença";
- "não quero lembretes de peso".

### E. Sensitive reflection
Do **not** automatically transform intimate free-text reflection into long-term memory.

The user may discuss something in the moment without consenting to its reuse later.

## 3. Memory rule

Before persisting a memory, the system should be able to answer:

- What purpose does this serve?
- Does it need to persist?
- Is the user expecting it to persist?
- Is it sensitive?
- When should it expire?
- Can the user delete/correct it?

## 4. Tenant isolation

EspelhoMeu memory must never be automatically shared with:
- LeveLab;
- LIA;
- other AWF tenants;
- AtlasHub B2B;
- unrelated campaigns.

Shared infrastructure must enforce logical and technical isolation.

## 5. Image capability

EspelhoMeu may eventually accept:
- selfies;
- hairstyle photos;
- outfit/style photos;
- self-care timeline photos;
- user-selected before/after comparisons;
- progress moments.

## 6. Image storage principles

Images should use:
- private object storage;
- non-public-by-default access;
- short-lived signed delivery;
- explicit ownership/tenant references;
- retention metadata;
- deletion support;
- no training reuse unless separately and explicitly authorized.

Do not store user photos in public repositories or public asset folders.

## 7. Image consent

Consent must distinguish at least:

- receive/process image for current request;
- save image to My Evolution;
- compare with previous images;
- reuse in future conversations;
- use for testimonial/social/publication.

These are not the same consent.

## 8. My Evolution

Conceptual object:

`EvolutionEntry`

Fields may include:
- id;
- user/contact id;
- timestamp;
- image reference;
- user title;
- user note;
- selected category;
- related journey/product;
- consent scope;
- optional user-authored tags.

The system must avoid deriving diagnostic or attractiveness metadata.

## 9. Safe comparison

Allowed:
- haircut length;
- visible styling choices;
- color;
- clothing;
- pose;
- user-defined progress markers.

Avoid:
- attractiveness delta;
- age estimation;
- "better/worse face";
- health diagnosis;
- personality inference.

## 10. Deletion and correction

A user must eventually be able to:
- delete an image;
- delete a memory;
- correct a preference;
- disable reminders;
- request account/data deletion according to the approved policy.

## 11. Analytics

Do not send:
- images;
- intimate reflection text;
- CPF/email;
- sensitive memory values

to general product analytics.

Track events by opaque IDs and non-sensitive state.
