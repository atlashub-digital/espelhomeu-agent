# Historical Agent Pack Preservation

Operations reported an historical/local EspelhoMeu agent pack containing:

- soul.md
- identity.md
- system.md
- safety.md
- memory.md
- handoff.md
- prompt.pt-br.md
- evals.md

The pack was found only in a local clone on branch `feat/agente-espelho-v1` and was preserved by Operations outside this repository, including a git bundle.

## Rule

Do not recreate or overwrite that package from memory.

When this repository is PRIVATE:

1. import the preserved v1 package under a clearly versioned historical location;
2. keep it immutable as evidence;
3. reconcile it against the new canonical docs;
4. create the next operational canon as a new version;
5. document all semantic changes.

Suggested location after privacy gate:

`preservation/v1-local-pack/`

The historical pack is evidence and source material, not automatically the production configuration.
