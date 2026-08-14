# CST / COSMOS ↔ Hermes-Agent - Prior-Art Candidate & Provenance Timeline

**Prepared as a documentary chronology, not an accusation.**  
**Maintainer / earlier-disclosure researcher:** Cory Davis / NavisWORLD  
**Comparison target:** public `NousResearch/hermes-agent` repository history  
**Last updated:** 2026-08-13

## 1. Scope and standard

This document asks a narrow factual question:

> **When did specific technical mechanisms become inspectable in the cited source history, and what did those artifacts actually implement?**

It does **not** assert that Nous Research copied CST/COSMOS, that any person saw a particular file before implementing a feature, that any patent is valid/invalid, or that any party infringed another party's rights.

For patent-law research, broad similarity is not enough. Anticipation analysis is claim-by-claim and depends on the elements actually disclosed, their arrangement, enablement, effective filing dates and historical public accessibility. See USPTO MPEP § 2131, § 2152, § 2121 and § 2128.

For the expanded source audit, see [`MASTER_RECEIPT_AUDIT.md`](./MASTER_RECEIPT_AUDIT.md).

---

# 2. Corrected high-confidence chronology

## 2025-01-30 - earliest located CST/CosmicSynapse memory-and-learning source artifact

**Repository:** `PHERACLEASE/test`  
**File:** `test1maybe.py`  
**Commit:** `10e86764c6d743b5ceaaaf1baab7279a0d6f0ba5`  
**URL:** https://github.com/PHERACLEASE/test/commit/10e86764c6d743b5ceaaaf1baab7279a0d6f0ba5

The historical source contains:

- fixed-size particle memory;
- a named `LearningMechanism`;
- rolling `np.roll(...)` memory updates;
- memory-informed adaptive behavior;
- persistent `cosmic_brain.json` accumulation;
- feedback-driven parameter adaptation.

A PyTorch model and optimizer are instantiated, but the audit did not locate an actual `loss.backward()` / `optimizer.step()` training path in this January snapshot. The optimizer declaration is not used as proof of completed neural training.

**Identity/provenance caveat:** Cory identifies `PHERACLEASE` as a legacy account. The inspected public GitHub profile metadata did not independently cross-link `PHERACLEASE` and `NavisWORLD`, so the attribution statement is kept separate from the independently verifiable source/date.

**Evidence weight:** A for technical source/date; separate identity caveat retained.

## 2025-02-26 - CST-LM automatic save/load memory restoration

**Repository:** `NavisWORLD/CosmicSynapse`  
**Commit:** `f4e7da1f1bf3fba07a23a3de932e675bea5078bd`  
**URL:** https://github.com/NavisWORLD/CosmicSynapse/commit/f4e7da1f1bf3fba07a23a3de932e675bea5078bd

The source contains:

- `self.memory = []`;
- `self.state_file = "cst_lm_state.json"`;
- initialization-time `self.load_state()`;
- explicit `learn()`;
- a 1,000-item retention bound;
- `save_state()`;
- `load_state()` restoration.

**Evidence weight:** A - source-level implementation and dated Git history.

## 2025-05-21 - maintained evolving world/environment state + sensory bridge

**Repository:** `NavisWORLD/The-theory-of-CST`  
**Commit:** `b96a56501cb447cb68e2683915d22024a0c526dd`  
**URL:** https://github.com/NavisWORLD/The-theory-of-CST/commit/b96a56501cb447cb68e2683915d22024a0c526dd  
**Timestamp:** `2025-05-21T08:04:53Z`

The historical Python/Unity source includes:

- entities with evolving retained position/velocity/energy/synaptic/ecosystem state;
- high-dimensional simulation variables projected into a live environment;
- microphone/audio-derived input feeding state updates;
- Python-to-Unity communication;
- procedural world/entity generation;
- timestamped/token-oriented `MemoryNodeLog` state records;
- temporal world evolution and interacting entities.

**Current assessment:** an important earlier public source receipt for Cory's own persistent world-state / sensory-environment lineage.

**Boundary:** not a claim that Cory globally invented world models, model-based RL or spatial intelligence.

**Evidence weight:** A - historical source commit.

## 2025-07-23 - first located public Hermes-Agent commit

**Repository:** `NousResearch/hermes-agent`  
**Commit:** `21d80ca68346dfdb8d3556015a723a9217f8566f`  
**URL:** https://github.com/NousResearch/hermes-agent/commit/21d80ca68346dfdb8d3556015a723a9217f8566f

The initial source implements a real tool-calling AI agent and accepts caller-supplied `conversation_history`.

**Current assessment:** no Cory-priority claim for the generic tool-calling-agent concept.

## 2025-10-28 02:21:23Z - original A-LMI autonomous learning + multi-store memory

**Repository:** `NavisWORLD/cosmic-synapse-A-lmi`  
**Commit:** `527cd7084d25c40275af77b5b7a5397a31ed6179`  
**URL:** https://github.com/NavisWORLD/cosmic-synapse-A-lmi/commit/527cd7084d25c40275af77b5b7a5397a31ed6179

This is now the primary A-LMI chronology anchor. The source/documented implementation includes:

- web/audio perception;
- Milvus vector memory;
- MinIO object/raw storage;
- Neo4j temporal/graph memory;
- knowledge-gap discovery;
- hypothesis generation;
- action/experiment planning;
- a closed loop from **hypothesis -> action -> data -> knowledge**;
- tests for closed autonomous learning and key subsystems.

**Current assessment:** strong earlier public autonomous-agent / multi-store-memory receipt.

**Evidence weight:** A.

## 2025-10-28 17:05:40Z - A-LMI v2 expansion

**Repository:** `NavisWORLD/cosmic-synapse-A-lmi-v.2`  
**Commit:** `8af672ff74f5506d1f9d26ae94ddaf1ca91a7962`  
**URL:** https://github.com/NavisWORLD/cosmic-synapse-A-lmi-v.2/commit/8af672ff74f5506d1f9d26ae94ddaf1ca91a7962

The public `a_lmi/core/agent.py` implements explicit perception/cognition/action lanes, vector/object/temporal-graph storage, reasoning triggers, autonomous hypothesis investigation and `learning_goal` handling.

**Current assessment:** strong expansion receipt, but no longer allowed to make the original A-LMI architecture look later than it was.

## 2025-11-10 - executable learning + persistent token save/load

**Repository:** `NavisWORLD/infinite-adaptive-audio-12d-universe-engine`  
**Commit:** `5172412deec6c037b058ba489c9676a4553a4efe`

Historical diff contains:

- `NeuralNetworkAdapter` forward/backward weight updates;
- `updateMemoryFromNeighbors()`;
- audio/frequency information integrated into memory;
- `saveTokensToStorage()` / `loadTokensFromStorage()` / `autoSaveTokens()`;
- 60-second localStorage autosave and startup loading.

**Evidence weight:** A.

## 2025-11-15 21:13:25Z - bounded continuous pattern-memory learning

**Commit:** `bbae16f878252f722112f3b1dcc5750daea6124c`  
**URL:** https://github.com/NavisWORLD/infinite-adaptive-audio-12d-universe-engine/commit/bbae16f878252f722112f3b1dcc5750daea6124c

The source defines fixed-capacity `RingBuffer` memory, `BandLearningSystem.patternMemory = new RingBuffer(128)`, retained successful-pattern state and confidence/adaptation state.

**Timestamp correction:** GitHub records this commit at **2025-11-15T21:13:25Z**.

**Evidence weight:** A.

## 2025-11-21 - trainable memory-augmented Hebbian Transformer

**Repository:** `NavisWORLD/The-Cosmic-Davis-12D-Hebbian-Transformer-`

Historical model source includes:

- fixed episodic-memory capacity;
- memory embeddings + x12 state memory;
- circular overwrite behavior;
- semantic + x12 similarity retrieval;
- retrieved-memory injection;
- Hebbian-modulated attention;
- ordinary gradient training.

**Boundary:** strong in-process memory-augmented retrieval receipt, but not the archive's strongest cross-restart persistence proof.

## 2025-11-22 - continuous self-directed autonomous study

**File:** `experiments/42d_singularity/autonomous_study.py`  
**Commit:** `dd70bc60faf841a51bfbc9dac1014e0462d45658`

The source repeatedly selects curriculum/source material, ingests content, trains models, logs results and saves checkpoints.

**Boundary:** autonomous/self-directed training, not an asserted exact equivalent of Hermes's later self-writing reusable skill documents.

## 2026-02-19 - Hermes explicit persistent-memory + SQLite system

**Commit:** `440c244cac71f0764e00ea85ab87ae0a2d18fe61`

The commit adds/implements persistent MEMORY/USER stores, bounded curated memory, startup/session injection, SQLite session persistence, FTS5 search and linked session behavior.

**Evidence weight:** A.

## 2026-02-20 - Hermes agent-created procedural skills

**Commit:** `4d5f29c74ca99928f053ac55d2f780be61b827df`

The agent can create, update and delete reusable skills described as procedural memory.

**Current assessment:** the catalogued pre-Hermes CST/A-LMI record is **not asserted to anticipate the exact agent-authored `SKILL.md` mechanism**.

## 2026-03-06 - Hermes self-improving-agent positioning

**Commit:** `2dbbedc05a7fec7a4efe7db0f305e15393d92e5d`

Documentation emphasizes the learning loop, skills, memory, session search and self-improvement framing.

**Evidence weight:** B for chronology; documentation language is weaker than executable source.

## 2026-03-19 - Cory submits sanitized COSMOS project directly to upstream Hermes

**PR:** `NousResearch/hermes-agent#2088`  
**Title:** `feat: add sanitized Cosmos project for audit review`  
**URL:** https://github.com/NousResearch/hermes-agent/pull/2088

The PR establishes formal submission/contact chronology. It was opened after Hermes's Feb. 19 persistent-memory and Feb. 20 skill-management commits.

**Critical boundary:** PR #2088 cannot by itself establish access for those earlier February features.

---

# 3. Mixed-lineage corrections

## Later ver4.2 repository is not a clean 2025 source anchor

`NavisWORLD/The-Cosmic-Davis-12D-Hebbian-Transformer-ver.4.2` was created on **2026-02-28T10:33:19Z** and contains identifiable third-party/Farnsworth history.

A concrete example is commit `6f201aa79898247d000391d6c375341959f7b60c`, authored by **Timo White** on **2026-01-25**, which added files described as `Q1 2025 Enhanced Memory features`.

Therefore a file such as `tests/test_q1_2025_features.py` cannot be used to establish Cory Q1-2025 chronology merely from its name/comment. Imported history keeps its actual author/date.

## `Cosmos` is a later mixed-lineage consolidation

`NavisWORLD/Cosmos` was created on **2026-02-28T23:45:11Z** and contains clear Farnsworth ancestry, including README material identifying Farnsworth and linking `timowhite88/Farnsworth`.

COSMOS-specific Cory additions can be evaluated commit-by-commit, but the whole repository is not treated as wholly Cory-authored historical source.

These corrections make the earlier independent 2025 receipts more important, not less.

---

# 4. Feature comparison

| Technical concept | Earliest relevant CST/COSMOS evidence catalogued | Relevant Hermes evidence | Current assessment |
|---|---|---|---|
| Adaptive bounded internal memory | 2025-01-30 PHERACLEASE rolling memory + named learning mechanism | later Hermes memory systems | **Earlier technical artifact located; different architecture** |
| Persistent accumulated observations | 2025-01-30 `cosmic_brain.json` accumulation | 2026-02-19 memory/session stores | **Earlier persistence mechanism; not equivalent to full session memory** |
| Persistent model memory across restarts | 2025-02-26 CST state file + startup `load_state()` | 2026-02-19 explicit persistent-memory system | **Strong earlier CST disclosure of the general mechanism** |
| Bounded/pruned retained model memory | 2025-02-26 oldest-entry removal | 2026-02-19 bounded curated memory | **Strong conceptual overlap; implementation differs** |
| Automatic restoration at initialization | 2025-02-26 constructor invokes `load_state()` | 2026-02-19 session/startup memory injection | **Strong functional overlap** |
| Maintained evolving environment/world state | 2025-05-21 Python/Unity CST simulation with sensory updates | not used here as a direct Hermes claim | **Important Cory lineage receipt; no global-first claim** |
| Autonomous learning / knowledge-gap loop | 2025-10-28 02:21 original A-LMI | 2026 Hermes closed-loop/self-improvement positioning | **Earlier A-LMI architecture; implementation differs** |
| Multi-layer retrievable memory | 2025-10-28 A-LMI Milvus + MinIO + Neo4j | 2026 MEMORY/USER + SQLite/FTS5 | **Earlier A-LMI multi-store architecture; materially different stores** |
| Executable online learning + local persistence | 2025-11-10 backprop adapter + neighbor memory + save/load | later Hermes learning/memory systems | **Strong enablement receipt, not exact architecture identity** |
| Fixed-capacity continuous pattern memory | 2025-11-15 `RingBuffer(128)` | later Hermes retained learning knowledge | **Earlier bounded implementation; different application** |
| Memory-augmented transformer retrieval | 2025-11-21 episodic embedding/x12 retrieval | later Hermes external/session memory | **Earlier executable mechanism; different memory placement** |
| Autonomous continuous study/training | 2025-11-22 curriculum/training/checkpoint loop | later Hermes self-improvement/skills | **Earlier self-directed training; not exact procedural-skill writing** |
| Generic tool-calling agent | no Cory-priority claim | present 2025-07-23 in Hermes | **No Cory-priority finding** |
| Agent writes/edits reusable `SKILL.md` documents | not established pre-Hermes | 2026-02-20 explicit skill management | **Not established** |

---

# 5. Strongest currently supportable propositions

> **By January 30, 2025, the `PHERACLEASE/test` source record contained executable CosmicSynapse-oriented software with rolling/bounded internal memory, a named learning mechanism, memory-informed adaptive behavior and persistent accumulation in `cosmic_brain.json`.**

> **By February 26, 2025, Cory Davis / NavisWORLD had disclosed executable CST software in which a model maintained internal memory, modified it through an explicit learning operation, bounded retained memory, serialized state and restored that state during later initialization.**

> **By May 21, 2025, Cory Davis / NavisWORLD had disclosed an evolving simulated-environment architecture that maintained entity/world state over time, consumed audio/sensory input, bridged Python and Unity state, and recorded timestamped state observations.**

> **By October 28, 2025 at 02:21 UTC, Cory Davis / NavisWORLD had disclosed an autonomous learning architecture that combined perception, multi-store memory, knowledge-gap discovery, hypothesis generation and planned actions/experiments in a closed learning loop.**

> **By November 2025, the CST/COSMOS record also included executable backprop learning, local save/load persistence, fixed-capacity pattern memory, similarity-retrieved episodic memory and a continuous self-directed model-training/checkpoint loop.**

These are chronology/provenance statements. They are not findings of legal anticipation, infringement, derivation or copying.

---

# 6. Findings deliberately not claimed

This archive does not claim:

- global invention of persistent AI memory;
- global invention of world models or spatial intelligence;
- global invention of autonomous agents, RAG, vector databases, Hebbian learning, replay buffers, checkpointing or skill libraries;
- Cory priority over generic tool-calling agents;
- a pre-Hermes exact equivalent of Hermes's agent-authored reusable `SKILL.md` mechanism;
- that social reactions prove repository review;
- that the March 19 PR caused features published before March 19;
- that a later mixed-lineage repository can be flattened into wholly Cory-authored history;
- that a filename, README slogan or global-first marketing sentence substitutes for source evidence.

---

# 7. Research archive

Related research archive / DOI: **10.5281/zenodo.17574447**  
https://doi.org/10.5281/zenodo.17574447

The DOI is useful as a durable scholarly/research record. Earlier source commits remain the primary anchors for the 2025 software chronology catalogued here.