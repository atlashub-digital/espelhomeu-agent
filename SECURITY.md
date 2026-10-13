# Security & Repository Boundary

## Current repository visibility

At bootstrap time this repository is **PUBLIC**.

This is not the intended final state for the operational EspelhoMeu agent repository.

Before adding production-sensitive agent assets, convert the repository to **PRIVATE**.

## Do not commit while public

- production system prompt;
- detailed safety routing prompt;
- private memory schema and fixtures;
- user data;
- transcripts;
- image references belonging to users;
- provider credentials;
- WhatsApp credentials;
- Evolution/Chatwoot/Typebot secrets;
- Hermes runtime IDs or secrets;
- production host/IP details;
- internal eval conversations containing sensitive material;
- preserved historical local agent pack if it contains operational details.

## Allowed public-safe material

- product vision;
- public persona principles;
- high-level safety principles;
- high-level architecture;
- avatar/voice creative direction;
- non-sensitive content seeds;
- channel experience descriptions.

## Production secrets

Secrets must live in an approved vault/environment mechanism, never in Git.

## Data separation

EspelhoMeu user data must remain isolated from other ventures and tenants.

Infrastructure reuse does not authorize data reuse.

## Incident rule

If any secret or private user content is committed:
1. treat it as exposed;
2. revoke/rotate where applicable;
3. remove it from current history as appropriate;
4. document the incident and remediation.
