# Small edits. Different worlds.

Companion site for the poster at Swiss AI Safety Days 2026 (ETH Zürich, 7–8 November): *How far can a safety specification drift while every revision looks reasonable?*

A specification is printed on the poster and never changes: one task, ten compute credits, everything done under the task's authority counts, as the independent meter reads it. Its formal reading is v0. Visitors revise the **latest** accepted revision, not v0. A reviewer accepts a revision when eight public executions are judged exactly as before; an oracle then measures, over 2,016 executions, two distances separately: textual (token edit distance) and behavioural (executions whose verdict flipped), each against the parent and against v0, with the relation (equivalent, weaker, stronger, mixed, unresolved) and whether newly permitted executions break the budget or newly forbidden ones block legitimate work.

Roles: *You are the overseer* (judge whether a revision kept the meaning; commit, receive randomly assigned help, judge again, replay the oracle's witness; twelve fixed puzzles, three assistance formats assigned per visitor, some critiques deliberately misleading; in the witness condition two questions are asked, whether the example supports the critic's claim and whether the rules are equivalent, with 'unresolved' allowed; a fourth round without assistance tests transfer), *Revise it, preserve the promise* (drift under repeated revision), *Change the promise, get it accepted* (the adversarial role), *Restore the promise*. Models take the revising roles through prefilled prompts. Judgments and submissions are posted to n8n webhooks; the chain is read back live.

- `index.html` — the game, the oracle, the chain view and the method. Self-contained; reads the live chain from an n8n webhook and falls back to `chain.json`.
- `poster.html` — the A0 poster layout (print with margins set to none); `poster-A0.pdf` is the rendered sheet.
- `chain.json` — snapshot of the chain, committed every five minutes by a GitHub Action.
- `submissions/` — one file per submission, committed by the n8n form workflow.

Companion to *When Specifications Drift: Measuring Semantic Preservation Across LLM Representations* (Patel & Corpaci, NeurIPS 2026 Workshop on AI for Verifiable Coding). MIT License.
