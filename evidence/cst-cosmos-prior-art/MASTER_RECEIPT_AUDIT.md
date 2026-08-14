# Master Source Receipt Audit

**Last updated:** 2026-08-13  
**Purpose:** preserve a conservative, reproducible chronology of CST/COSMOS technical artifacts and selected public Hermes-Agent comparison artifacts.

> This is a technical chronology. It does not allege copying, derivation, infringement, bad faith or unlawful conduct. Similar systems can be independently developed. Broad AI-memory, retrieval, world-model, autonomous-agent, replay-buffer, checkpointing and Hebbian concepts have substantial third-party history outside these repositories.

## Audit rules

A row receives strong weight only when the relevant mechanism can be tied to a platform-native timestamp and inspected source or commit diff.

The audit now keeps five clocks/boundaries separate:

1. repository creation date;
2. commit timestamp;
3. first commit where the actual mechanism is inspectable;
4. actual commit/file authorship and upstream ancestry;
5. later moves/imports/reorganizations that could create false chronology.

Repository names, README claims, filenames, screenshots, current archive paths and later-imported history are not substitutes for historical source.

## Corrected chronology

| Date | Public artifact | Mechanism actually supported | Audit result |
|---|---|---|---|
| **2025-01-30** | `PHERACLEASE/test` commit `10e86764c6d743b5ceaaaf1baab7279a0d6f0ba5` | rolling/fixed-size particle memory; named learning mechanism; memory-informed adaptive behavior; persistent `cosmic_brain.json` accumulation | **Earliest located CST/CosmicSynapse memory-and-learning source artifact in this audit.** Account attribution to Cory is stated by the maintainer; public profile metadata did not independently cross-link the legacy account. |
| **2025-02-26** | `NavisWORLD/CosmicSynapse` commit `f4e7da1f1bf3fba07a23a3de932e675bea5078bd` | `memory`; explicit `learn()`; bounded retention; `save_state()`; constructor-time `load_state()`; larger state/history persistence | **Strongest early receipt for explicit automatic save/load restoration of AI model memory across executions.** |
| **2025-05-21** | `NavisWORLD/The-theory-of-CST` commit `b96a56501cb447cb68e2683915d22024a0c526dd` | evolving simulated entity/world state; audio/sensory input; Python-to-Unity state bridge; procedural environment generation; timestamped/token-oriented logging | **Newly added key receipt for Cory's persistent world-state / sensory-environment lineage. Not a global-first world-model claim.** |
| **2025-07-23** | `NousResearch/hermes-agent` initial commit `21d80ca68346dfdb8d3556015a723a9217f8566f` | real tool-calling agent; caller-supplied conversation history | **No Cory-priority claim for generic tool calling.** |
| **2025-10-28 02:21:23Z** | `NavisWORLD/cosmic-synapse-A-lmi` commit `527cd7084d25c40275af77b5b7a5397a31ed6179` | web/audio perception; Milvus vector memory; MinIO object storage; Neo4j graph memory; knowledge-gap discovery; hypothesis generation; action/experiment planning; closed learning loop | **Primary A-LMI receipt. Earlier than the v2 receipt previously used by the archive.** |
| **2025-10-28 17:05:40Z** | `NavisWORLD/cosmic-synapse-A-lmi-v.2` commit `8af672ff74f5506d1f9d26ae94ddaf1ca91a7962` | perception->cognition->action loop; vector/object/graph stores; reasoning triggers; hypothesis-driven investigation; learning-goal handling | **Strong same-day expansion receipt, no longer treated as the first A-LMI anchor.** |
| **2025-11-10** | `NavisWORLD/infinite-adaptive-audio-12d-universe-engine` commit `5172412deec6c037b058ba489c9676a4553a4efe` | neural forward/backward weight updates; neighbor-memory learning; localStorage token save/load; startup loading; 60-second persistence | **Strong executable learning + persistence receipt.** |
| **2025-11-15 21:13:25Z** | same repository, commit `bbae16f878252f722112f3b1dcc5750daea6124c` | `RingBuffer(128)` pattern memory; continuous learning system; retained successful patterns; confidence/adaptation state | **Strong bounded continuous-learning/pattern-memory receipt. Timestamp corrected to GitHub's 21:13:25Z record.** |
| **2025-11-21** | `NavisWORLD/The-Cosmic-Davis-12D-Hebbian-Transformer-`, historical transformer source | fixed-size circular episodic memory of embeddings/x12 state; semantic + adaptive similarity retrieval; Hebbian attention; gradient training | **Strong executable memory-augmented transformer receipt. In-process retrieval is not used as the strongest cross-restart proof.** |
| **2025-11-22** | same repository, `autonomous_study.py` commit `dd70bc60faf841a51bfbc9dac1014e0462d45658` | continuous self-directed study; curriculum/source selection; repeated model training; logs; checkpoints | **Strong autonomous-training/self-directed-study receipt. Not asserted as exact pre-Hermes self-writing procedural skills.** |
| **2026-02-19** | `NousResearch/hermes-agent` commit `440c244cac71f0764e00ea85ab87ae0a2d18fe61` | explicit persistent MEMORY/USER stores; bounded curated memory; session/startup injection; SQLite store; FTS5 search; linked sessions | **Feature-specific Hermes persistent-memory implementation.** |
| **2026-02-20** | Hermes commit `4d5f29c74ca99928f053ac55d2f780be61b827df` | agent creates/updates/deletes reusable skills, described as procedural memory | **Exact pre-Hermes CST equivalent of agent-authored `SKILL.md` procedural skills not established.** |
| **2026-02-28** | `NavisWORLD/The-Cosmic-Davis-12D-Hebbian-Transformer-ver.4.2` | later dynamic-state/COSMOS integration and benchmark surface with imported third-party/Farnsworth commit ancestry | **Mixed-lineage repository. Not used as a clean 2025 priority anchor.** |
| **2026-02-28** | `NavisWORLD/Cosmos` | later COSMOS integration/consolidation with identifiable Farnsworth ancestry plus Cory additions | **Mixed-lineage repository. File/commit-level attribution required.** |
| **2026-03-06** | Hermes commit `2dbbedc05a7fec7a4efe7db0f305e15393d92e5d` | public “self-improving AI agent” positioning around learning loop, skills, memory and session search | **Documentation/positioning chronology; weaker than executable source.** |
| **2026-03-19** | `NousResearch/hermes-agent#2088` | Cory/NavisWORLD submits sanitized COSMOS project for audit review | **Direct submission/contact chronology. It occurs after Hermes's Feb. 19/20 commits and cannot establish access for those earlier features.** |

---

# Detailed receipts

## January 30, 2025 - PHERACLEASE/test

Commit: https://github.com/PHERACLEASE/test/commit/10e86764c6d743b5ceaaaf1baab7279a0d6f0ba5

Historical `test1maybe.py` contains a named `LearningMechanism`, rolling memory updates with `np.roll(...)`, writes of normalized frequency features into retained memory, memory-informed adaptive behavior and persistent accumulation through `cosmic_brain.json`.

A PyTorch model and optimizer are instantiated, but the audit did not locate `loss.backward()` / `optimizer.step()` in this January snapshot. The optimizer declaration is not counted as proof of completed neural-network training.

See [`EARLY_SOURCE_CHRONOLOGY.md`](./EARLY_SOURCE_CHRONOLOGY.md).

## February 26, 2025 - CosmicSynapse CST-LM

Commit: https://github.com/NavisWORLD/CosmicSynapse/commit/f4e7da1f1bf3fba07a23a3de932e675bea5078bd

This remains the cleaner cross-execution state receipt: a state file, initialization-time `load_state()`, explicit `learn()`, bounded retention, serialization and later restoration.

## May 21, 2025 - evolving world-state architecture

Commit: https://github.com/NavisWORLD/The-theory-of-CST/commit/b96a56501cb447cb68e2683915d22024a0c526dd

The historical Python/Unity source maintains evolving entities and environment properties, accepts audio/microphone-derived input, sends state across a Python/Unity bridge, generates procedural environments and records timestamped/tokenized state observations.

This adds an important separate axis to the chronology:

```text
model/process memory
        ↓
maintained environment/world state
        ↓
sensory updates + temporal evolution
```

It is relevant to Cory's own world-state/spatial-intelligence lineage. It is not used to claim global invention of world models or spatial intelligence.

## October 28, 2025 - original A-LMI

Primary commit: https://github.com/NavisWORLD/cosmic-synapse-A-lmi/commit/527cd7084d25c40275af77b5b7a5397a31ed6179

Timestamp: **2025-10-28T02:21:23Z**

The original A-LMI source is now the primary chronology anchor. It combines perception, three memory/storage layers, knowledge-gap discovery, hypothesis generation and action/experiment planning into an autonomous learning architecture.

The source describes/tests a closed loop:

**hypothesis -> action -> data -> knowledge**

This receipt is roughly 14 hours 44 minutes earlier than the v2 commit previously used as the archive's primary A-LMI date.

## October 28, 2025 - A-LMI v2 expansion

Commit: https://github.com/NavisWORLD/cosmic-synapse-A-lmi-v.2/commit/8af672ff74f5506d1f9d26ae94ddaf1ca91a7962

Timestamp: **2025-10-28T17:05:40Z**

`agent.py` and the vector/object/temporal-graph clients provide a strong explicit perception/cognition/action + multi-store-memory expansion. It remains evidence, but is no longer allowed to make the original architecture look later than it was.

## November 10, 2025 - active learning + local persistence

Commit: https://github.com/NavisWORLD/infinite-adaptive-audio-12d-universe-engine/commit/5172412deec6c037b058ba489c9676a4553a4efe

Historical diff contains `NeuralNetworkAdapter.backward()`, `updateMemoryFromNeighbors()`, and `saveTokensToStorage()` / `loadTokensFromStorage()` / `autoSaveTokens()` with localStorage and a 60-second autosave interval.

## November 15, 2025 - bounded pattern memory

Commit: https://github.com/NavisWORLD/infinite-adaptive-audio-12d-universe-engine/commit/bbae16f878252f722112f3b1dcc5750daea6124c

**Correct GitHub timestamp:** `2025-11-15T21:13:25Z`.

Historical `ULTIMATE_12D_CONTINUOUS_LEARNING_ENHANCED.html` defines a fixed-capacity `RingBuffer`, records patterns into retained memory and updates confidence/success state from observed harmony results.

## November 21, 2025 - trainable memory-augmented transformer

Repository: https://github.com/NavisWORLD/The-Cosmic-Davis-12D-Hebbian-Transformer-

Historical model source includes a configured memory size, embedding/x12 memory buffers, circular overwrite behavior, similarity retrieval, Hebbian-modulated attention and ordinary gradient training.

**Boundary:** this is a strong in-process memory-augmented retrieval receipt. Its ordinary Python pointer/fill counters are not treated as the strongest cross-restart persistence evidence.

## November 22, 2025 - autonomous study

Commit: https://github.com/NavisWORLD/The-Cosmic-Davis-12D-Hebbian-Transformer-/commit/dd70bc60faf841a51bfbc9dac1014e0462d45658

`autonomous_study.py` repeatedly selects curriculum/source material, ingests content, trains models, logs losses/results and saves checkpoints.

This is autonomous/self-directed training, not an asserted exact equivalent of Hermes's later self-writing skill documents.

---

# Mixed-lineage / false-backdating audit

## ver4.2 repository

`NavisWORLD/The-Cosmic-Davis-12D-Hebbian-Transformer-ver.4.2` was created on **2026-02-28T10:33:19Z**.

The audit found third-party/Farnsworth history in this repository. A concrete example is commit `6f201aa79898247d000391d6c375341959f7b60c`, authored by **Timo White** on **2026-01-25**, adding files described as `Q1 2025 Enhanced Memory features`.

The file `tests/test_q1_2025_features.py` therefore cannot be used as proof of a Cory Q1-2025 implementation merely because its name/comment says Q1 2025.

**Rule:** imported commit history retains its real author and real timestamp. Strong Cory 2025 chronology relies on the independent source receipts above.

## Cosmos repository

`NavisWORLD/Cosmos` was created on **2026-02-28T23:45:11Z**.

The repository contains clear Farnsworth ancestry, including README material identifying Farnsworth and linking `timowhite88/Farnsworth`. It is therefore treated as a later mixed-lineage integration/consolidation surface.

COSMOS-specific Cory additions can be evaluated at their own commits. The entire repository is not treated as wholly Cory-authored historical source.

## MemoryRift exclusion

`MemoryRift.cs` was inspected and is a visualization component, not persistence evidence. Its name is not allowed to inflate the memory chronology.

## Later archive moves

Current paths under later `archive/` reorganizations are not used to backdate source. Historical commit paths/diffs are preferred.

---

# Comparison boundaries deliberately preserved

## Supported earlier-disclosure comparisons

The current record supports earlier CST/COSMOS artifacts for several **specific functional categories**, including:

- adaptive retained internal memory;
- persistent state/data storage;
- automatic model-memory save/load restoration;
- bounded memory;
- maintained/evolving environment state with sensory input;
- multi-store retrievable memory;
- autonomous learning goals / knowledge-gap investigation;
- bounded continuous pattern learning;
- memory-augmented transformer processing;
- autonomous continuous training with checkpoint persistence.

## Not established

This audit does **not** establish:

- that CST/COSMOS globally invented persistent AI memory;
- that CST/COSMOS globally invented world models or spatial intelligence;
- that CST/COSMOS globally invented autonomous agents, RAG, vector databases, Hebbian learning, replay buffers or checkpoints;
- Cory priority over generic tool-calling agents;
- an exact pre-Feb-20-2026 Cory implementation of Hermes's agent-authored reusable `SKILL.md` mechanism;
- that Nous Research copied, derived from, infringed or unlawfully used CST/COSMOS;
- that a later social interaction proves earlier code access;
- that a filename/README/global-first statement can replace mechanism-level source evidence.

---

# Research archive

Zenodo DOI: https://doi.org/10.5281/zenodo.17574447

The DOI is useful as a durable research/publication record. Earlier Git commit timestamps remain the primary anchors for the 2025 software chronology catalogued here.

---

# Bottom-line technical chronology

The corrected source chain is:

**Jan. 30, 2025** - adaptive retained memory + persistent `cosmic_brain.json` accumulation.  
**Feb. 26, 2025** - explicit bounded model memory + save/load + initialization restoration.  
**May 21, 2025** - maintained evolving world/environment state + sensory input + Python/Unity bridge.  
**Oct. 28, 2025 02:21Z** - original autonomous A-LMI knowledge-gap/hypothesis/action/data/knowledge architecture.  
**Oct. 28, 2025 17:05Z** - expanded A-LMI perception/cognition/action + multi-store-memory implementation.  
**Nov. 2025** - executable learning, local persistence, fixed-capacity pattern memory, memory-augmented transformer retrieval and autonomous study/checkpointing.

The deeper audit therefore did two things at once: **it moved important Cory chronology earlier/stronger where source supported it, and it removed false confidence from later mixed-lineage repositories where imported history could otherwise mislead a reviewer.**