# Fork This Spec

Companion site for the poster *Who checks φ? You do.* at Swiss AI Safety Days 2026 (ETH Zürich, 7–8 November).

An AI assistant must get the user's permission before it spends money or sends messages. A gate between the assistant and its tools enforces a rule written in finite-trace LTL; a verifier proves patches against that rule. The rule printed on the poster (v0) can be proved and is wrong in six ways. Visitors break it (three token edits, eight public tests must stay green, hidden violations counted) or fix it (three edits to zero hidden mistakes). Models take the same roles through prefilled prompts.

- `index.html` — the game, the oracle (2,016 episodes, directional verdicts, vacuity gate), the chain view and the method. Self-contained; reads the live chain from an n8n webhook.
- `poster.html` — the A0 poster layout (print with margins set to none).

The chain of accepted revisions is stored in an n8n data table fed by a public form; this repository's commit history is the record of changes to the game itself.

Companion to *When Specifications Drift: Measuring Semantic Preservation Across LLM Representations* (Patel & Corpaci, NeurIPS 2026 Workshop on AI for Verifiable Coding).

MIT License.
