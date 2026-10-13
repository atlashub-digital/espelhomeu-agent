# EspelhoMeu Agent — Implementation Roadmap

## Phase 0 — Canon & preservation

Status: in progress.

Deliver:
- canonical docs;
- operational canon;
- eval suites;
- runtime target contracts;
- avatar direction;
- historical v1 preservation/import.

Gate:
Founder/venture review.

## Phase 1 — Hermes isolated agent

Deliver:
- isolated Hermes workspace/profile;
- canon bundle loaded;
- model/provider config;
- tool stubs;
- observability;
- no production user access.

Gate:
internal chat tests + eval pass.

## Phase 2 — WhatsApp private MVP

Use:
- espelho-wa instance after connectivity is fixed;
- private test numbers only.

Deliver:
- inbound normalization;
- DM/private mode;
- identity/contact resolver;
- no premium memory initially;
- human handoff;
- audit logs.

Gate:
internal staff smoke.

## Phase 3 — Free DM

Deliver:
- public/free content;
- samples;
- lightweight preferences;
- catalogue explanation;
- no payment dependency for first launch.

Gate:
limited pilot.

## Phase 4 — Product entitlement companion

Depends on:
- Commerce/Entitlement backend from EspelhoMeu SALES READY.

Deliver:
- entitlement resolver;
- product-aware content tools;
- Reader deep links;
- progress;
- resume;
- milestones.

Gate:
P01–P05 matrix tests.

## Phase 5 — Community Mode

Deliver:
- controlled WhatsApp group;
- mention/reply triggers;
- scheduled content;
- moderation;
- DM transition;
- anti-loop/rate limits.

Gate:
community pilot.

## Phase 6 — My Evolution images

Deliver:
- explicit consent;
- private storage;
- image intake;
- save/delete;
- compare selected entries;
- safe image eval suite.

Gate:
privacy/security review.

## Phase 7 — Membership

Deliver:
- recurring entitlement;
- richer memory;
- check-ins;
- evolution timeline;
- new member content;
- notification preferences;
- cancellation behavior.

Gate:
retention pilot.

## Phase 8 — Social channels

Deliver:
- Instagram/Messenger adapters;
- public/private policy separation;
- same identity.

## Phase 9 — Voice/avatar

Deliver:
- approved voice;
- approved avatar master;
- short audio;
- talking avatar clips;
- controlled generated media.

## Production invariants

Never skip:
- tenant isolation;
- entitlement authority;
- consent;
- handoff;
- eval regression;
- secret hygiene.
