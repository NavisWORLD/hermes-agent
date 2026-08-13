# CST / COSMOS ↔ Hermes-Agent — Prior-Art Candidate & Provenance Timeline

**Prepared as a documentary chronology, not an accusation.**  
**Author / earlier-disclosure researcher:** Cory Davis / NavisWORLD  
**Comparison target:** public `NousResearch/hermes-agent` repository history  
**Last updated:** 2026-08-13

## 1. Scope and standard

This document asks a narrow factual question:

> **When did specific technical mechanisms become publicly inspectable in the cited repositories, and what did those public artifacts actually implement?**

It does **not** assert that Nous Research copied CST/COSMOS, that any person saw a particular file before implementing a feature, that any patent is valid/invalid, or that any party infringed another party's rights.

For patent-law research, broad similarity is not enough. A serious anticipation analysis is claim-by-claim and asks whether a single earlier reference contains every required claim element arranged as required. See USPTO MPEP § 2131 and § 2152.

---

## 2. High-confidence chronology

### 2025-02-26 — Public CST/COSMOS implementation

**Repository:** `NavisWORLD/CosmicSynapse`  
**Commit:** `f4e7da1f1bf3fba07a23a3de932e675bea5078bd`  
**URL:** https://github.com/NavisWORLD/CosmicSynapse/commit/f4e7da1f1bf3fba07a23a3de932e675bea5078bd

The committed CST-LM implementation contains executable behavior including:

- `self.memory = []`
- `self.state_file = "cst_lm_state.json"`
- `self.load_state()` invoked during initialization
- an explicit `learn()` method that appends learned items to memory
- bounded retention (`> 1000` causes the oldest memory entry to be removed)
- `save_state()` serializing vocabulary + memory
- `load_state()` restoring vocabulary + memory from persistent storage

The larger CST simulation in the same public snapshot also contains `COSMIC_BRAIN_FILE = "cosmic_brain.json"`, retained `memory`, `emotion_history`, and `face_history`, serialized/restored internal state, and staged evolution state.

**Evidence weight:** A — source-code implementation with public Git history.

### 2025-07-23 — First public Hermes-Agent commit located

**Repository:** `NousResearch/hermes-agent`  
**Commit:** `21d80ca68346dfdb8d3556015a723a9217f8566f`  
**URL:** https://github.com/NousResearch/hermes-agent/commit/21d80ca68346dfdb8d3556015a723a9217f8566f

The initial source implements a real tool-calling AI agent and accepts caller-supplied `conversation_history`. The currently reviewed initial snapshot does **not** establish that Cory preceded Hermes on the generic concept of a tool-calling agent, and this archive makes no such claim.

**Evidence weight:** A — source-code chronology.

### 2025-10-28 — Public A-LMI autonomous learning architecture

**Repository:** `NavisWORLD/cosmic-synapse-A-lmi-v.2`  
**Commit:** `8af672ff74f5506d1f9d26ae94ddaf1ca91a7962`  
**URL:** https://github.com/NavisWORLD/cosmic-synapse-A-lmi-v.2/commit/8af672ff74f5506d1f9d26ae94ddaf1ca91a7962

The public `a_lmi/core/agent.py` describes an autonomous perception-cognition-action loop and implements perceptual ingestion, cognition and multi-layer memory storage, vector-database storage, object/raw-data storage, knowledge-graph storage, reasoning triggers, autonomous hypothesis investigation, action handling, and `learning_goal` handling.

**Evidence weight:** A — source-code implementation with public Git history.

### 2026-02-19 — Hermes explicit persistent-memory + SQLite system

**Commit:** `440c244cac71f0764e00ea85ab87ae0a2d18fe61`  
**URL:** https://github.com/NousResearch/hermes-agent/commit/440c244cac71f0764e00ea85ab87ae0a2d18fe61

Commit title: `feat: add persistent memory system + SQLite session store`

The public commit describes/implements `MEMORY.md` and `USER.md` persistent stores, bounded curated memory, replacement/removal/pruning behavior, memory injection at session start, SQLite session persistence, FTS5 session search, session-search tooling, and linked session splitting.

**Evidence weight:** A — feature-specific source commit.

### 2026-02-20 — Hermes agent-created procedural skills

**Commit:** `4d5f29c74ca99928f053ac55d2f780be61b827df`  
**URL:** https://github.com/NousResearch/hermes-agent/commit/4d5f29c74ca99928f053ac55d2f780be61b827df

The commit explicitly adds a skill-management tool allowing the agent to create, update, and delete its own skills, described as **procedural memory**.

This is more specific than a general autonomous-learning loop. The currently catalogued CST/A-LMI evidence is therefore **not asserted to anticipate the exact Hermes `SKILL.md` self-writing mechanism**.

**Evidence weight:** A — feature-specific source commit.

### 2026-03-06 — Hermes “self-improving AI agent” public positioning

**Commit:** `2dbbedc05a7fec7a4efe7db0f305e15393d92e5d`  
**URL:** https://github.com/NousResearch/hermes-agent/commit/2dbbedc05a7fec7a4efe7db0f305e15393d92e5d

Public documentation was changed to emphasize a built-in learning loop, autonomous skill creation, skill improvement, persistent knowledge, session search, and cross-session user modeling.

**Evidence weight:** B for technical chronology; documentation/marketing language is weaker than executable implementation.

### 2026-03-19 — Cory submits sanitized COSMOS project directly to upstream Hermes repository

**PR:** `NousResearch/hermes-agent#2088`  
**Title:** `feat: add sanitized Cosmos project for audit review`  
**URL:** https://github.com/NousResearch/hermes-agent/pull/2088

The PR was opened by `NavisWORLD`, targeted `NousResearch:main`, contained two commits, and was later closed without merge.

Important adverse-timeline fact preserved intentionally: **this PR came after the 2026-02-19 Hermes persistent-memory commit and the 2026-02-20 skill-management commit.** Therefore PR #2088 cannot, by itself, establish that those February features came from this submission.

**Evidence weight:** A for contact/submission chronology; not evidence of copying.

---

## 3. Feature comparison

| Technical concept | Earliest Cory public evidence currently catalogued | Relevant Hermes public evidence | Current assessment |
|---|---|---|---|
| Persistent model memory across restarts | 2025-02-26 CST `state_file`, startup `load_state()`, `save_state()` | 2026-02-19 explicit persistent-memory system | **Strong earlier public CST disclosure of the general mechanism** |
| Bounded/pruned retained memory | 2025-02-26 memory limit + oldest-entry removal | 2026-02-19 bounded curated memory | **Strong conceptual overlap; different implementation details** |
| Persistent internal state beyond transient conversation | 2025-02-26 `cosmic_brain.json` and saved histories/state | 2026-02-19 memory files + SQLite session store | **Strong/moderate overlap** |
| Automatic restoration at startup/session initialization | 2025-02-26 constructor invokes `load_state()` | 2026-02-19 persistent memory loaded/injected per session | **Strong functional overlap** |
| Explicit learning operation modifies retained memory | 2025-02-26 `learn()` appends to memory/history | 2026 memory tools/learning-loop architecture | **Moderate/strong functional overlap** |
| Multiple retained internal-history categories | 2025-02-26 memory + emotion + face histories | later declarative/identity/episodic/procedural knowledge categories | **Moderate overlap** |
| Autonomous perception → cognition → action learning loop | 2025-10-28 A-LMI | 2026 Hermes closed learning loop | **Earlier A-LMI public architecture; implementation details differ** |
| Multi-layer retrievable long-term memory | 2025-10-28 vector DB + object storage + knowledge graph | 2026 MEMORY/USER + SQLite/FTS5 | **Moderate overlap; materially different architectures** |
| Generic tool-calling agent | No Cory priority claim made here | Present in 2025-07-23 initial Hermes commit | **No Cory-priority finding** |
| Agent writes/edits reusable skill documents | Not established by currently catalogued pre-Hermes evidence | 2026-02-20 explicit `skill_manage` | **Not established** |

---

## 4. Strongest currently supportable propositions

> **By 2025-02-26, Cory Davis / NavisWORLD had publicly disclosed executable CST software in which a transformer-based system maintained internal memory, modified that memory through an explicit learning operation, bounded retained memory, serialized learned state to persistent storage, and restored that state during later executions.**

> **By 2025-10-28, Cory Davis / NavisWORLD had publicly disclosed an autonomous-agent architecture organized around perception, cognition, multi-layer memory, reasoning, autonomous investigation, action, and self-directed learning goals.**

These are chronology/provenance statements. They are not findings of legal anticipation, infringement, derivation, or copying.

---

## 5. Zenodo / research archive

Related research archive / DOI: **10.5281/zenodo.17574447**  
https://doi.org/10.5281/zenodo.17574447

The DOI archive is useful as a durable scholarly/research record and should be read together with source-control history and test materials. **The February 2025 Git commit remains the key presently catalogued timestamp for the earliest public executable implementation discussed above unless an earlier independently verifiable deposit/version is identified.**

---

## 6. Contact / awareness evidence

The documentary exhibits archived beside this file are categorized separately from source-code chronology. They may support propositions about public visibility, technical discussion, or later access/contact, but they do not by themselves prove copying.

The strongest screenshot supplied in this category is the Hermes-community Discord exchange where Cory posts the COSMOS contribution link and a participant displaying a NOUS community badge asks specifically about **agent coordination or state persistence across tasks**. That supports a limited proposition that the contribution and persistence-related concepts were being discussed in the Hermes community at that time.

---

## 7. What this archive expressly does NOT claim

This archive does **not** claim that:

1. Nous Research copied Cory Davis's code.
2. Any Nous developer had access to a particular CST file before writing a particular Hermes feature unless independent evidence establishes that fact.
3. Cory Davis owns Hermes-Agent or its independently authored code.
4. Every Hermes feature is anticipated by CST/COSMOS.
5. Similarity alone proves copyright infringement.
6. A social-media block, like, repost, or reply is evidence of guilt or wrongdoing.
7. An unrelated third-party PR merged into Hermes proves that Cory's PR was merged.

Preserving contrary and limiting facts is intentional. A chronology is more credible when it records what the evidence **does not** prove.

---

## 8. Preservation methodology

- Source commits are identified by immutable commit IDs and repository URLs.
- Documentary screenshots should be preserved without editorial annotation.
- Original platform message URLs/export IDs should be added when available because platform-native timestamps are stronger than relative labels such as `3h`.
- Future evidence should be hashed with SHA-256 and indexed separately from interpretation.

---

## 9. Research/legal references

- USPTO MPEP § 2152: https://www.uspto.gov/web/offices/pac/mpep/s2152.html
- USPTO MPEP § 2131: https://www.uspto.gov/web/offices/pac/mpep/s2131.html
- USPTO MPEP § 2121: https://www.uspto.gov/web/offices/pac/mpep/s2121.html

Nothing in this repository is legal advice.
