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

## NavisWORLD/CosmicSynapse - February 2025

Commit: `f4e7da1f1bf3fba07a23a3de932e675bea5078bd`

Date: **2025-02-26T03:46:15Z**

URL: https://github.com/NavisWORLD/CosmicSynapse/commit/f4e7da1f1bf3fba07a23a3de932e675bea5078bd

Repository metadata currently shows creation at **2025-02-26T03:44:15Z** and current public visibility. The relevant upload commit identifies GitHub/web-flow as committer and GitHub reports a valid verification record.

This later source artifact provides a cleaner AI-state persistence mechanism: `memory`, an explicit `learn()` path, bounded retention, `save_state()`, and constructor-time `load_state()` restoration.

Accordingly, the January artifact is the earliest presently located CST/CosmicSynapse memory-and-learning GitHub source artifact in this audit, while the February artifact remains the stronger receipt for automatic save/load restoration of model memory across executions.

For the adversarial review and older third-party technical baseline, see [`RED_TEAM_AND_THIRD_PARTY_BASELINE.md`](./RED_TEAM_AND_THIRD_PARTY_BASELINE.md).
