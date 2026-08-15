---
format: 0
requires: []
---

# language — language-learning base node

A bare DAFNE node: no memory, therefore not a grove. One parent:
`parents/deck`.

Method for building a language deck: leveling/frequency/grammar tagging
taxonomy, plus pedagogy notes on card-format choices.

| File | What |
|---|---|
| `./language-defaults.md` | Entry point: splices deck base + language tagging taxonomy |
| `./production_vs_comprehension.md` | L1→L2 vs L2→L2 card-format analysis |
| `./creative-usages.md` | Ideas for AI reasoning over a full deck |
| `./queue-policy.md` | Post-add scheduling rules — deliberately **not** `#include`d into any deck spec, read directly instead |

`requires: []` here is correct even though `deck` requires `anki` — the
engine unions `requires:` up the parent tree (`manifest.py:effective_requires`),
so consumers of `language` see `{anki}` without this node re-declaring it.
