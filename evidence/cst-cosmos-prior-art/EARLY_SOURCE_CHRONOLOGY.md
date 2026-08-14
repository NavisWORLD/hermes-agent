# Early CST / CosmicSynapse Source Chronology

This file records source-control facts and technical mechanisms found during a historical audit of GitHub-hosted repositories. It makes no allegation about any third party.

> **Public-accessibility caveat:** a platform-native GitHub commit date establishes a strong source-control timestamp, but patent-law public accessibility is a separate question. Current repository visibility does not by itself prove the historical public/private state on every earlier date. For legal-facing use, treat these as dated GitHub-hosted source artifacts and candidate prior-art references unless historical public accessibility is independently established.

## PHERACLEASE/test - January 2025

Repository: `PHERACLEASE/test`

Historical source file: `test1maybe.py`

Repository metadata currently shows:

- repository creation: **2025-01-15T02:26:18Z**;
- relevant push/commit timestamp: **2025-01-30T07:13:05Z**;
- current visibility: public.

First located commit adding the file: **2025-01-30T07:13:05Z**

Commit: `10e86764c6d743b5ceaaaf1baab7279a0d6f0ba5`

URL: https://github.com/PHERACLEASE/test/commit/10e86764c6d743b5ceaaaf1baab7279a0d6f0ba5

GitHub's commit record identifies GitHub/web-flow as committer and reports a valid verification record for the January 30 commit. The commit message includes `open sourcing`.

The January 30 source contains executable mechanisms including:

- a fixed-size particle memory array;
- a named `LearningMechanism` that updates memory using frequency/environmental features;
- rolling memory updates using `np.roll(...)` before writing new features;
- adaptive behavior that uses retained memory together with neural-network output;
- `COSMIC_BRAIN_FILE = "cosmic_brain.json"`;
- `save_cosmic_brain()` that reads existing stored JSON when present, adds a timestamped observation, and writes the accumulated data back;
- loaders for JSON, SQLite and pickle data;
- feedback-driven parameter updates in `MathSystem.evolve()`.

A PyTorch model and optimizer are instantiated in the file, but this audit did not locate a corresponding `loss.backward()` / `optimizer.step()` training path in this January snapshot. The optimizer declaration therefore is not counted as proof of completed neural-network training.

### Conservative technical statement

By January 30, 2025, GitHub's source-control record contains a CosmicSynapse-oriented source artifact with rolling/bounded internal memory, an explicit memory-update learning mechanism, memory-informed adaptive behavior, and persistent accumulation of observations in `cosmic_brain.json`.

### Identity/provenance note

Archive maintainer Cory Davis identifies `PHERACLEASE` as a legacy account. The currently inspected public GitHub profile metadata does not independently cross-link `PHERACLEASE` and `NavisWORLD`, so the account-attribution statement is kept separate from the independently verifiable repository timestamp and source contents.

---

## NavisWORLD/CosmicSynapse - February 2025

Commit: `f4e7da1f1bf3fba07a23a3de932e675bea5078bd`

Date: **2025-02-26T03:46:15Z**

URL: https://github.com/NavisWORLD/CosmicSynapse/commit/f4e7da1f1bf3fba07a23a3de932e675bea5078bd

Repository metadata currently shows creation at **2025-02-26T03:44:15Z** and current public visibility. The relevant upload commit identifies GitHub/web-flow as committer and GitHub reports a valid verification record.

This later source artifact provides a cleaner AI-state persistence mechanism:

- `self.memory = []`;
- an explicit `learn()` path;
- memory bounded to 1,000 retained entries;
- `save_state()` persistence;
- constructor-time `load_state()` restoration.

The larger CST simulation in the same upload also carries multiple histories and `cosmic_brain.json` state surfaces.

### Conservative technical statement

By February 26, 2025, the GitHub source-control record contains executable CST software with explicit model memory, learning, bounded retention, serialization and automatic restoration during a later initialization.

### Implementation-quality boundary

This is strong evidence of the disclosed architecture, not a claim that every standalone historical file was polished production software. Source quality and source chronology are separate questions.

---

## NavisWORLD/The-theory-of-CST - April / May 2025

The repository had a public CST theory/simulation surface by April 2025. The stronger mechanism-level receipt located in the audit is the May 21 source upload below.

Commit: `b96a56501cb447cb68e2683915d22024a0c526dd`

Date: **2025-05-21T08:04:53Z**

URL: https://github.com/NavisWORLD/The-theory-of-CST/commit/b96a56501cb447cb68e2683915d22024a0c526dd

The historical source includes a substantial Python + Unity simulation architecture with:

- evolving entities with retained position, velocity, energy/synaptic and ecosystem state;
- high-dimensional simulation variables projected into a live 3D environment;
- audio/microphone features feeding update behavior;
- Python-to-Unity communication over TCP;
- procedural generation of planets, atmospheres, ecosystems and visual properties;
- timestamped/token-oriented state logging through `MemoryNodeLog` surfaces;
- ongoing entity interaction and world evolution rather than a one-shot stateless render.

### Conservative technical statement

By May 21, 2025, the GitHub source-control record contains CST software that maintains and updates an evolving simulated environment, consumes live sensory/audio input, communicates state between a Python backend and Unity frontend, and records state observations over time.

### World-model / spatial-intelligence boundary

This source is relevant to the chronology of Cory's own persistent world-state / environment-modeling direction. It does **not** establish global invention of world models, model-based reinforcement learning or spatial intelligence, all of which have earlier third-party history.

---

## Chronology result

The January artifact remains the earliest presently located CST/CosmicSynapse memory-and-learning GitHub source artifact in this audit. The February artifact remains the stronger receipt for automatic save/load restoration of model memory across executions. The May artifact adds a distinct milestone: maintained **environment/world state**, sensory input, temporal evolution and a Python/Unity bridge.

For later autonomous-agent chronology, see [`MASTER_RECEIPT_AUDIT.md`](./MASTER_RECEIPT_AUDIT.md). For the adversarial review and older third-party technical baseline, see [`RED_TEAM_AND_THIRD_PARTY_BASELINE.md`](./RED_TEAM_AND_THIRD_PARTY_BASELINE.md).