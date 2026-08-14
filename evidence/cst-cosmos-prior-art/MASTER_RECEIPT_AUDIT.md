# Master Source Receipt Audit

**Last updated:** 2026-08-13  
**Purpose:** preserve a conservative, reproducible chronology of public CST/COSMOS technical artifacts and selected public Hermes-Agent comparison artifacts.

> This is a technical chronology. It does not allege copying, derivation, infringement, bad faith, or unlawful conduct. Similar systems can be independently developed. Broad AI-memory, retrieval, autonomous-agent, replay-buffer, checkpointing and Hebbian concepts also have substantial third-party history outside these repositories.

## Audit rules

A row receives strong weight only when the relevant mechanism can be tied to a platform-native public timestamp and inspected source or commit diff. Repository names, marketing language, screenshots and later-moved archive paths are not treated as substitutes for historical source.

## Chronology

| Date | Public artifact | Mechanism actually supported | Audit result |
|---|---|---|---|
| **2025-01-30** | `PHERACLEASE/test` commit `10e86764c6d743b5ceaaaf1baab7279a0d6f0ba5` | rolling/fixed-size particle memory; named learning mechanism; memory-informed adaptive behavior; persistent `cosmic_brain.json` accumulation | **Earliest located CST/CosmicSynapse memory-and-learning source artifact in this audit.** Account attribution to Cory is stated by the maintainer; public profile metadata does not independently cross-link the legacy account. |
| **2025-02-26** | `NavisWORLD/CosmicSynapse` commit `f4e7da1f1bf3fba07a23a3de932e675bea5078bd` | `memory`; explicit `learn()`; bounded retention; `save_state()`; constructor-time `load_state()`; larger `cosmic_brain.json` state/history persistence | **Strongest early receipt for explicit automatic save/load restoration of AI model memory across executions.** |
| **2025-07-23** | `NousResearch/hermes-agent` initial commit `21d80ca68346dfdb8d3556015a723a9217f8566f` | real tool-calling agent; caller-supplied conversation history | **No Cory-priority claim for generic tool calling.** |
| **2025-10-28** | `NavisWORLD/cosmic-synapse-A-lmi-v.2` commit `8af672ff74f5506d1f9d26ae94ddaf1ca91a7962` | perception→cognition→action loop; vector storage; raw/object storage; temporal knowledge graph; reasoning triggers; hypothesis-driven investigation; learning-goal handling | **Strong public autonomous-agent / multi-store memory receipt.** |
| **2025-11-10** | `NavisWORLD/infinite-adaptive-audio-12d-universe-engine` commit `5172412deec6c037b058ba489c9676a4553a4efe` | actual neural-network forward/backward weight updates; neighbor-memory learning; localStorage token save/load; automatic 60-second persistence | **Strong executable learning + persistence receipt.** |
| **2025-11-15** | same repository, commit `bbae16f878252f722112f3b1dcc5750daea6124c` | `RingBuffer(128)` pattern memory; continuous learning system; retained successful patterns; confidence/adaptation state | **Strong bounded continuous-learning/pattern-memory receipt.** |
| **2025-11-21** | `NavisWORLD/The-Cosmic-Davis-12D-Hebbian-Transformer-`, historical transformer source | fixed-size circular episodic memory of embeddings/x12 state; semantic + adaptive similarity retrieval; Hebbian attention; adaptive internal state; gradient training | **Strong executable memory-augmented transformer receipt.** |
| **2025-11-22** | same repository, `autonomous_study.py` at commit `dd70bc60faf841a51bfbc9dac1014e0462d45658` | continuous self-directed study loop; autonomous curriculum/source selection; repeated model training; progress logs; persistent checkpoints | **Strong autonomous-training/self-directed-study receipt.** |
| **2026-02-19** | `NousResearch/hermes-agent` commit `440c244cac71f0764e00ea85ab87ae0a2d18fe61` | explicit persistent MEMORY/USER stores; bounded curated memory; startup/session injection; SQLite session store; FTS5 search; linked sessions | **Feature-specific Hermes persistent-memory implementation.** |
| **2026-02-20** | Hermes commit `4d5f29c74ca99928f053ac55d2f780be61b827df` | agent can create/update/delete reusable skills; described as procedural memory | **Exact pre-Hermes CST equivalent of agent-authored `SKILL.md` procedural skills not established by this audit.** |
| **2026-03-06** | Hermes commit `2dbbedc05a7fec7a4efe7db0f305e15393d92e5d` | public “self-improving AI agent” positioning around learning loop, skills, memory and session search | **Documentation/positioning chronology; weaker than executable-source evidence.** |
| **2026-03-19** | `NousResearch/hermes-agent#2088` | Cory/NavisWORLD submits sanitized COSMOS project for audit review | **Direct submission/contact chronology. It occurs after Hermes's Feb. 19/20 commits and therefore cannot establish access for those earlier features.** |

## Detailed receipts

### January 30, 2025 — PHERACLEASE/test

Commit: https://github.com/PHERACLEASE/test/commit/10e86764c6d743b5ceaaaf1baab7279a0d6f0ba5

Historical `test1maybe.py` contains a named `LearningMechanism` and performs rolling memory updates with `np.roll(...)`, then writes new normalized frequency features into memory. It also defines `COSMIC_BRAIN_FILE = "cosmic_brain.json"`; `save_cosmic_brain()` reads existing JSON when present, adds a timestamp-keyed observation and writes accumulated data back.

See [`EARLY_SOURCE_CHRONOLOGY.md`](./EARLY_SOURCE_CHRONOLOGY.md).

### February 26, 2025 — CosmicSynapse CST-LM

Commit: https://github.com/NavisWORLD/CosmicSynapse/commit/f4e7da1f1bf3fba07a23a3de932e675bea5078bd

This is the cleaner cross-execution state receipt: the model initializes with a state file, calls `load_state()`, has an explicit `learn()` operation, bounds retained memory, serializes memory/vocabulary and reloads them during a later initialization.

### October 28, 2025 — A-LMI

Commit: https://github.com/NavisWORLD/cosmic-synapse-A-lmi-v.2/commit/8af672ff74f5506d1f9d26ae94ddaf1ca91a7962

File-specific Git history ties the vector database client, object-storage client and temporal-knowledge-graph client to this same public commit. `agent.py` combines those memory stores with perception, cognition, reasoning, action, autonomous hypothesis investigation and learning-goal handling.

### November 10, 2025 — active learning + local persistence

Commit: https://github.com/NavisWORLD/infinite-adaptive-audio-12d-universe-engine/commit/5172412deec6c037b058ba489c9676a4553a4efe

Historical file:

`Cosmic synaptic demo vr.4.20/cosmic420/cosmic 12D internal memory demo/html/12D_Cosmic_Synapse_Audio_Engine-demo.html`

The commit diff contains a real `NeuralNetworkAdapter.backward()` weight-update implementation, `updateMemoryFromNeighbors()`, and `saveTokensToStorage()` / `loadTokensFromStorage()` / `autoSaveTokens()` with localStorage and a 60-second autosave interval.

### November 15, 2025 — bounded pattern memory

Commit: https://github.com/NavisWORLD/infinite-adaptive-audio-12d-universe-engine/commit/bbae16f878252f722112f3b1dcc5750daea6124c

Historical file:

`music project/ULTIMATE_12D_CONTINUOUS_LEARNING_ENHANCED.html`

The added source defines a fixed-capacity `RingBuffer`, instantiates `BandLearningSystem.patternMemory = new RingBuffer(128)`, records patterns into the memory and updates confidence/success state based on observed harmony results.

### November 21, 2025 — trainable memory-augmented transformer

Repository: https://github.com/NavisWORLD/The-Cosmic-Davis-12D-Hebbian-Transformer-

Historical source includes `EpisodicMemory` with a configured memory size, memory embeddings and x12 buffers, a circular pointer, similarity-based retrieval, Hebbian-modulated attention and ordinary gradient training through a trainer.

### November 22, 2025 — autonomous study

Path history commit: https://github.com/NavisWORLD/The-Cosmic-Davis-12D-Hebbian-Transformer-/commit/dd70bc60faf841a51bfbc9dac1014e0462d45658

`autonomous_study.py` describes and implements a continuous self-directed study session: select curriculum/source, ingest content, train models, log losses/results, save checkpoints and continue the loop.

## Comparison boundaries deliberately preserved

### Supported earlier-public-disclosure comparisons

The current record supports earlier public CST/COSMOS artifacts for several **specific functional categories**, including:

- adaptive retained internal memory;
- persistent state/data storage;
- automatic model-memory save/load restoration;
- bounded memory;
- multi-store retrievable memory;
- autonomous learning goals / investigation;
- bounded continuous pattern learning;
- memory-augmented transformer processing;
- autonomous continuous training with checkpoint persistence.

### Not established

This audit does **not** establish:

- that CST/COSMOS globally invented persistent AI memory;
- that CST/COSMOS globally invented autonomous agents, RAG, vector databases, Hebbian learning, replay buffers or checkpoints;
- Cory priority over the generic tool-calling-agent concept;
- an exact pre-Feb-20-2026 Cory implementation of Hermes's agent-authored reusable `SKILL.md` mechanism;
- that Nous Research copied, derived from, infringed, or unlawfully used CST/COSMOS;
- that a later social interaction proves earlier access.

## Excluded / downgraded receipts

- `MemoryRift.cs` was inspected and is a visualization component, not a persistence mechanism; it is excluded from the strong memory claim set despite its filename.
- Current paths under later `archive/` reorganizations are not used to backdate source. Historical commit paths/diffs are preferred.
- Repository names, commit messages and documentation are not treated as proof of a mechanism when source was available to inspect.
- Screenshots are kept in the separate exhibit index and are not substituted for source chronology.

## Research archive

Zenodo DOI: https://doi.org/10.5281/zenodo.17574447

The DOI is useful as a durable research/publication record. Earlier Git commit timestamps remain the primary anchors for the 2025 software chronology catalogued here.

## Bottom-line technical chronology

The earliest located CST/CosmicSynapse memory-and-learning code in this audit is now **January 30, 2025**. The strongest early automatic model-state restoration receipt remains **February 26, 2025**. By **October 28, 2025**, the public record expands to an autonomous agent with multiple memory stores and learning goals; by **November 2025**, the record includes executable backprop learning, local save/load persistence, bounded continuous pattern memory, a memory-augmented Hebbian transformer, and autonomous continuous study/checkpointing.
