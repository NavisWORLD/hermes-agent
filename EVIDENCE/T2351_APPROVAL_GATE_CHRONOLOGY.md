# T-2351 — Approval-Gate / Agent-Control Chronology Evidence Matrix

**Recorded in Hermes fork:** 2026-08-15  
**Owner of this fork:** Cory Davis / NavisWORLD  
**Nous support reference:** `T-2351`  

This file is intentionally stored **inside the Hermes Agent fork** so the comparison is attached to the same code lineage being reviewed.

> **Claim boundary:** This is a chronology/provenance exhibit, not an allegation that Nous Research copied COSMOS or had access to Cory Davis's work. Architectural similarity and chronology do not by themselves establish derivation. Any stronger attribution would require independent evidence.

---

## 1. Earlier COSMOS public record

### 2026-01-25 — licensing + documentation record

Repository:

`NavisWORLD/The-Cosmic-Davis-12D-Hebbian-Transformer-ver.4.2`

Commit:

`401ab05714cd465009f49ba198e454e807149b91`

Public commit URL:

https://github.com/NavisWORLD/The-Cosmic-Davis-12D-Hebbian-Transformer-ver.4.2/commit/401ab05714cd465009f49ba198e454e807149b91

The commit message publicly records:

- dual licensing;
- free/personal use;
- commercial licensing required for enterprise use;
- user documentation;
- roadmap material;
- contribution documentation.

### 2026-01-25 — architecture + security specification

Commit:

`22ed52fab102909cd350f3526414c1e50f4cfd9b`

Public commit URL:

https://github.com/NavisWORLD/The-Cosmic-Davis-12D-Hebbian-Transformer-ver.4.2/commit/22ed52fab102909cd350f3526414c1e50f4cfd9b

The commit message publicly records:

- system architecture diagrams;
- component interaction documentation;
- capability descriptions;
- performance specifications;
- security considerations.

These commits establish an independently timestamped public systems/licensing record before this provenance file existed.

---

## 2. Approval-gated implementation now present in COSMOS

The current public COSMOS-derived repository contains explicit approval-control implementation.

### A. Compliance policy gate

File:

`cosmos/compliance/policy_engine.py`

Public URL:

https://github.com/NavisWORLD/The-Cosmic-Davis-12D-Hebbian-Transformer-ver.4.2/blob/dddb1325b90c9abbe8da77974874e5770623035e/cosmos/compliance/policy_engine.py

GitHub code indexing surfaces `require_approval` behavior in this policy layer.

**Architectural role:** policy-controlled actions can be classified such that execution requires approval rather than proceeding automatically.

### B. Collaboration/session approval gate

File:

`cosmos/collaboration/sessions.py`

Public URL:

https://github.com/NavisWORLD/The-Cosmic-Davis-12D-Hebbian-Transformer-ver.4.2/blob/dddb1325b90c9abbe8da77974874e5770623035e/cosmos/collaboration/sessions.py

GitHub code indexing also surfaces `require_approval` behavior in the collaboration/session layer.

**Architectural role:** approval is not limited to a static policy document; it is represented in a live session/collaboration control path.

### C. Pending-approval / controlled-execution surfaces

GitHub indexing of the same repository surfaces approval/pending-approval behavior across additional subsystems, including:

- `cosmos/incidents/runbook_executor.py`
- network node/admin/configuration components;
- mesh routes;
- DEX/server components;
- remote web/server control;
- frontend/UI surfaces;
- repository documentation.

This matters because the pattern is broader than a single boolean or a single README sentence: approval-oriented control appears across execution, policy, networking, collaboration, incident response, remote control, and UI layers.

---

## 3. Functional pattern being preserved

The COSMOS pattern can be stated neutrally as:

1. an agent/system proposes or reaches an action boundary;
2. policy or context determines that approval is required;
3. the action is held/pending rather than executed automatically;
4. a human or authorized control path approves/rejects/resumes;
5. execution proceeds only after the gate condition is satisfied;
6. the control decision can be surfaced through system/session/UI layers.

This is the architectural pattern relevant to later comparisons involving interactive stopping, approval gates, gated writes, or human-authorized continuation in agent systems.

---

## 4. Hermes-side comparison scope

The Hermes Agent comparison should be performed at **commit and file granularity**, not by marketing language alone.

For each Hermes approval/stop/write-gate feature, preserve:

- first public issue/PR date;
- first merged commit SHA;
- first file containing the behavior;
- exact control semantics;
- whether the behavior is fail-open or fail-closed;
- whether approval occurs before tool execution, state mutation, memory write, shell/code execution, or continuation;
- whether the action can be stopped while running;
- whether human approval resumes the same execution context;
- whether the gate is policy-driven, UI-driven, or both.

### Comparison table

| Dimension | Earlier COSMOS evidence | Hermes evidence to compare |
|---|---|---|
| Human approval required | `require_approval` in `policy_engine.py` | first corresponding Hermes file/commit |
| Session-level approval | `require_approval` in `collaboration/sessions.py` | first corresponding Hermes session/control implementation |
| Pending execution state | indexed across runbook/network/UI surfaces | first Hermes pending/paused state implementation |
| Stop / pause control | broader COSMOS controlled-execution architecture | first Hermes interactive stop/pause implementation |
| Gated mutation/write | policy + approval-controlled actions | first Hermes write/memory gate implementation |
| Resume after approval | session/control architecture | first Hermes continuation/resume implementation |
| Auditability | repository-level policy, docs, multiple control surfaces | first Hermes audit/receipt/log implementation |

Rows on the Hermes side should be filled only with verifiable public SHAs/URLs.

---

## 5. Licensing chronology is a separate provenance axis

The licensing record should not be conflated with the technical gate comparison.

The January 25, 2026 COSMOS-family commit provides a public timestamp for Cory Davis's commercial-use boundary and enterprise licensing direction:

`401ab05714cd465009f49ba198e454e807149b91`

This does **not** mean a later project using a different license copied Cory's license. It means the licensing chronology is independently timestamped and should be preserved when reviewing commercial provenance alongside technical provenance.

---

## 6. Evidence hierarchy

For any future claim, use this order of evidence strength:

1. Git commit SHA with provider timestamp;
2. exact file at that SHA;
3. pull request / issue creation and merge timestamps;
4. tagged release;
5. DOI-backed archived artifact;
6. repository documentation;
7. screenshots or correspondence only as secondary corroboration.

Do **not** upgrade a hypothesis into a factual attribution merely because two systems later resemble one another.

---

## 7. Public provenance surfaces

Cory Davis / NavisWORLD:

- GitHub: https://github.com/NavisWORLD
- COSMOS: https://github.com/NavisWORLD/Cosmos
- Systems/Transformer repository: https://github.com/NavisWORLD/The-Cosmic-Davis-12D-Hebbian-Transformer-ver.4.2
- Portfolio: https://github.com/NavisWORLD/Cory-Davis-portfolio-
- Zenodo DOI: https://doi.org/10.5281/zenodo.17574447

Hermes fork containing this exhibit:

- https://github.com/NavisWORLD/hermes-agent

Existing provenance notice in this fork:

- `PROVENANCE_T2351.md`

---

## 8. What this timestamp proves

This commit proves only that, **no later than the GitHub timestamp of this commit**, the owner of this fork publicly recorded this specific comparison and linked it to the earlier COSMOS commit/file evidence above.

The earlier COSMOS commit SHAs remain the evidence for earlier dates. This new Hermes-fork commit must never be misrepresented as retroactively dating the underlying work.

That distinction is important: provenance should be aggressive about preserving evidence and conservative about what the evidence actually proves.

— Cory Davis
