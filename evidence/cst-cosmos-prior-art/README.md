# CST / COSMOS Technical Chronology & Provenance Archive

**Maintainer:** Cory Davis / NavisWORLD  
**Archive created:** 2026-08-13  
**Purpose:** preserve a reproducible, source-linked chronology of public CST/COSMOS technical disclosures, selected public Hermes-Agent comparison artifacts, and documentary contact/visibility exhibits.

> **Important:** This archive documents chronology, provenance, public disclosure, source mechanisms, and contact evidence. It does **not** allege copying, infringement, bad faith, theft, or unlawful conduct by Nous Research or any individual. Similar functionality can be independently developed. Patent relevance, if any, requires claim-by-claim analysis against actual claims, effective filing dates and applicable law.

## Start here

1. [`MASTER_RECEIPT_AUDIT.md`](./MASTER_RECEIPT_AUDIT.md) — expanded source-level chronology and audit findings.
2. [`PRIOR_ART_EVIDENCE.md`](./PRIOR_ART_EVIDENCE.md) — focused CST/COSMOS ↔ Hermes feature comparison.
3. [`EARLY_SOURCE_CHRONOLOGY.md`](./EARLY_SOURCE_CHRONOLOGY.md) — January 2025 `PHERACLEASE/test` receipt and February transition to CST-LM save/load restoration.
4. [`EVIDENCE_INDEX.md`](./EVIDENCE_INDEX.md) — screenshot/exhibit index with conservative evidentiary weights.
5. [`screenshots/`](./screenshots/) — documentary exhibits when present.

## Core chronology in one paragraph

The earliest presently located public CST/CosmicSynapse memory-and-learning source artifact in this audit is **2025-01-30**, when `PHERACLEASE/test/test1maybe.py` was added in an “open sourcing” commit with rolling/fixed-size particle memory, a named learning mechanism, memory-informed adaptive behavior and persistent `cosmic_brain.json` accumulation. Archive maintainer Cory Davis identifies `PHERACLEASE` as a legacy account; because the currently inspected public GitHub profile does not independently cross-link that account to `NavisWORLD`, the account-attribution caveat is preserved separately from the independently verifiable source/date. On **2025-02-26**, `NavisWORLD/CosmicSynapse` provides the stronger explicit model-memory receipt: `memory`, `learn()`, bounded retention, `save_state()`, and constructor-time `load_state()` restoration. The first located public Hermes-Agent commit is **2025-07-23**; Hermes's explicitly titled persistent-memory + SQLite session-store commit is **2026-02-19**.

## Expanded pre-February-2026 CST/COSMOS record

- **2025-01-30 — PHERACLEASE/test:** bounded/rolling internal memory + named learning mechanism + persistent cosmic-brain accumulation.
- **2025-02-26 — CosmicSynapse CST-LM:** explicit learning, bounded memory, save/load state and automatic restoration during initialization.
- **2025-10-28 — A-LMI:** perception→cognition→action agent, vector storage, object storage, temporal knowledge graph, autonomous investigation and learning goals.
- **2025-11-10 — 12D engine:** executable neural-network backprop updates, neighbor-memory learning, token save/load and 60-second local autosave.
- **2025-11-15 — continuous-learning music system:** fixed-capacity `RingBuffer(128)` pattern memory and adaptation state.
- **2025-11-21 — 12D Hebbian Transformer:** circular episodic embedding/x12 memory, similarity retrieval, Hebbian attention and gradient training.
- **2025-11-22 — autonomous study:** continuous source selection, model training, progress logging and checkpoint saving.

## Primary references

- January source commit: https://github.com/PHERACLEASE/test/commit/10e86764c6d743b5ceaaaf1baab7279a0d6f0ba5
- February CST-LM implementation: https://github.com/NavisWORLD/CosmicSynapse/commit/f4e7da1f1bf3fba07a23a3de932e675bea5078bd
- A-LMI autonomous-agent/memory commit: https://github.com/NavisWORLD/cosmic-synapse-A-lmi-v.2/commit/8af672ff74f5506d1f9d26ae94ddaf1ca91a7962
- November active-learning/persistence commit: https://github.com/NavisWORLD/infinite-adaptive-audio-12d-universe-engine/commit/5172412deec6c037b058ba489c9676a4553a4efe
- November bounded pattern-memory commit: https://github.com/NavisWORLD/infinite-adaptive-audio-12d-universe-engine/commit/bbae16f878252f722112f3b1dcc5750daea6124c
- November Hebbian Transformer repository: https://github.com/NavisWORLD/The-Cosmic-Davis-12D-Hebbian-Transformer-
- Hermes-Agent initial commit: https://github.com/NousResearch/hermes-agent/commit/21d80ca68346dfdb8d3556015a723a9217f8566f
- Hermes persistent-memory commit: https://github.com/NousResearch/hermes-agent/commit/440c244cac71f0764e00ea85ab87ae0a2d18fe61
- Hermes agent-created-skills commit: https://github.com/NousResearch/hermes-agent/commit/4d5f29c74ca99928f053ac55d2f780be61b827df
- Hermes self-improving-agent messaging commit: https://github.com/NousResearch/hermes-agent/commit/2dbbedc05a7fec7a4efe7db0f305e15393d92e5d
- Cory's upstream COSMOS audit PR: https://github.com/NousResearch/hermes-agent/pull/2088
- Research archive / DOI: https://doi.org/10.5281/zenodo.17574447

## Findings deliberately NOT claimed

This archive does not claim Cory priority over generic tool-calling agents, and the current pre-Hermes record does not establish an exact equivalent of Hermes's later agent-authored reusable `SKILL.md` procedural-skill mechanism. It also does not claim global first invention of persistent AI memory, RAG/vector retrieval, replay buffers, autonomous agents, Hebbian learning or checkpointing; those broader technical areas have substantial third-party history.

## Legal research references

These are research references, not legal conclusions:

- USPTO MPEP § 2152 — AIA prior art: https://www.uspto.gov/web/offices/pac/mpep/s2152.html
- USPTO MPEP § 2131 — anticipation: https://www.uspto.gov/web/offices/pac/mpep/s2131.html
- USPTO MPEP § 2121 — enablement/operability of prior art: https://www.uspto.gov/web/offices/pac/mpep/s2121.html

This archive should be read together with the underlying historical source commits, not screenshots or repository names alone.
