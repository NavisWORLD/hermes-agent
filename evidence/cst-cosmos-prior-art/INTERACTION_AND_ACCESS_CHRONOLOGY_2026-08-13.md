# Interaction and Access Chronology

> Neutral evidence note. This record documents timestamps, public interactions, formal submission paths, and observable account activity. It does **not** allege copying, infringement, bad faith, theft, or unlawful conduct. Similar functionality can be independently developed. A social-media reaction or repost does not prove that the underlying repository or source code was opened, read, or used.

## Why this file exists

The evidence archive already documents source chronology and feature-level comparisons. This companion file records a different question: **what public contact and access opportunities are independently visible in the historical record?**

The distinction matters:

- **Interaction / exposure** means an account responded to, reposted, liked, or otherwise interacted with material.
- **Access opportunity** means technical material was placed in a location where it could be inspected, such as a public repository, community channel, or pull request.
- **Actual technical review or derivation** requires additional evidence and is **not established merely by interaction or access opportunity**.

## Record preserved from screenshots

### Direct Discord interaction with the Phera account

A screenshot from the `#hermes-agent` Discord shows Teknium directly replying in the channel after a Phera post and asking that material be moved to `#off-topic`.

**What this supports:** prior direct interaction between the Teknium account and the Phera account.

**What it does not establish:** that Teknium opened or reviewed a repository, paper, or source file.

### Technical discussion inside the Hermes community

A separate Discord screenshot shows a NOUS-badged participant responding to a Cosmos contribution and asking how the integration handled **agent coordination or state persistence across tasks**.

**What this supports:** Cosmos/CST material was being discussed inside the Hermes community at a technical-mechanism level.

**What it does not establish:** who else read the contribution or whether any later implementation was derived from it.

### Memory / consolidation demonstrations in the Hermes Discord

Additional screenshots show Phera posting COSMOS material in `#hermes-agent`, including memory-consolidation/runtime material and project screenshots.

**What this supports:** technical material was affirmatively placed inside the project community rather than merely existing elsewhere on the public internet.

**What it does not establish:** that any particular maintainer inspected all uploaded material.

### Reposts, likes, and direct X interactions

The preserved screenshots show repeated account-level interaction between Teknium and Phera/CosMos posts, including reposts, likes, and direct replies. Additional screenshots show the official Nous Research account reacting to at least one Phera reply about preparing a project submission.

Examples preserved in the screenshot bundle include:

- Teknium reposting a Phera post discussing Hermes + CST testing/integration.
- Teknium liking multiple Phera posts/replies about technical demos and integration.
- Teknium liking a post telling him that a commit/contribution was ready for review.
- Teknium and the official Nous Research account both liking a Phera reply about assembling and entering the project.
- Teknium later interacting with chronology/prior-work posts.

**What this supports:** repeated public interaction and exposure to the existence of the project and its demonstrations.

**What it does not establish:** that every linked artifact was opened, read, or used.

## Formal GitHub submission

On **2026-03-19**, `NavisWORLD` opened upstream PR **NousResearch/hermes-agent#2088**, titled:

`feat: add sanitized Cosmos project for audit review`

The PR targeted `NousResearch:main` from `NavisWORLD:cosmos-contribution` and contained two commits. The changed-file inventory exposed a substantial COSMOS code tree, including memory, persistence, continual-learning, orchestration, agent, and Hermes-integration surfaces.

Public PR:

https://github.com/NousResearch/hermes-agent/pull/2088

Examples visible in the PR file inventory include:

- `Cosmos/core/collective/persistent_agent.py`
- `Cosmos/core/cross_agent_memory.py`
- `Cosmos/core/learning/continual.py`
- `Cosmos/memory/episodic_memory.py`
- `Cosmos/memory/memory_system.py`
- `Cosmos/memory/unified_memory.py`
- `Cosmos/compatibility/hermes_adapter.py`
- `Cosmos/core/collective/dialogue_memory.py`
- `Cosmos/core/collective/claude_persistence.py`
- `Cosmos/tests/verify_memory_persistence.py`

**What this supports:** by March 19, 2026, a substantial Cosmos implementation was formally submitted into the upstream Hermes repository for review.

**Critical chronology limit:** this PR came after the February 19-20, 2026 Hermes persistent-memory / agent-created-skills commits already catalogued in this archive. Therefore PR #2088 **cannot be used to infer access or causation for those earlier February features**.

## Statement-consistency record

Later public statements attributed in the screenshots to Teknium include a broad recollection that he did not remember ever seeing, reacting to, or engaging with the user before, followed later by a narrower denial that he had read, touched, used, looked at, or had Hermes inspect the user's repositories, code, research, or papers.

The preserved interaction screenshots are inconsistent with the **broad no-prior-interaction recollection** because earlier direct replies, reposts, and reactions are visible.

However, the screenshots do **not** by themselves disprove the narrower claim that Teknium personally never opened/read/used the repositories or papers.

This archive therefore records both propositions separately:

1. **Prior direct interaction / exposure:** supported by the preserved record.
2. **Personal technical review or use by Teknium:** not established by the interaction screenshots alone.

No motive is inferred. Memory error, account confusion, skimming, or other explanations remain possible.

## Hiring / provenance relevance

The value of this record is not social-media drama. It demonstrates a reproducible provenance method:

`public source timestamp -> public demonstration -> community discussion -> formal submission -> later statements -> side-by-side chronology`

That method allows reviewers to separate what is documented from what remains unknown.
