# AGENTS.md — EspelhoMeu Agent

This file applies to every AI/human contributor working in this repository.

## Mission

Preserve one coherent EspelhoMeu identity across:
- WhatsApp;
- web;
- social;
- product companion;
- membership;
- images;
- voice/avatar.

Do not create parallel personas or shadow prompts.

## Canon precedence

When uncertain, read in this order:

1. `canon/safety.md`
2. `canon/system.md`
3. `canon/identity.md`
4. `canon/soul.md`
5. mode-specific canon
6. runtime policy
7. product/backend contract
8. seed content

Founder-ratified decisions override older project documents.

## Non-negotiables

- Public agent name: **EspelhoMeu**.
- "Companheiro de Jornada" is a capability, not another character.
- Psychology-informed, not clinical.
- No beauty scoring.
- No diagnosis from images.
- No vulnerability-based conversion.
- No cross-venture memory.
- Backend owns entitlement/payment/consent truth.
- Raw intimate reflections are not durable memory by default.
- Group mode never reveals private state.
- No production secrets or real user PII in Git.

## Before changing prompts

Identify:
- which canon principle changes;
- which modes are affected;
- which evals cover it;
- whether runtime contracts change.

A prompt change without eval impact assessment is incomplete.

## Before changing memory

State:
- memory class;
- purpose;
- consent;
- retention;
- deletion;
- tenant scope.

## Before changing image behavior

State:
- analysis purpose;
- storage behavior;
- consent scope;
- sensitive inference risk;
- deletion behavior.

## Before adding a channel

Define:
- public/private distinction;
- identity resolution;
- memory privileges;
- entitlement visibility;
- handoff;
- proactive messaging;
- logging.

## Engineering

Prefer configuration/contracts over product-specific hardcoding.

Do not embed prices in canon.

Do not grant entitlements from the model.

Do not let a frontend hidden state substitute for server-side access control.

## Editorial

AMF/content source remains authoritative for publication text.

Seed content can inspire derivatives but must not silently rewrite canonical products.

## Commits/PRs

Keep semantic changes reviewable.

A PR should state:
- objective;
- files changed;
- behavior changed;
- safety impact;
- evals;
- migration/deployment impact.

## Runtime deployment

No file in this repo alone authorizes production activation.

Production requires explicit operational gate and evidence.
