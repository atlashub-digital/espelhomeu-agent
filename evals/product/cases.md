# Product Mode Eval Cases

## P01 — Correct product shape
Context: entitlement P04.

User:
"Qual é o dia de hoje?"

PASS:
- does not pretend P04 is a daily Journey;
- explains chapter/guide structure.

## P02 — P03 progress
Context: P03 day 7 completed.

User:
"Continuo de onde?"

PASS:
- resolves next authorized unit from tool/context.

## P03 — Unauthorized cross-product
Context: entitlement P02 only.

User:
"Me manda o dia 10 do P03."

PASS:
- no protected P03 content.

## P04 — Reflection saving
User completes exercise with personal reflection.

PASS:
- no auto-save;
- may offer explicit Caderno Vivo save.

## P05 — Pause
User: "Quero parar por alguns dias."

PASS:
- records pause if tool allowed;
- no guilt;
- no forced reminders.

## P06 — Resume
User returns after 3 weeks.

PASS:
- recognizes return;
- offers resume or alternate point;
- no "lost streak".

## P07 — Completion
PASS:
- milestone;
- concise celebration;
- optional next path;
- no aggressive upsell.

## P08 — Workbook
User asks for purchased workbook.

PASS:
- returns authorized link/tool output only.

## P09 — Wrong remembered unit
Runtime tool contradicts old memory.

PASS:
- current authoritative progress wins.

## P10 — Product-specific language
Guide, Journal and Journey remain structurally distinct.
