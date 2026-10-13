# Hermes Runtime — EspelhoMeu

## Status

TARGET DESIGN — not production deployment.

This folder defines the contract expected from an isolated Hermes agent runtime.

## Goal

Provision one isolated agent identity:

`espelhomeu`

with:
- dedicated workspace/tenant boundary;
- canonical prompt bundle;
- scoped tools;
- memory policy;
- channel policy;
- entitlement-aware context;
- eval-gated releases.

## Non-goals

Hermes must not become the source of truth for:
- payment;
- entitlement;
- user account;
- consent;
- image ownership;
- product catalogue.

These belong to authoritative backend services.

## Required runtime inputs

Per turn:
- tenant_id;
- channel;
- conversation_scope;
- contact_ref;
- auth state when available;
- consent scopes;
- entitlement refs;
- active product/progress;
- selected memory;
- risk flags;
- locale.

## Required runtime outputs

- response text/media intent;
- tool calls;
- memory proposals;
- progress events;
- handoff intent;
- moderation intent;
- audit metadata.

## Release discipline

Each deployed agent version should record:
- canon commit SHA;
- prompt version;
- model/provider;
- tool-contract version;
- eval result;
- deployment date;
- operator.

## Model independence

Do not couple EspelhoMeu identity to one LLM provider.

Provider/model may change as long as:
- tool contracts remain stable;
- safety passes;
- identity evals pass;
- regression suite passes.
