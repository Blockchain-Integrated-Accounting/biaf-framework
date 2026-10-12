# BIAF Roadmap – 2026–2027 Development Plan

## Overview

This document outlines the current and forward development roadmap for the **Blockchain-Integrated Accounting Framework (BIAF)**.

BIAF is a **research-driven, experimental framework supported by a functional working prototype**. The project has progressed beyond its original invoice-and-settlement proof of concept and now includes broader accounting, reporting, audit, and credit-note functionality.

The roadmap emphasizes:

- accounting correctness,
- verifiable commercial transaction flows,
- cryptographic authorization,
- progressive expansion of accounting scope,
- integration with traditional accounting and operational systems,
- privacy-aware system design,
- public blockchain deployment,
- and, at a later stage, supervised AI-agent integration.

The current development sequence is:

**Credit-note completion and validation → detailed commercial documents / packing lists and inventory integration → equity module → payroll module → public testnet deployment → AI-agent integration**

---

## Current Status – Q4 2026

As of Q4 2026, BIAF includes a substantially expanded functional prototype.

### Core Commercial Workflow

The current system supports:

- Invoice issuance
- Receipt issuance
- Seller and buyer wallet identification
- Buyer acceptance / cryptographic authorization
- Stablecoin-based settlement
- Full payments
- Partial payments
- Outstanding balance tracking
- Document status management
- Buyer and seller transaction views

### Accounting Functionality

The framework currently supports automated accounting treatment for major trade flows, including:

- Seller-side journals
- Buyer-side journals
- Revenue recognition
- Inventory / expense recognition
- Accounts receivable
- Accounts payable
- VAT payable
- VAT claimable
- Bank / settlement accounts
- Partial settlement accounting

### Reporting

Current reporting capabilities include:

- Journal views
- Buyer and seller subledgers
- Trial balance generation
- VAT reporting
- Balance-sheet / financial reporting logic
- CSV and accounting-data export

### Audit and Reconciliation

BIAF currently includes an experimental audit and reconciliation layer supporting:

- Blockchain-to-accounting reconciliation
- Detection of missing accounting entries
- Review of commercial-document acceptance
- Review of settlement events
- Accounting consistency checks
- Audit-oriented transaction visibility

### Credit Notes and Refunds

Credit-note and refund functionality has now been implemented and validated within the current BIAF workflow.

The implementation includes:

- Credit-note issuance
- Association with original commercial documents
- Buyer-requested credit-note workflows
- Seller approval / rejection
- Credit application
- Partial credit usage
- Remaining credit tracking
- Refund settlement
- Controls against improper or duplicate credit use
- Corresponding buyer and seller accounting treatment
- Credit-note journal logic
- Audit treatment
- Export / reporting support

Additional independent testing of this functionality is ongoing.

---

## Q4 2026 — Detailed Commercial Documents, Packing Lists and Inventory Integration

### Objectives

The next major development phase is to expand the current BIAF document model beyond aggregate accounting values.

The objective is to create a richer commercial-document layer while preserving the existing blockchain-accounting architecture.

### Planned Functionality

Detailed invoice / receipt information may include:

- Individual goods or services
- Product / service descriptions
- Quantities
- Units of measurement
- Unit prices
- VAT treatment
- Vendor details
- Customer details
- Commercial registration information
- Delivery information
- Packing-list data
- Additional commercial-document metadata

### Cryptographic Association

The current design direction is to avoid storing all detailed commercial information directly on a public blockchain.

Instead, BIAF will investigate:

- Structured off-chain commercial documents
- Cryptographic document hashes
- On-chain document references
- Integrity verification
- Immutable association between the detailed document and the corresponding blockchain transaction

The objective is to allow users and auditors to verify that a detailed commercial document has not been modified after being associated with the blockchain record.

### Inventory Integration

The same structured line-item information may support integration with external inventory-management systems.

Potential event flows include:

- Seller invoice → inventory reduction
- Buyer receipt / acceptance → inventory increase
- Credit note → inventory reversal
- Returned goods → corresponding inventory adjustment

The current objective is not to transform BIAF into a complete ERP or warehouse-management system.

Instead, BIAF will investigate adapter- or API-based integration with existing inventory systems.

---

## Q4 2026 – Q1 2027 — Equity and Corporate Accounting Module

### Objectives

The next accounting expansion will focus on corporate equity and ownership-related events.

### Planned Areas

Potential functionality includes:

- Corporate incorporation-related records
- Shareholder accounts / wallet identities
- Capital contributions
- Share issuance
- Ownership changes
- Shareholder transactions
- Capital increases
- Capital reductions
- Distributions
- Dividend-related accounting
- Equity-account movements
- Corresponding journal entries
- Reporting integration

### Design Considerations

This module will require particular attention to:

- Identity
- Ownership
- Authorization
- Corporate governance
- Privacy
- On-chain vs off-chain information boundaries

The objective is to connect verifiable corporate events with conventional equity accounting without unnecessarily exposing confidential corporate information.

---

## Q1 2027 — Payroll and Employee Accounting

### Objectives

Expand BIAF into payroll-related accounting and settlement workflows.

### Planned Functionality

Potential areas include:

- Salary expenses
- Employee liabilities
- Payroll settlement
- Taxes and deductions
- Employer obligations
- Payroll-related journal entries
- Payment status
- Reporting integration

### Privacy Considerations

Payroll is expected to require a significantly stronger privacy boundary than ordinary commercial invoices.

The design will therefore investigate:

- Selective disclosure
- Off-chain employee information
- Cryptographic references
- Role-based access
- Separation between public transaction data and sensitive personal information

No assumption is made that payroll data should be directly visible on a public blockchain.

---

## February–March 2027 — Public Testnet Deployment

### Objective

Between **February 2027 and March 2027**, BIAF is planned to move from local Hardhat-based blockchain testing to one or more suitable public blockchain testnets.

This will represent a major transition from local experimentation to public-network validation.

### Deployment Goals

The public-testnet phase will test:

- Smart-contract behavior under real network conditions
- Stablecoin or token settlement
- Wallet interaction
- Commercial-document issuance
- Document acceptance
- Partial and full settlement
- Credit notes and refunds
- Accounting-event generation
- Audit and reconciliation
- Transaction costs
- Network latency
- Scalability
- User workflow reliability

### Network Selection Criteria

Candidate blockchain environments will be assessed according to:

- Low transaction costs
- EVM compatibility where advantageous
- Stablecoin availability
- Wallet ecosystem
- Transaction throughput
- Privacy and identity capabilities
- Developer tooling
- Network stability
- Ecosystem support
- Suitability for accounting and commercial transaction volumes

The framework is intended to remain conceptually blockchain-agnostic where possible.

---

## Q2 2027 — Public Testnet Evaluation and Architecture Refinement

### Objectives

Following public testnet deployment, BIAF will enter a structured evaluation period.

### Planned Activities

- Transaction-cost benchmarking
- Performance evaluation
- Stability testing
- Security review
- User-flow evaluation
- Accounting consistency validation
- Public-network audit testing
- Documentation refinement
- Deployment architecture review

This phase may also include comparison between alternative blockchain environments.

---

## Q2–Q3 2027 — AI-Agent Integration

### Objectives

AI-agent integration is planned **after the underlying accounting and transaction infrastructure has matured and been tested on public blockchain infrastructure**.

The aim is to avoid building agent automation on top of an unstable accounting architecture.

### Potential AI-Agent Roles

Future AI agents may assist with:

- Procurement operations
- Sales processing
- Commercial-document preparation
- Transaction preparation
- Accounting classification
- Journal-entry suggestions
- Reconciliation
- Audit assistance
- Financial monitoring
- Operational exception detection

### Human Supervision

AI agents are not intended to have unrestricted autonomous financial authority.

Economically significant actions should remain subject to identifiable human supervision through mechanisms such as:

- Wallet-based approvals
- Cryptographic signatures
- Role-based permissions
- Transaction limits
- Human review
- Explicit delegation

The intended model is:

**AI-assisted operation with human-controlled execution authority.**

---

## Longer-Term Accounting Expansion

Following the major modules above, BIAF is intended to progressively expand toward broader accounting-system coverage.

Potential future areas include:

- Fixed assets
- Depreciation
- Intangible assets
- Inventory
- Cash and bank accounts
- Receivables
- Payables
- Provisions
- Accruals
- Deferrals
- Taxation
- Financing transactions
- Equity
- Revenue
- Expenses
- Payroll
- Financial statements
- Consolidation-related logic
- Audit and assurance workflows

The long-term objective is to explore whether a large portion of conventional accounting can be driven by verifiable blockchain-based economic events.

---

## Off-Chain Integration and Interoperability

BIAF will continue to investigate interoperability with conventional systems.

Potential integration targets include:

- Inventory-management systems
- ERP systems
- Accounting software
- Tax-reporting systems
- Banking / payment infrastructure
- Document-management systems
- Audit tools

The preferred architectural direction is modular integration through:

- APIs
- Structured event formats
- Export schemas
- Adapters
- Cryptographic document references

The objective is interoperability rather than replacement of existing enterprise systems.

---

## Privacy and Identity

Privacy will become increasingly important as BIAF expands beyond basic commercial transactions.

Areas requiring particular consideration include:

- Individual / natural-person transactions
- Payroll
- Shareholder identity
- Corporate ownership
- VAT / tax identification
- Commercial registration information
- Physical addresses
- Beneficial ownership information
- Sensitive financial data

Future research will investigate mechanisms allowing a participant to prove relevant attributes without unnecessarily exposing the underlying data.

Potential approaches may include:

- Verifiable credentials
- Selective disclosure
- Cryptographic attestations
- Zero-knowledge mechanisms
- Permissioned data layers
- Off-chain identity records linked to on-chain proofs

---

## Security and Review

As BIAF approaches public-testnet deployment, security review will become increasingly important.

Priority review areas include:

- Smart-contract authorization
- Payment routing
- Stablecoin interaction
- Document ownership
- Buyer / seller authorization
- Credit-note application
- Refund logic
- Prevention of duplicate or improper credit use
- Wallet permissions
- Event integrity
- Accounting-event consistency

Formal external review or audit will be considered before any production-oriented deployment.

---

## Research and Publication

BIAF remains both a software-development project and an accounting research project.

Research areas include:

- Blockchain-integrated accounting
- Verifiable accounting records
- Real-time reconciliation
- Digital commercial documents
- Auditability
- Accounting automation
- Internally generated intangible assets
- Privacy in blockchain accounting
- Human-supervised AI financial operations

Two academic articles relating to the project are currently pending publication.

Following publication, citations and links will be added to the public repository.

---

## Open-Source and Disclosure Strategy

BIAF follows a **progressive publication and disclosure strategy**.

The project currently emphasizes:

- Public documentation
- Public demonstrations
- Progressive publication of stable components
- Clear separation between experimental and production-ready functionality
- Preservation of licensing flexibility while the framework remains under active development

Licensing decisions will continue to be evaluated as additional modules are released.

---

## Risks and Limitations

BIAF remains an experimental research framework.

Current limitations include:

- Accounting requirements vary by jurisdiction
- Tax treatment differs across legal systems
- Public blockchains create privacy challenges
- Transaction fees may affect economic feasibility
- Smart-contract security remains critical
- Identity integration is not yet finalized
- External ERP / inventory integration remains experimental
- AI-agent execution introduces additional authorization and supervision risks
- Public-testnet performance may differ from local testing

These limitations are treated as research parameters rather than ignored assumptions.

---

## Long-Term Vision

BIAF aims to contribute to the development of:

- Accounting-aware blockchain applications
- Verifiable commercial transaction systems
- Reduced reconciliation requirements
- Improved auditability
- Stronger links between economic events and accounting records
- Privacy-aware business identity
- Cryptographically supervised financial workflows
- Integration between blockchain and traditional enterprise systems
- Responsible AI-assisted financial operations

The broader objective is to investigate whether blockchain infrastructure can become a **verifiable economic-event layer beneath conventional accounting systems**, while preserving familiar accounting standards, reporting structures, organizational control, and human responsibility.
