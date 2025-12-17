# BIAF System Architecture

## Purpose of This Document

This document provides a **high-level architectural overview** of the Blockchain-Integrated Accounting Framework (BIAF).

The goal is to describe:
- the main system components,
- their responsibilities,
- and their interactions,

without committing to a fixed implementation or production-ready design.

BIAF is an **experimental and research-oriented framework**, and the architecture described here is intended to support clarity, reviewability, and progressive refinement.

---
### Asset Denomination and Prototype Variants

BIAF has been explored through multiple prototype configurations that share the same architectural principles but differ in asset denomination.

Current experimental implementations include:
- an ETH-denominated configuration, where transaction execution, settlement, and unit of account are native to ETH, and
- a stable-denominated configuration, where a fiat-referenced token (e.g. USDC) is used as the unit of account and settlement asset, while Ethereum provides execution, finality, and metadata.

These variants are used to study how accounting interpretation, valuation stability, and reporting logic behave under different monetary assumptions, without altering the core framework architecture.
Both configurations share identical accounting interpretation logic; only the unit of account and settlement asset differ.

## Architectural Principles

BIAF is guided by the following architectural principles:

- **Accounting-aware design**  
  Blockchain transactions are interpreted as economic events with accounting meaning, not merely state changes.

- **Separation of concerns**  
  Execution, interpretation, supervision, and reporting are treated as distinct layers.

- **Human accountability**  
  Final execution authority remains with human-controlled cryptographic identities (wallets).

- **Progressive disclosure**  
  Components are documented and released incrementally as they stabilize.


---

## High-Level Component Overview

At a high level, BIAF consists of the following layers:

1. **On-chain execution layer**
2. **Accounting interpretation layer**
3. **Supervision and authorization layer**
4. **Off-chain accounting and reporting layer**
5. **User interfaces (experimental)**

Each layer is described below.

---

## 1. On-Chain Execution Layer

### Role

The on-chain layer is responsible for:
- representing transactional state,
- enforcing execution rules,
- and providing cryptographically verifiable records.

### Typical responsibilities include:
- invoice representation
- payment execution
- emitting structured events for off-chain interpretation

### Design constraints
- Deterministic execution
- Minimal accounting logic embedded on-chain
- Clear event semantics for downstream processing

The on-chain layer **does not attempt** to replicate full accounting systems.

---

## 2. Accounting Interpretation Layer

### Role

This layer maps on-chain events to **accounting-relevant representations**, such as:
- journal entries
- account balances
- transaction classifications

### Characteristics
- May operate off-chain
- Uses on-chain data as an authoritative source
- Applies predefined accounting rules and mappings

This layer is where:
- double-entry logic is applied,
- chart-of-accounts mappings are defined,
- accounting assumptions are made explicit and auditable.

---

## 3. Supervision and Authorization Layer

### Role

BIAF emphasizes **explicit supervision** over autonomous execution.

This layer governs:
- who is allowed to initiate actions,
- who must approve them,
- and how responsibility is assigned.

### Core concepts
- Wallets represent accountable actors
- Cryptographic signatures express consent and authority
- Roles (e.g. seller, buyer, supervisor) constrain permissible actions

All economically meaningful actions are intended to be:
- attributable,
- reviewable,
- and non-anonymous within the system’s context.

---

## 4. Off-Chain Accounting and Reporting Layer

### Role

This layer bridges blockchain execution with traditional accounting workflows.

### Responsibilities may include:
- maintaining an off-chain ledger mirror
- exporting accounting data in standard formats
- supporting reconciliation and reporting processes

This layer is designed to:
- integrate with existing accounting tools,
- not replace established ERP or reporting systems.

---

## 5. User Interfaces (Experimental)

### Role

User interfaces provide:
- visibility into transactions and ledger entries,
- interaction with on-chain execution,
- supervision and approval workflows.

### Characteristics
- Experimental and subject to change
- Intended for demonstration and testing
- Not production-grade at the current stage

Different interfaces may exist for:
- sellers,
- buyers,
- supervisory roles.

---

## On-Chain vs Off-Chain Responsibilities

BIAF deliberately avoids overloading the blockchain with accounting logic.

| Function                          | On-Chain | Off-Chain |
|----------------------------------|----------|-----------|
| Transaction execution            | ✔        |           |
| State finality                   | ✔        |           |
| Event emission                   | ✔        |           |
| Journal entry construction       |          | ✔         |
| Chart of accounts mapping        |          | ✔         |
| Financial statement preparation  |          | ✔         |

This separation supports flexibility, scalability, and auditability.

---

## Extensibility and Future Considerations

The architecture is designed to allow future extensions, including:
- expanded accounting coverage,
- additional supervision models,
- optional AI-assisted tooling,
- Layer 2 deployment scenarios.

Such extensions are **non-mandatory** and subject to further research and validation.

---

## Limitations

- The framework does not claim regulatory compliance.
- Accounting interpretations depend on explicit assumptions.
- Jurisdiction-specific requirements are out of scope at this stage.
- Security and correctness require ongoing review.

---

## Status

This architecture description reflects the **current research understanding** of the BIAF system.

It is expected to evolve as:
- documentation improves,
- components are released,
- and feedback is incorporated.
