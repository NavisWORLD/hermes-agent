# CST / COSMOS ↔ Hermes-Agent — Prior-Art Candidate & Provenance Timeline

**Prepared as a documentary chronology, not an accusation.**  
**Maintainer / earlier-disclosure researcher:** Cory Davis / NavisWORLD  
**Comparison target:** public `NousResearch/hermes-agent` repository history  
**Last updated:** 2026-08-13

## 1. Scope and standard

This document asks a narrow factual question:

> **When did specific technical mechanisms become publicly inspectable in the cited repositories, and what did those public artifacts actually implement?**

It does **not** assert that Nous Research copied CST/COSMOS, that any person saw a particular file before implementing a feature, that any patent is valid/invalid, or that any party infringed another party's rights.

For patent-law research, broad similarity is not enough. A serious anticipation analysis is claim-by-claim and asks whether the relevant earlier reference contains the required claim elements arranged as claimed and is sufficiently enabling. See USPTO MPEP § 2131, § 2152 and § 2121.

For the expanded source audit, see [`MASTER_RECEIPT_AUDIT.md`](./MASTER_RECEIPT_AUDIT.md).

---

## 2. High-confidence chronology

### 2025-01-30 — Earliest located public CST/CosmicSynapse memory-and-learning source artifact

**Repository:** `PHERACLEASE/test`  
**File:** `test1maybe.py`  
**Commit:** `10e86764c6d743b5ceaaaf1baab7279a0d6f0ba5`  
**URL:** https://github.com/PHERACLEASE/test/commit/10e86764c6d743b5ceaaaf1baab7279a0d6f0ba5

The historical source contains executable behavior including:

- a fixed-size particle memory array;
- a named `LearningMechanism` that updates retained memory from frequency/environmental features;
- a rolling update using `np.roll(...)`, followed by writes of new normalized features into the newest memory slots;
- adaptive behavior that consumes retained memory together with neural-network output;
- `COSMIC_BRAIN_FILE = "cosmic_brain.json"`;
- `save_cosmic_brain()` that reads pre-existing JSON when present, adds a timestamp-keyed observation, and writes the accumulated data back;
- JSON, SQLite and pickle loaders;
- feedback-driven parameter adaptation in `MathSystem.evolve()`.

The file instantiates a PyTorch model and optimizer, but this audit did not locate an actual `loss.backward()` / `optimizer.step()` training path in the January snapshot. That optimizer declaration is therefore **not** used as proof of completed neural-network training.

**Identity/provenance caveat:** archive maintainer Cory Davis identifies `PHERACLEASE` as a legacy account. The currently inspected public GitHub profile metadata does not independently cross-link `PHERACLEASE` and `NavisWORLD`, so the account-attribution statement is kept separate from the independently verifiable public code/date.

**Evidence weight:** A for technical source/date; separate attribution caveat retained.

See [`EARLY_SOURCE_CHRONOLOGY.md`](./EARLY_SOURCE_CHRONOLOGY.md).

### 2025-02-26 — Public CST-LM automatic save/load memory restoration

**Repository:** `NavisWORLD/CosmicSynapse`  
**Commit:** `f4e7da1f1bf3fba07a23a3de932e675bea5078bd`  
**URL:** https://github.com/NavisWORLD/CosmicSynapse/commit/f4e7da1f1bf3fba07a23a3de932e675bea5078bd

The committed CST-LM implementation contains executable behavior including:

- `self.memory = []`;
- `self.state_file = "cst_lm_state.json"`;
- `self.load_state()` invoked during initialization;
- an explicit `learn()` method that appends learned items to memory;
- bounded retention (`> 1000` removes the oldest memory item);
- `save_state()` serializing vocabulary + memory;
- `load_state()` restoring vocabulary + memory from persistent storage.

The larger CST simulation in the same public snapshot also includes `cosmic_brain.json`, retained histories, serialized/restored internal state and staged evolution state.

**Evidence weight:** A — source-code implementation with public Git history.

### 2025-07-23 — First public Hermes-Agent commit located

**Repository:** `NousResearch/hermes-agent`  
**Commit:** `21d80ca68346dfdb8d3556015a723a9217f8566f`  
**URL:** https://github.com/NousResearch/hermes-agent/commit/21d80ca68346dfdb8d3556015a723a9217f8566f

The initial source implements a real tool-calling AI agent and accepts caller-supplied `conversation_history`. The reviewed evidence does **not** establish Cory priority over Hermes on the generic concept of a tool-calling agent, and this archive makes no such claim.

**Evidence weight:** A — source-code chronology.

### 2025-10-28 — Public A-LMI autonomous learning + multi-store memory architecture

**Repository:** `NavisWORLD/cosmic-synapse-A-lmi-v.2`  
**Commit:** `8af672ff74f5506d1f9d26ae94ddaf1ca91a7962`  
**URL:** https://github.com/NavisWORLD/cosmic-synapse-A-lmi-v.2/commit/8af672ff74f5506d1f9d26ae94ddaf1ca91a7962

The public `a_lmi/core/agent.py` implements a perception-cognition-action architecture with perceptual ingestion, cognition, reasoning triggers, autonomous hypothesis investigation, action handling and `learning_goal` handling. File-specific Git history ties the following memory-store clients to this same public commit:

- `a_lmi/memory/vector_db_client.py`;
- `a_lmi/memory/object_storage_client.py`;
- `a_lmi/memory/tkg_client.py`.

**Evidence weight:** A — source-code implementation plus file-specific Git history.

### 2025-11-10 — Executable learning + persistent token save/load

**Repository:** `NavisWORLD/infinite-adaptive-audio-12d-universe-engine`  
**Commit:** `5172412deec6c037b058ba489c9676a4553a4efe`  
**URL:** https://github.com/NavisWORLD/infinite-adaptive-audio-12d-universe-engine/commit/5172412deec6c037b058ba489c9676a4553a4efe

The historical commit diff contains:

- a `NeuralNetworkAdapter` with explicit forward and backward weight-update logic;
- `updateMemoryFromNeighbors()` for Hebbian-like neighbor memory adaptation;
- current audio/frequency features integrated into memory;
- `saveTokensToStorage()`, `loadTokensFromStorage()` and `autoSaveTokens()`;
- a 60-second localStorage autosave interval and startup loading.

This is stronger than a commit message alone because the implementation appears directly in the historical diff.

**Evidence weight:** A — historical executable source diff.

### 2025-11-15 — Bounded continuous pattern-memory learning

**Repository:** `NavisWORLD/infinite-adaptive-audio-12d-universe-engine`  
**Commit:** `bbae16f878252f722112f3b1dcc5750daea6124c`  
**URL:** https://github.com/NavisWORLD/infinite-adaptive-audio-12d-universe-engine/commit/bbae16f878252f722112f3b1dcc5750daea6124c

The added `music project/ULTIMATE_12D_CONTINUOUS_LEARNING_ENHANCED.html` defines a fixed-capacity `RingBuffer`, creates `BandLearningSystem.patternMemory = new RingBuffer(128)`, pushes observed patterns into retained memory, and changes confidence/success state based on observed outcomes.

**Evidence weight:** A — source-code implementation in an immutable historical diff.

### 2025-11-21 — Trainable memory-augmented Hebbian Transformer

**Repository:** `NavisWORLD/The-Cosmic-Davis-12D-Hebbian-Transformer-`  
**Historical source path:** `packages/cosmic-synapse-transformer/cosmic_synapse/models/cosmic_synapse_transformer.py`

File history ties this implementation to the public repository by **2025-11-21**. The source includes:

- a configured fixed episodic-memory size;
- memory embeddings + x12 memory buffers;
- circular-memory pointer/fill tracking;
- memory updates during training;
- semantic + x12-adaptive similarity retrieval;
- retrieved-memory injection into transformer processing;
- Hebbian-modulated attention;
- adaptive x12 internal-state dynamics;
- ordinary gradient training through `loss.backward()` and `optimizer.step()` in the trainer.

**Evidence weight:** A — executable historical model source + file-specific commit history.

### 2025-11-22 — Continuous self-directed autonomous study

**Repository:** `NavisWORLD/The-Cosmic-Davis-12D-Hebbian-Transformer-`  
**File:** `experiments/42d_singularity/autonomous_study.py`  
**Commit:** `dd70bc60faf841a51bfbc9dac1014e0462d45658`  
**URL:** https://github.com/NavisWORLD/The-Cosmic-Davis-12D-Hebbian-Transformer-/commit/dd70bc60faf841a51bfbc9dac1014e0462d45658

The historical source describes and implements a continuous self-directed study loop that selects curriculum categories/sources, ingests content, trains 12D and 42D models, logs comparative losses/results, saves model checkpoints and continues the loop.

This is evidence of autonomous/self-directed training, **not** an asserted equivalent of Hermes's later self-writing reusable skill documents.

**Evidence weight:** A — executable historical source + file path history.

### 2026-02-19 — Hermes explicit persistent-memory + SQLite system

**Commit:** `440c244cac71f0764e00ea85ab87ae0a2d18fe61`  
**URL:** https://github.com/NousResearch/hermes-agent/commit/440c244cac71f0764e00ea85ab87ae0a2d18fe61

Commit title: `feat: add persistent memory system + SQLite session store`

The commit describes/implements `MEMORY.md` and `USER.md` persistent stores, bounded curated memory, replacement/removal/pruning behavior, memory injection at session start, SQLite session persistence, FTS5 session search, session-search tooling and linked session splitting.

**Evidence weight:** A — feature-specific source commit.

### 2026-02-20 — Hermes agent-created procedural skills

**Commit:** `4d5f29c74ca99928f053ac55d2f780be61b827df`  
**URL:** https://github.com/NousResearch/hermes-agent/commit/4d5f29c74ca99928f053ac55d2f780be61b827df

The commit explicitly adds skill management allowing the agent to create, update and delete reusable skills, described as procedural memory.

This is more specific than a general autonomous-learning loop. The pre-Hermes CST/A-LMI record currently catalogued here is therefore **not asserted to anticipate the exact Hermes agent-authored `SKILL.md` mechanism**.

**Evidence weight:** A — feature-specific source commit.

### 2026-03-06 — Hermes “self-improving AI agent” public positioning

**Commit:** `2dbbedc05a7fec7a4efe7db0f305e15393d92e5d`  
**URL:** https://github.com/NousResearch/hermes-agent/commit/2dbbedc05a7fec7a4efe7db0f305e15393d92e5d

Public documentation was changed to emphasize a built-in learning loop, autonomous skill creation, skill improvement, persistent knowledge, session search and cross-session user modeling.

**Evidence weight:** B for technical chronology; documentation/marketing language is weaker than executable implementation.

### 2026-03-19 — Cory submits sanitized COSMOS project directly to upstream Hermes

**PR:** `NousResearch/hermes-agent#2088`  
**Title:** `feat: add sanitized Cosmos project for audit review`  
**URL:** https://github.com/NousResearch/hermes-agent/pull/2088

The PR was opened by `NavisWORLD`, targeted upstream `main`, contained two commits and was later closed without merge.

Important adverse-timeline fact preserved intentionally: **this PR came after the 2026-02-19 persistent-memory commit and 2026-02-20 skill-management commit.** Therefore PR #2088 cannot, by itself, establish that those February features came from this submission.

**Evidence weight:** A for submission/contact chronology; not evidence of copying.

---

## 3. Feature comparison

| Technical concept | Earliest relevant CST/COSMOS evidence catalogued | Relevant Hermes evidence | Current assessment |
|---|---|---|---|
| Adaptive bounded internal memory | 2025-01-30 PHERACLEASE rolling particle memory + named learning mechanism | later Hermes memory systems | **Earlier public technical artifact located; different architecture** |
| Persistent accumulated observations | 2025-01-30 `cosmic_brain.json` read/append/write | 2026-02-19 persistent memory/session stores | **Earlier persistence mechanism; not equivalent to full session memory** |
| Persistent model memory across restarts | 2025-02-26 CST `state_file`, startup `load_state()`, `save_state()` | 2026-02-19 explicit persistent-memory system | **Strong earlier public CST disclosure of the general mechanism** |
| Bounded/pruned retained model memory | 2025-02-26 memory limit + oldest-entry removal | 2026-02-19 bounded curated memory | **Strong conceptual overlap; implementation differs** |
| Automatic restoration at initialization | 2025-02-26 constructor invokes `load_state()` | 2026-02-19 persistent memory injected per session | **Strong functional overlap** |
| Autonomous perception→cognition→action + learning goals | 2025-10-28 A-LMI | 2026 Hermes closed-learning-loop positioning | **Earlier A-LMI public architecture; implementation differs** |
| Multi-layer retrievable memory | 2025-10-28 vector DB + object store + temporal knowledge graph | 2026 MEMORY/USER + SQLite/FTS5 | **Earlier A-LMI architecture; materially different stores** |
| Executable online learning + local persistence | 2025-11-10 backprop adapter + neighbor memory + local save/load | later Hermes learning/memory systems | **Strong technical enablement receipt, not exact architecture identity** |
| Fixed-capacity continuous pattern memory | 2025-11-15 `RingBuffer(128)` learning system | later Hermes retained learning knowledge | **Earlier bounded continuous-learning implementation; different subject/application** |
| Memory-augmented transformer retrieval | 2025-11-21 episodic embedding/x12 circular buffer + similarity retrieval | later Hermes external/session memory | **Earlier executable mechanism; substantially different memory placement** |
| Autonomous continuous study/training | 2025-11-22 curriculum selection + training + checkpoint loop | later Hermes self-improvement/skills | **Earlier self-directed training receipt; not exact procedural-skill writing** |
| Generic tool-calling agent | No Cory-priority claim made here | Present in 2025-07-23 initial Hermes commit | **No Cory-priority finding** |
| Agent writes/edits reusable `SKILL.md` documents | Not established by catalogued pre-Hermes evidence | 2026-02-20 explicit skill management | **Not established** |

---

## 4. Strongest currently supportable technical propositions

> **By January 30, 2025, the public `PHERACLEASE/test` repository contained executable CosmicSynapse-oriented software with explicit rolling/bounded internal memory, a named learning mechanism that updates retained memory, memory-informed adaptive behavior, and persistent accumulation of timestamped observations in `cosmic_brain.json`.**

> **By February 26, 2025, Cory Davis / NavisWORLD had publicly disclosed executable CST software in which a model maintained internal memory, modified that memory through an explicit learning operation, bounded retained memory, serialized learned state to persistent storage, and restored that state during later initializations.**

> **By October 28, 2025, Cory Davis / NavisWORLD had publicly disclosed an autonomous-agent architecture organized around perception, cognition, multi-layer memory, reasoning, autonomous investigation, action and self-directed learning goals.**

> **By November 2025, the public CST/COSMOS record also included executable backprop learning, local save/load persistence, fixed-capacity pattern memory, a similarity-retrieved episodic-memory transformer, and a continuous self-directed model-training/checkpoint loop.**

These are chronology/provenance statements. They are not findings of legal anticipation, infringement, derivation or copying.

---

## 5. Zenodo / research archive

Related research archive / DOI: **10.5281/zenodo.17574447**  
https://doi.org/10.5281/zenodo.17574447

The DOI archive is useful as a durable scholarly/research record and should be read together with source-control history and test materials. For the 2025 software chronology in this archive, immutable Git commit dates remain the primary time anchors.

---

## 6. What the audit rejected or downgraded

- `MemoryRift.cs` was inspected and is a visualization component rather than a persistence implementation; it is excluded from the strong memory claim set.
- Current later `archive/` paths are not used to backdate files. Historical commit paths and diffs are used instead.
- Commit messages are discovery clues, not enough by themselves when executable source can be inspected.
- A declared optimizer without an actual training step is not counted as completed training.
- No pre-Hermes exact `SKILL.md` self-writing mechanism was found in the reviewed CST/COSMOS source.
- Screenshots are separated from source-code chronology and cannot substitute for immutable source history.

---

## 7. What this archive expressly does NOT claim

This archive does **not** claim that:

1. Nous Research copied Cory Davis's code.
2. Any Nous developer had access to a particular CST file before writing a particular Hermes feature unless independent evidence establishes that fact.
3. Cory Davis owns Hermes-Agent or its independently authored code.
4. Every Hermes feature is anticipated by CST/COSMOS.
5. Similarity alone proves copyright infringement.
6. Cory globally invented persistent AI memory, RAG/vector memory, replay buffers, autonomous agents, checkpointing or Hebbian learning.
7. A social-media block, like, repost or reply is evidence of guilt or wrongdoing.
8. An unrelated third-party PR merged into Hermes proves Cory's PR was merged.

Preserving contrary and limiting facts is intentional. A chronology is stronger when it records what the evidence does **not** prove.

---

## 8. Preservation methodology

- Source commits are identified by immutable commit IDs and repository URLs.
- File-specific commit history is used where a later repository contains reorganized paths.
- Documentary screenshots should be preserved without editorial alteration.
- Platform-native message URLs/export IDs should be added when available.
- Future evidence should be hashed with SHA-256 and indexed separately from interpretation.

---

## 9. Research/legal references

- USPTO MPEP § 2152: https://www.uspto.gov/web/offices/pac/mpep/s2152.html
- USPTO MPEP § 2131: https://www.uspto.gov/web/offices/pac/mpep/s2131.html
- USPTO MPEP § 2121: https://www.uspto.gov/web/offices/pac/mpep/s2121.html

Nothing in this repository is legal advice.
