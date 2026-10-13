# Hermes Target Architecture — EspelhoMeu

## 1. Decision direction

EspelhoMeu should be designed as an **isolated Hermes agent identity** using shared AtlasHub channel/runtime capabilities.

This is preferable to a minimal:

`WhatsApp webhook → LLM API → response`

because the product requires:
- persistent identity;
- memory governance;
- tools;
- multi-channel continuity;
- entitlements;
- progress;
- image workflows;
- human handoff;
- evals;
- auditable execution.

## 2. Isolation principle

Hermes is the runtime platform.

**EspelhoMeu remains the tenant/product identity.**

Using Hermes does not authorize:
- cross-venture memory;
- shared customer data;
- LeveLab/LIA reads;
- unrestricted AWF staff access.

## 3. Conceptual flow

```text
Channel
  ↓
Channel Gateway
  ↓
Workspace / Tenant Resolver
  ↓
Contact / Identity Resolver
  ↓
Consent Resolver
  ↓
Entitlement Resolver
  ↓
EspelhoMeu Context Builder
  ↓
Hermes EspelhoMeu
  ├── Canon / Soul
  ├── Channel Policy
  ├── Safety Policy
  ├── Memory Policy
  ├── Content Tools
  ├── Progress Tools
  ├── Image Tools
  └── Commerce-safe tools
  ↓
Response Policy
  ↓
Channel Adapter
```

## 4. Runtime context

Each turn should receive only the context required for that turn.

Conceptual context envelope:

```text
tenant
channel
conversation_scope
contact_identity
consent_scopes
entitlements
available_products
active_product
progress
allowed_memory
recent_context
channel_policy
risk_state
```

Do not dump unrestricted user history into every request.

## 5. Tool domains

Future EspelhoMeu tools may include:

### Content
- list publications;
- resolve chapter/unit;
- fetch authorized excerpt;
- fetch public sample.

### Progress
- start product;
- complete unit;
- pause/resume;
- save milestone.

### Memory
- read allowed preference;
- propose/save memory with policy;
- forget/correct memory.

### Images
- upload private image;
- save Evolution entry;
- list user-approved timeline;
- compare selected images.

### Commerce
- list active offers;
- explain entitlements;
- start checkout via backend.

The agent should never directly manufacture entitlement.

### Human support
- request handoff;
- pause AI;
- resume AI.

## 6. Backend source of truth

Hermes should not become the database of record for:
- payment;
- entitlement;
- identity;
- consent;
- image ownership.

Those remain authoritative backend services.

Hermes may use runtime memory capabilities, but durable product state needs explicit contracts.

## 7. Channel strategy

Initial:
- WhatsApp.

Next:
- web chat;
- Instagram/Messenger.

Later:
- voice/avatar;
- proactive member experiences.

All channels must resolve to the same EspelhoMeu identity but may expose different capabilities.

## 8. WhatsApp community

Group context requires a restricted policy:
- no private memory;
- no entitlement disclosure;
- no automatic answer to every message;
- scheduled content allowed;
- direct mention/reply triggers allowed;
- DM handoff for personal context.

## 9. WhatsApp private

Private conversation can progressively enable:
- profile context;
- product access;
- progress;
- image timeline;
- membership features

according to consent and entitlement.

## 10. Memory architecture

Recommended separation:
- working/session memory;
- durable profile memory;
- progress state;
- explicit saved reflection;
- image evolution references;
- operational logs.

Do not treat raw transcript as automatically reusable memory.

## 11. Observability

Log:
- tool calls;
- policy decisions;
- channel;
- entitlement resolution result;
- handoff;
- message delivery state;
- errors.

Do not put sensitive free-text reflections or raw images into general-purpose logs.

## 12. Model independence

EspelhoMeu identity must not depend on one model provider.

The runtime may evolve between providers/models while preserving:
- canon;
- policies;
- evals;
- tool contracts.

## 13. Deployment gates

### G0 — Preserve
Preserve historical local pack and current infrastructure state.

### G1 — Canon
Approve identity, safety, memory, channels and avatar/voice.

### G2 — Private repository
Operational prompt/policies/evals may be committed.

### G3 — Hermes isolated runtime
Provision dedicated agent profile/workspace with tenant boundaries.

### G4 — WhatsApp DM
Connect `espelho-wa` and validate private conversation.

### G5 — Community
Enable group-mode policy and scheduled interventions.

### G6 — Entitlements
Connect product access/progress.

### G7 — Images
Enable private image intake and My Evolution.

### G8 — Membership
Enable recurring member capabilities.

No gate should silently imply the next one.
