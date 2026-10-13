# Security & Repository Boundary

## Temporary public bootstrap

The Founder explicitly authorized committing the canonical agent bootstrap while this repository remains public to facilitate multi-agent intervention.

This includes:
- Soul;
- system prompt;
- policies;
- architecture;
- eval definitions;
- tool contracts;
- content seeds.

The repository should still be made PRIVATE when convenient.

## Never commit

Regardless of visibility:

- production credentials;
- API keys;
- WhatsApp session secrets;
- Evolution/Chatwoot/Typebot credentials;
- Hermes secrets;
- authentication cookies;
- database passwords;
- Vercel secrets;
- provider tokens;
- real user PII;
- private user images;
- real transcripts containing personal/sensitive data;
- exports/dumps from production;
- payment credentials.

## Historical pack

The preserved local v1 pack may be imported after a human check confirms it contains no secrets or real user data.

## Data separation

EspelhoMeu user data must remain isolated from other ventures and tenants.

Infrastructure reuse does not authorize data reuse.

## Logs

General observability must not contain:
- full intimate reflections;
- raw private images;
- credentials;
- CPF/email where not strictly required.

Use opaque references where possible.

## Incident rule

If a secret or private user content is committed:

1. treat it as exposed;
2. revoke/rotate where applicable;
3. remove it from the active branch/history as appropriate;
4. document the incident;
5. verify downstream caches/artifacts where relevant.
