# Secrets / PII Scan — preservation/v1-local-pack (G0 gate)

**Date:** 2026-10-13 · **Scanner:** regex sweep (automated) + manual read of all files · **Repo visibility:** PUBLIC → this scan is a mandatory pre-import gate.

## Scope

All 9 imported artefacts: soul.md, identity.md, system.md, safety.md, memory.md, handoff.md, prompt.pt-br.md, evals.md, schemas/espelho.agent.json.

## Patterns checked

- emails (any TLD)
- phone numbers (pt-PT +351 / pt-BR +55 formats, national formats)
- API keys/tokens: `sk-`, `ghp_`/`gho_`/`ghu_`/`ghs_`/`ghr_`, AWS `AKIA…`, Bearer tokens, URL-embedded credentials (`scheme://user:pass@`)
- keyword-adjacent assignments (`password|senha|secret|api_key|token = …`)
- PEM private key blocks
- client proper names (manual read — see below)

## Result

**0 findings. 0 blockers.**

- Emails: none (brand names LeveLab / EspelhoMeu / AVS appear, but no contact addresses; commit-message-only artefacts like `contact@lia.doctor` are NOT in this pack).
- Phone numbers: none.
- API keys / tokens / credentials: none of any pattern.
- Private key blocks: none.
- Client proper names: none. The pack speaks generically of "a cliente / a pessoa"; no real user names, identifiers or personal data appear.
- No quotes, testimonials or dated user examples that could identify a person.

## Conclusion

The pack is safe to publish in a public repository. The files were imported unmodified; future edits to `preservation/v1-local-pack/` are prohibited anyway (immutable evidence), so this gate result is stable.
