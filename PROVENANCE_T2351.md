# Provenance Record — COSMOS / Hermes Agent Comparison

**Recorded:** 2026-08-15  
**Nous support reference:** `T-2351`  
**Purpose:** Preserve a public, reviewable pointer from this fork to earlier timestamped COSMOS artifacts that may be relevant when comparing approval-gated / human-in-the-loop agent architectures.

> This file is a provenance notice, not an allegation of copying or access. Similarity alone does not establish derivation. The relevant question is chronology, and the underlying Git history should be reviewed at commit/file granularity.

## Earlier public COSMOS licensing / architecture record

Repository:

- https://github.com/NavisWORLD/The-Cosmic-Davis-12D-Hebbian-Transformer-ver.4.2

Public commit dated **2026-01-25**:

- `401ab05714cd465009f49ba198e454e807149b91`
- Commit message documents a dual-license structure with commercial licensing required for enterprise use, plus user documentation and roadmap material.
- https://github.com/NavisWORLD/The-Cosmic-Davis-12D-Hebbian-Transformer-ver.4.2/commit/401ab05714cd465009f49ba198e454e807149b91

A technical-specification commit followed the same day:

- `22ed52fab102909cd350f3526414c1e50f4cfd9b`
- The commit message describes system architecture, component interactions, capabilities, performance specifications, and security considerations.
- https://github.com/NavisWORLD/The-Cosmic-Davis-12D-Hebbian-Transformer-ver.4.2/commit/22ed52fab102909cd350f3526414c1e50f4cfd9b

## Approval-gated implementation currently indexed in COSMOS

GitHub code search surfaces approval-related implementation in the public COSMOS repository, including:

### Compliance policy engine

`cosmos/compliance/policy_engine.py`

https://github.com/NavisWORLD/The-Cosmic-Davis-12D-Hebbian-Transformer-ver.4.2/blob/dddb1325b90c9abbe8da77974874e5770623035e/cosmos/compliance/policy_engine.py

The indexed implementation includes `require_approval` behavior.

### Collaboration sessions

`cosmos/collaboration/sessions.py`

https://github.com/NavisWORLD/The-Cosmic-Davis-12D-Hebbian-Transformer-ver.4.2/blob/dddb1325b90c9abbe8da77974874e5770623035e/cosmos/collaboration/sessions.py

The indexed implementation also includes `require_approval` behavior.

### Additional approval / pending-approval surfaces

The same public codebase indexes approval-related behavior across components including:

- incident runbook execution
- network node / admin / configuration
- mesh routes
- DEX/server components
- remote web server
- frontend/UI surfaces
- documentation

The important provenance task is to trace each specific file to the first commit in which its approval-gated behavior appeared.

## Why this record exists in the Hermes fork

Recent Hermes Agent development has included work around interactive stopping, approvals, gated actions, and staged write/approval concepts. Those are sufficiently close in architectural theme to make a clean chronology comparison useful.

This fork-level record exists so the comparison cannot later depend on memory, screenshots, or private correspondence. The primary evidence remains the original repositories, commit SHAs, file histories, and DOI-backed/public research artifacts.

## Claim boundary

This record does **not** claim that Nous Research copied COSMOS, saw COSMOS before implementing its own work, or derived Hermes Agent features from Cory Davis's code. Establishing any such claim would require evidence beyond architectural similarity and public chronology.

It **does** establish a dated public pointer, as of 2026-08-15, to earlier COSMOS artifacts that should be included in any serious chronology/provenance review.

## Public provenance surfaces

- GitHub: https://github.com/NavisWORLD
- COSMOS: https://github.com/NavisWORLD/Cosmos
- Transformer / systems repository: https://github.com/NavisWORLD/The-Cosmic-Davis-12D-Hebbian-Transformer-ver.4.2
- Portfolio: https://github.com/NavisWORLD/Cory-Davis-portfolio-
- Zenodo DOI: https://doi.org/10.5281/zenodo.17574447

— Cory Davis
