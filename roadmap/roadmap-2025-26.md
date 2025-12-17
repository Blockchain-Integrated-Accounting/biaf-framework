# BIAF Roadmap – 2025 (Q4 Baseline) and Forward Plan

## Overview

This document outlines the near-term roadmap for the **Blockchain-Integrated Accounting Framework (BIAF)** starting from **late Q4 2025**, with planned milestones extending into 2026.

BIAF is a **research-driven, experimental framework** supported by a working prototype. The roadmap emphasizes:
- documentation-first clarity,
- progressive open-source release,
- accounting correctness,
- secure supervision (human + cryptographic authorization),
- and practical interoperability with traditional accounting workflows.

---

## Current Status (Baseline – late Q4 2025)

As of late Q4 2025, BIAF includes:
- A functional prototype supporting invoice issuance, settlement, and ledger recording
- Ethereum-based transaction execution and buyer–seller interaction flows
- Wallet-based authorization and supervision concepts
- Accounting-aware transaction mapping (double-entry logic)
- Ongoing testing, UX iteration, and security hardening considerations

Public GitHub presence has been established to host:
- conceptual documentation,
- architecture and process descriptions,
- and an execution roadmap.

---

## 2025 Q4 — Public Documentation Foundation (Completion)

**Objectives**
- Establish a stable public “front door” for reviewers and collaborators
- Publish non-sensitive documentation suitable for grant review

**Deliverables**
- Public repository with:
  - README (project overview, scope, status, disclosure strategy)
  - Roadmap (this document)
  - Initial architecture note (high-level actors and components)
- Conservative disclosure policy:
  - documentation public,
  - functional code released progressively when stabilized

**Notes**
- No requirement to publish functional smart contract/UI code in 2025 Q4
- Focus: clarity, credibility, readiness for funding review

---

## 2026 Q1 — Architecture & Specification Stabilization

**Objectives**
- Convert prototype knowledge into stable, reviewable specifications
- Define module boundaries to enable staged publication

**Deliverables**
- System architecture document (on-chain vs off-chain responsibilities)
- Actor and permission model:
  - seller, buyer, supervisor, AI agent roles
- Data model and event semantics (what must be emitted on-chain for accounting interpretation)
- Threat model (high-level) and security assumptions

---

## 2026 Q1–Q2 — Core Smart Contract Modules (Experimental Release)

**Objectives**
- Isolate and stabilize core accounting-relevant smart contract logic
- Prepare selected components for public experimental release

**Deliverables**
- Experimental contract modules for:
  - invoice representation
  - payment execution
  - event emission for accounting interpretation
- Minimal test suite and testnet examples
- Documentation of assumptions, limitations, and intended use

**Notes**
- Released as *experimental* and *unaudited*
- Intended for research, demos, and controlled testing—not production

---

## 2026 Q2–Q3 — Accounting Coverage Expansion

**Objectives**
- Expand accounting scope beyond basic trade flows
- Improve mapping coverage to real-world accounting systems

**Deliverables**
- Expanded journal-entry mapping logic and documentation for additional categories, e.g.:
  - current assets
  - liabilities
  - equity-related events (conceptual scope and constraints)
- Documentation: accounting treatment assumptions and chart-of-accounts approach
- Examples of transaction-to-ledger mappings for additional event types

**Notes**
- Focus on conceptual correctness and transparency
- No claim of jurisdiction-specific regulatory compliance

---

## 2026 Q3 — AI Assistance and Supervised Automation (Exploratory)

**Objectives**
- Explore the role of AI-assisted tooling within the framework
- Maintain strict human supervision and accountability
- Avoid assumptions about autonomous execution or external AI infrastructures

**Deliverables**
- Conceptual documentation of potential AI-assisted use cases, such as:
  - transaction classification suggestions
  - accounting entry assistance
  - workflow support for procurement or sales operations
- Description of supervision-first execution principles:
  - all economically relevant actions remain subject to explicit human approval
  - cryptographic signatures define responsibility boundaries
- Clear separation between:
  - decision support (AI-assisted)
  - execution authority (human-controlled)

**Notes**
- AI components are treated as optional, exploratory, and non-essential
- No dependency on specific AI networks, protocols, or external initiatives
- No autonomous agent assumptions
- Implementation details may remain conceptual at this stage


---

## 2026 Q3–Q4 — Off-Chain Integration and Reporting

**Objectives**
- Bridge on-chain execution with traditional accounting workflows and reporting artifacts

**Deliverables**
- Off-chain ledger export formats (e.g., CSV/JSON schemas suitable for import)
- Prototype reporting outputs (trial balance / basic statements as demonstrators)
- Documentation of reconciliation logic and data integrity checks
- Interfaces/adapter approach for ERP/accounting software integration

---

## 2026 Q4 — Scaling and Network Considerations

**Objectives**
- Evaluate scalability and cost efficiency for broader experimentation
- Prepare deployment options beyond L1-only assumptions

**Deliverables**
- Layer 2 exploration plan and proof-of-concept integration (where appropriate)
- Gas cost analysis and benchmarking methodology
- Updated deployment architecture recommendations
- Revised roadmap for subsequent phases (2027+)

---

## Open-Source Strategy

BIAF follows a **progressive open-source** strategy:
- Documentation-first
- Modular, staged publication of code
- Clear maturity labels (experimental vs stable)
- No production claims without review/audit

Licensing decisions will be finalized as code components are released.

---

## Risks and Limitations

- Accounting requirements vary by jurisdiction and entity type
- Blockchain execution costs may constrain certain transaction classes
- Secure AI-agent operation requires explicit supervision boundaries
- No immediate production or regulatory guarantees are implied

These constraints are treated as research parameters guiding careful iteration.

---

## Long-Term Vision

BIAF aims to contribute to:
- accounting-aware blockchain applications,
- verifiable audit trails and supervisory controls,
- responsible AI-assisted financial operations,
- and open research at the intersection of accounting and decentralized systems.
