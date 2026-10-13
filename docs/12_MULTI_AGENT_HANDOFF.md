# EspelhoMeu — Multi-Agent Handoff

## Purpose

Allow Helena, CODEX, Claude Code and other authorized agents to work without redefining EspelhoMeu independently.

## Canon hierarchy

Use this order:

1. Founder decisions / ratified venture decisions.
2. This repository `canon/`.
3. This repository `runtime/`.
4. EspelhoMeu product repo contracts.
5. AMF canonical content.
6. Implementation-specific notes.

If an older document conflicts with newer ratified canon, document the conflict rather than silently combining both.

## Role split

### Founder / PDG
- final product decisions;
- brand direction;
- commercial strategy;
- approval gates.

### Sofia / AVS venture governance
- venture coordination according to current organization model.

### Helena
- infrastructure;
- runtime inventory;
- secure configuration;
- WhatsApp/Evolution/Chatwoot coordination;
- deployment evidence;
- operational handoff;
- preservation.

Helena does not redefine Soul or product semantics independently.

### Engineering Lead / CODEX
- backend contracts;
- entitlements;
- product integration;
- APIs;
- tests;
- PRs.

### Claude Code / alternative engineering agents
May execute scoped implementation when assigned, using the same canon and GitHub as source of truth.

### AMF / editorial
- canonical product content;
- derivative content sources according to AMF governance.

### Psychology reviewer
Future professional review of:
- body-image language;
- vulnerability;
- dependency;
- crisis boundaries;
- motivational patterns.

## Branch discipline

Use separate branches/PRs for:
- canon;
- runtime;
- channels;
- memory;
- image capability;
- membership.

Do not mix production secrets into Git.

## Agent task template

Every implementation mission should state:

- repository;
- branch/base;
- objective;
- authoritative files;
- allowed modifications;
- forbidden modifications;
- acceptance tests;
- evidence required;
- merge authority.

## Decision log

Material semantic changes should record:
- decision;
- date;
- owner;
- reason;
- affected files;
- migration impact.

## No shadow prompts

Production must not accumulate hidden prompts in:
- n8n;
- Typebot;
- VPS files;
- Chatwoot automations;
- ad hoc environment variables

without a canonical reference here.

If a runtime-specific wrapper is required, document it and version it.
