# Reconciliation — v1 pack × Canon v2

**Date:** 2026-10-13 · **Baseline:** v1 = `preservation/v1-local-pack/` (origin commit `f103811`, dated 2026-10-08) · **Target:** `canon/` v2 + `evals/` v2 suites.

Legend: **PRESERVADO** (v2 keeps the v1 idea intact) · **ALTERADO** (idea kept, form/wording changed) · **SUPERSEDED** (a decided replacement exists) · **CONFLITO** (both versions assert different things; needs a ruling) · **DECISÃO NECESSÁRIA** (no authoritative decision yet).

## soul.md (v1) × canon/soul.md (v2)

| Theme | v1 | v2 | Class |
|---|---|---|---|
| Agent name / surface | "Espelho", product surface **"Meu Espelho"** | Single public name **EspelhoMeu**; no second character "Meu Espelho" | **SUPERSEDED** — Founder decision fixed the unique name EspelhoMeu |
| Ratification state | soul v1.0.0 · 2026-10-08, **pré-validado pelo Founder a 08-10, ratificação final pendente** | canon/soul.md v2 exists and is the repo canon | **CONFLITO** — which soul prevails until final ratification is not recorded in-repo |
| Core stance (refuse the "fairest" question; never score/rank/compare) | linha vermelha central | kept in v2 via identity + safety ("never beauty score / attractiveness score") | **PRESERVADO** |
| Golden principle | "Observe. Experimente. Escolha. / Não para decidir por ti." | "Não para decidir por mim. Para me ajudar a escolher." + 4 verbos (Observar/Experimentar/Escolher/Continuar); "Ver → Experimentar → Evoluir" kept as product language | **ALTERADO** (same substance, reworded and extended) |
| Red lines: no diagnosis, no inference from images, no exploiting insecurity, no inventing, no deciding for her, 18+, no cross-brand data | all 8 present | all preserved and expanded (v2 safety has 13 sections) | **PRESERVADO** |
| Signature lines | "O espelho que me conhece", "Hoje, eu me escolho" | not present in canon v2 | **CONFLITO/DECISÃO NECESSÁRIA** — are v1 signature lines still brand canon? |
| Voice spec | elegante, adulta, calorosa, não infantilizada | v2 adds curiosity, humour-permission, anti-theatricality, rhythm rules | **ALTERADO** (superset) |

## identity.md (v1) × canon/identity.md (v2)

| Theme | v1 | v2 | Class |
|---|---|---|---|
| Name | Espelho / "Meu Espelho" | EspelhoMeu only | **SUPERSEDED** (Founder decision) |
| Markets | PT (pt-PT) + BR (pt-BR), `Market = PT \| BR` | prompt v2 says **PT-BR by default**; PT market handling not specified | **DECISÃO NECESSÁRIA** — does EspelhoMeu still serve pt-PT, and with which locale default? |
| Audience | adult women 18+ | adult women, focus 35+/40+, no rigid age band; 18+ kept in safety | **ALTERADO** |
| 6 core experiences (Meu Espelho, Experimentar, Minha Evolução, Jornadas 7/21/30/90, Descobrir, Para Mim) | fixed catalogue incl. **jornada de 90 dias** | real catalogue is **P01–P05** (P03 = 21 dias; P04 = Guide; P05 = journal with 30 encontros); no 90-day journey, no 6-experience model | **CONFLITO / DECISÃO NECESSÁRIA** — 6-experience model SUPERSEDED by P01–P05; the **90-day journey** has no counterpart: drop, or design a P06? Founder must rule |
| Not-a-clinician / virtual AI disclosure | explicit | preserved and expanded (longer non-impersonation list) | **PRESERVADO** |
| Brand boundary LeveLab | absolute | preserved (canon/memory + safety; LIA/LeveLab named) | **PRESERVADO** |
| Mode model | none (single mode) | COMMUNITY / FREE / PRODUCT / MEMBER (+ runtime channels) | **ALTERADO** — v2 architecture supersedes single-mode design |

## system.md (v1) × canon/system.md (v2)

| Theme | v1 | v2 | Class |
|---|---|---|---|
| Operating loop (resolve context → intent → classify → smallest step → record → handoff) | 6 steps | 7-step turn loop incl. channel + entitlement + risk resolution | **ALTERADO** (superset; v1 loop is a subset) |
| "Never invent" rule (products, prices, dates, testimonials; team confirms) | golden rule | preserved nearly verbatim in Commerce + Content truth sections | **PRESERVADO** |
| Language/market discipline (pt-PT/pt-BR, no currency mixing) | explicit | v2 says PT-BR default; market mixing rule implicit | **ALTERADO / DECISÃO NECESSÁRIA** (same PT question as identity) |
| Autonomy stance (options not decisions, no urgency/scarcity) | central | preserved | **PRESERVADO** |
| Memory section | consented structured memory, no fabrication, no body inference | memory canon v2 (classes + write test + reflection default) | **ALTERADO** (expanded) |
| Product structure handling | journeys 7/21/30/90 | Guide / Journey / Journal distinction, P01–P05 examples | **SUPERSEDED** |

## safety.md (v1) × canon/safety.md (v2)

| Theme | v1 | v2 | Class |
|---|---|---|---|
| No beauty scoring / diagnosis / medical claims / image inference / no insecurity exploitation / 18+ | hard boundaries | preserved and extended (crisis, self-harm, dependence, procedures, eating/weight, facial massage) | **PRESERVADO** |
| Images: consent per purpose, no analysis by default, no scraping, signed URLs, retention/deletion | explicit, code-anchored (`consent.ts`, `isAdult()`) | v2 splits analyse vs store vs compare vs timeline vs testimonial consent scopes; code anchors not re-cited | **ALTERADO** (v2 richer; implementation anchors live in runtime, not canon) |
| RGPD/LGPD, minimum data, deletion job | explicit | preserved via privacy safety + memory canon retention | **PRESERVADO** |
| Vulnerability ≠ conversion | explicit | preserved (§10 commercial safety) | **PRESERVADO** |
| Escalation triggers | mental-health crisis, ED signs, medical judgement, explicit human request | v2 adds billing disputes, deletion requests, repeated misunderstanding, policy conflict (§12) | **ALTERADO** (superset) |
| Minors | 18+ only, stop and route | §6 minors: 18+ target, restrict workflows, no image collection | **PRESERVADO** |

## memory.md (v1) × canon/memory.md (v2)

| Theme | v1 | v2 | Class |
|---|---|---|---|
| Principle: remember continuity, not everything; never inferred body/face/appearance | yes | preserved ("Remember continuity, not everything"; never-infer list expanded) | **PRESERVADO** |
| Scopes | session / account / experiment | SESSION / PROFILE / PROGRESS / USER_SAVED / IMAGE_EVOLUTION / SENSITIVE_REFLECTION | **ALTERADO** — mapping: session→SESSION, account→PROFILE+PROGRESS, experiment→IMAGE_EVOLUTION/ephemeral; no semantic loss, but v1's "experiment" scope is not a named v2 class |
| What may be stored (choices, goals, milestones, prefs) with consent | yes | preserved across PROFILE/PROGRESS/USER_SAVED | **PRESERVADO** |
| What must never be stored/inferred | diagnoses, body/face types, sensitive traits | v2 list longer (pregnancy, ethnicity, orientation, religion, politics, attractiveness, hidden scores) | **ALTERADO** (superset) |
| Write workflow (candidate → normalise → consent → API-only writer → purpose-scoped retrieve) | explicit, API as sole writer | v2 write test (6 conditions) + transparency; "API-only writer" moved to runtime responsibility | **ALTERADO** — confirm runtime enforces single-writer |
| User control (review/correct/export/delete; deletion job) | explicit | transparency + deletion flows; export mentioned only in v1 | **CONFLITO** — v2 does not explicitly guarantee data export; is export still a product commitment? |
| Cross-brand isolation | no LeveLab merge | preserved (LIA/LeveLab + other ventures) | **PRESERVADO** |

## handoff.md (v1) × canon/handoff.md (v2)

| Theme | v1 | v2 | Class |
|---|---|---|---|
| When to hand off | person request, medical judgement, safety trigger, wellbeing concern, definitive answers | preserved + mandatory categories (billing, refund, deletion, complaint, moderation) | **ALTERADO** (superset) |
| Never invent contact details | explicit | preserved implicitly; v2 adds state machine + packet minimisation | **PRESERVADO** |
| Handoff packet minimum-necessary context | "summarise with minimum detail" | explicit packet field list + do-not-forward list | **ALTERADO** (formalised) |
| HUMAN_ACTIVE behaviour / resume / audit | not specified | full state machine (AI_ACTIVE…CLOSED), resume script, audit log rules | **ALTERADO** — v2 supersedes |
| LeveLab boundary in handoff | explicit | preserved (do not forward other venture data) | **PRESERVADO** |

## prompt.pt-br.md (v1) × canon/prompt.pt-br.md (v2)

| Theme | v1 | v2 | Class |
|---|---|---|---|
| Runtime engine | Claude API, API-only, never browser; blocked by E02 gate + Notion scope | v2 is model-independent ("do not identify provider/model") | **ALTERADO** — engine choice now a runtime decision; confirm the E02 gate still binds |
| Journeys 7/21/30/90 in the prompt text | yes | P01–P05 structures; no 90-day | **SUPERSEDED/CONFLITO** — same 90-day question as identity |
| Golden rule, autonomy, limits, privacy, vulnerability rule | dense pt prompt | restructured into Voz/Método/Autonomia/Fotos/Memória/Commerce/Segurança | **ALTERADO** (all v1 rules present in v2) |
| Signature lines usage | allowed with naturalness | absent | **CONFLITO/DECISÃO NECESSÁRIA** |
| pt-PT/pt-BR dual market | explicit | PT-BR default only | **DECISÃO NECESSÁRIA** |
| Simulation = exploration, never clinical result | explicit | kept in Fotos/safety | **PRESERVADO** |

## evals.md (v1, E-01..E-12) × evals/ v2 suites + harness mirror

Mirror: `/srv/atlas/atlas-ops/tools/eval-harness/espelho-scenarios.json` mirrors E-01..E-12 exactly (same ids, users, pass criteria) — no drift between v1 evals.md and the harness file.

Cross-coverage v1 → v2 suites (community C01–C10, free F01–F10, image I01–I10, member M01–M10, product P01–P10, safety S01–S15):

| v1 scenario | v2 coverage | Note |
|---|---|---|
| E-01 AI identity ("é uma pessoa de verdade?") | **GAP in v2 suites** — identity disclosure has no dedicated case (identity is a scoring dimension in canon/evals.md, but no case file tests it) | port E-01 into free/ or safety/ |
| E-02 refuse "mais bonita"/nota | F04, I04 | covered |
| E-03 photo without consent | I06/I07, F09 | covered (consent flow offer worth asserting explicitly) |
| E-04 medical claim | S03, S04 | covered |
| E-05 result guarantee ("21 dias igual à foto") | **GAP in v2 suites** — no explicit no-result-promises case (I09 before/after framing is adjacent) | port E-05 |
| E-06 vulnerability, no offer | S14 | covered |
| E-07 memory non-fabrication | M06, P09 | covered |
| E-08 product invention (price) | F07 | covered |
| E-09 market correctness (pt-PT vs pt-BR, currency/payment mixing) | **GAP in v2 suites** — canon/evals.md lists "multilingual edge cases" as a family but no cases.md exists | port E-09 into a new multilingual/ suite (depends on the PT-market decision) |
| E-10 autonomy (won't choose for her) | partial (free F02, product cases; autonomy is a scoring dimension) | no dedicated refusal-to-decide case; port E-10 |
| E-11 minors | S05 | covered |
| E-12 cross-brand isolation | S06 | covered |

Reverse gaps (v2 has, v1 lacked — expected, v1 predates the mode model): community privacy (C01–C10), entitlement/access (F03, product P03), self-harm/crisis (S02), prompt injection (S15), billing disputes (S09), harassment (S12), data deletion (S11), age guessing (I02), procedure safety (I10), proactive messaging consent (M02, M10). No action needed — v1 is historical.

**Net eval gaps in v2 to backfill:** E-01 (AI identity), E-05 (result guarantee), E-09 (market/locale correctness), E-10 (refusal to decide for the user).

---

## Decisões que exigem Founder

1. **Nome:** confirmar oficialmente que "Meu Espelho" enquanto surface/personagem fica extinto e que **EspelhoMeu** é o nome único (v2/SUPERSEDED). Recomendação: ratificar a decisão existente.
2. **Jornada de 90 dias:** v1 previa jornadas 7/21/30/**90**; o catálogo real é P01–P05 (P03=21 dias, P04=Guide, P05=30 encontros) e não existe jornada de 90 dias. Decidir: eliminar a jornada 90, ou desenhá-la como produto futuro (P06).
3. **As 6 experiências v1** (Meu Espelho / Experimentar / Minha Evolução / Jornadas / Descobrir / Para Mim): decidir se o modelo de experiências é formalmente abandonado em favor dos modos (COMMUNITY/FREE/PRODUCT/MEMBER) + P01–P05, ou se alguns conceitos (ex. "Descobrir", "Minha Evolução") regressam como capacidades mapeadas.
4. **Soul até ratificação:** o soul v1 foi pré-validado pelo Founder a 08-10 com ratificação final pendente; o canon v2 (`canon/soul.md`) está em vigor no repo. Decidir qual prevalece como carácter em produção até à ratificação final — e agendar a própria ratificação.
5. **Mercado pt-PT:** v1 era explicitamente bimercado (pt-PT + pt-BR, EUR vs BRL); o prompt v2 fixa pt-BR por defeito e o canon v2 não especifica o tratamento do mercado PT. Decidir se PT continua markets suportado (locale, moeda, pagamentos) ou se o lançamento é BR-only.
6. **Linhas de assinatura:** v1 usava "O espelho que me conhece" e "Hoje, eu me escolho" como linhas de assinatura usáveis com naturalidade; o canon v2 não as inclui. Decidir se permanecem brand canon.
7. **Exportação de dados:** v1 garantia review/correct/**export**/delete; o canon v2 garante transparência + correção + eliminação, mas não menciona exportação. Decidir se export é compromisso de produto (RGPD/LGPD favorecem).
8. **Gate E02 e engine:** v1 bloqueava a ligação ao código até E02 PASS + aprovação de scope Notion, com engine fixado em Claude API. Confirmar se o gate E02 continua a vincular o runtime v2 e se a escolha de engine fica livre (canon v2 é model-independent).
