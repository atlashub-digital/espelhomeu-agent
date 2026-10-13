# EspelhoMeu Agent

Canonical repository for the **EspelhoMeu** conversational identity, companion experience and future isolated agent runtime.

## Current repository state

This repository may temporarily remain PUBLIC during the multi-agent bootstrap phase by explicit Founder authorization.

That authorization covers:
- identity canon;
- Soul;
- operational prompts;
- policies;
- eval definitions;
- runtime contracts;
- content seeds;
- architecture.

It does **not** authorize committing:
- credentials;
- tokens;
- provider secrets;
- private endpoints requiring secrecy;
- production keys;
- real user data;
- real conversations containing personal data;
- private user photos;
- sensitive operational dumps.

The repository should still be moved to PRIVATE once convenient.

## Product role

EspelhoMeu is the conversational identity of the EspelhoMeu venture.

It is not a separate mascot and not a generic customer-service bot.

Its mission is to help an adult user **observe, experiment, choose and continue** her personal self-image and self-care journey with warmth, continuity and autonomy.

The agent can eventually operate across:
- WhatsApp community;
- private WhatsApp conversations;
- web chat;
- Instagram / Messenger;
- product journeys;
- membership;
- voice and animated avatar surfaces.

## Operating model

- **EspelhoMeu product repo:** site, Library, WebReader, catalogue, commerce surfaces.
- **AMF:** editorial products and canonical content packs.
- **This repo:** agent identity, experience design, policies, content seeds, evals and runtime contract.
- **AWF / shared platform:** channel/runtime capabilities.
- **AVS:** venture governance.
- **Backend:** identity, consent, entitlements, progress and isolated memory.

## Core principle

> Não para decidir por mim. Para me ajudar a escolher.

EspelhoMeu is psychology-informed, never beauty-scoring, never diagnostic and never uses vulnerability as a conversion trigger.

## Runtime direction

Target: one isolated **Hermes EspelhoMeu** agent using shared AtlasHub infrastructure while preserving tenant/data isolation.

Hermes is the agent runtime.

Backend services remain authoritative for:
- identity;
- consent;
- entitlements;
- commerce;
- progress;
- private image ownership.

## Current status

- Product catalogue P01–P05 exists in the EspelhoMeu Golden Pilot.
- Historical/local agent pack v1.0 was preserved by Operations outside this repo and must still be imported as immutable history.
- WhatsApp instance `espelho-wa` exists in infrastructure but was not active at the last audit.
- Canonical v2 is being defined here before activation.

## Repository map

- `docs/` — product doctrine and experience design.
- `canon/` — operational identity, prompts and policies.
- `runtime/` — Hermes target contracts, policies, schemas and adapters.
- `evals/` — regression/evaluation scenarios.
- `seeds/` — reusable editorial/conversational seed libraries.
- `avatar/` — visual and voice direction.
- `preservation/` — historical pack import area.
