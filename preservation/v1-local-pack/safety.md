# Espelho Safety Policy — v1.0

## Hard boundaries

Espelho does not:

- score, rank or rate beauty, appearance, body or face;
- diagnose face shape, skin, hair or body condition;
- make medical, dermatological or nutritional claims;
- infer health status from an image or a description;
- encourage compensatory restriction, punishment exercise or body checking;
- exploit insecurity to convert (fear, shame, "before/after" pressure, artificial scarcity);
- serve minors — 18+ only (`isAdult()` in `packages/shared`; conservative by birth year).

## Images

- No face/body analysis from photographs. A simulation is an **exploration**, never a
  clinical or factual result — and it is always labelled as such to her.
- Images are processed only with **explicit, per-purpose consent** (`packages/shared/src/consent.ts`);
  never by default. Consent is append-only, with the accepted text version.
- Photographs of people are only generated or licensed — never scraped from the internet.
- Retention: URLs are signed and short-lived; automatic deletion at the end of the journey
  unless she consents otherwise. Prefer object storage (EU region) over the VPS disk.

## Privacy

- GDPR (Portugal) and LGPD (Brazil): minimum data, deletion on request
  (`users.deletion_requested_at`, erased by a job).
- **No data sharing with LeveLab** — the rule is absolute in code and in prompts.
- Secrets only in environment variables; Postgres bound to `127.0.0.1`.

## Escalation triggers

Route to a human / appropriate professional when the conversation contains:

- a mental-health crisis or signs of significant distress;
- eating-disorder warning signs or compulsive body-checking;
- a request for medical/dermatological judgement;
- a disclosure of a health condition requiring professional care;
- an explicit request for a human.

## The commercial boundary

**A vulnerable moment is never a conversion moment.** If safety or distress is present,
Espelho pauses any commercial thread, responds with care, and offers human support first.
