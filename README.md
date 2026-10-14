# Blockchain-Integrated Accounting Framework (BIAF)


## Demonstration video

The current public repository contains project notes and release materials.  
The prototype demonstration video is available under the GitHub Releases section:

https://github.com/Blockchain-Integrated-Accounting/biaf-framework/releases/tag/v0.1.0

## Recognition

The BIAF paper received the Best Cutting-Edge Technology Paper Award at ENTRenova 2026.

## Overview

The **Blockchain-Integrated Accounting Framework (BIAF)** is a research-driven software framework exploring how blockchain-based transaction execution can be directly integrated with conventional double-entry accounting, financial reporting, taxation, audit, and supervisory controls.

BIAF connects commercial documents and their economic lifecycle — including issuance, counterparty acceptance, settlement, partial payments, credit notes, and refunds — with corresponding accounting records generated from verifiable blockchain events.

The framework is designed around a simple principle:

**blockchain records the economic event, while BIAF interprets that event through conventional accounting logic.**

The objective is not to replace established accounting standards or financial reporting practices, but to investigate whether blockchain infrastructure can provide a shared and verifiable transaction layer beneath them.

BIAF originated from academic research in accounting and has evolved into a functional EVM-based prototype developed and tested locally using a Hardhat blockchain environment.

---

## Motivation

Traditional accounting systems generally rely on:

- Separate databases maintained by individual organizations
- Post-hoc reconciliation between counterparties
- Manual or semi-automated controls
- Independent transaction, payment, and accounting records

Blockchain systems, by contrast, provide:

- Deterministic transaction execution
- Cryptographic authorization
- Immutable transaction histories
- Shared verification of state changes

However, blockchain transactions generally lack native accounting semantics.

BIAF investigates whether these two environments can be connected so that commercial transactions recorded through blockchain infrastructure can simultaneously become structured accounting events.

This approach may reduce:

- Reconciliation requirements
- Duplicate transaction recording
- Inconsistencies between commercial documents and payments
- Certain payment risks, such as incorrect payment amounts or destination wallets
- Delays between transaction execution and accounting recognition

It may also improve transaction information available to both businesses and individual consumers by linking commercial documents, counterparties, payment status, and accounting consequences within the same verifiable workflow.

---

## Current Prototype Capabilities

The current BIAF prototype supports a growing commercial and accounting transaction lifecycle.

### Commercial Documents

- Invoice issuance
- Receipt issuance
- Seller and buyer identification through blockchain wallets
- Buyer acceptance / cryptographic authorization
- Document status tracking
- Commercial document descriptions
- On-chain economic commitments

### Settlement

- Stablecoin-based settlement
- Full payments
- Partial payments
- Outstanding balance tracking
- Buyer-to-seller settlement
- Wallet-based transaction authorization

### Credit Notes and Refunds

BIAF now includes implemented and tested credit-note functionality, including:

- Credit-note issuance
- Association with original commercial documents
- Buyer-requested credit-note workflows
- Seller approval or rejection
- Credit application against eligible transactions
- Refund settlement
- Partial credit usage
- Remaining credit tracking
- Controls designed to prevent improper or duplicate credit use
- Corresponding seller and buyer accounting treatment

The current credit-note implementation has passed functional accounting and workflow testing, with additional independent testing continuing.

### Accounting Engine

BIAF automatically interprets blockchain events through conventional double-entry accounting logic.

Current accounting functionality includes:

- Seller-side journals
- Buyer-side journals
- Revenue recognition
- Inventory / expense recognition
- Accounts receivable
- Accounts payable
- VAT payable
- VAT claimable
- Bank / settlement accounts
- Credit-note accounting
- Refund accounting
- Partial settlement accounting

### Reporting

The prototype currently includes:

- Journal views
- Buyer and seller subledgers
- Trial balance generation
- VAT reporting
- Balance-sheet / financial reporting logic
- CSV and accounting-data exports

### Audit and Reconciliation

BIAF includes an experimental audit layer designed to compare blockchain events with accounting records.

Current functionality includes:

- Blockchain-to-accounting reconciliation
- Identification of missing accounting entries
- Review of document acceptance and settlement events
- Credit-note and refund audit logic
- Accounting consistency checks
- Audit-oriented transaction visibility

---

## Consumer and Transaction Safety

Although BIAF is primarily an accounting framework, its transaction architecture may also reduce certain operational risks for businesses and individual consumers.

By linking settlement directly to an identified commercial document and its counterparties, BIAF can reduce risks such as:

- Sending funds to an unintended wallet
- Paying an incorrect amount
- Settling the wrong commercial document
- Losing visibility over amounts already paid
- Uncertainty regarding remaining balances
- Separation between payment information and the underlying invoice or receipt

The objective is not to eliminate transaction risk entirely, but to provide better structured information and stronger cryptographic linkage between the commercial document, the parties, and the corresponding payment.

---

## Scope and Design Principles

BIAF is guided by several core principles.

### Accounting-First Design

Blockchain transactions are interpreted as economic and accounting events rather than merely technical state changes.

### Verifiable Commercial Relationships

Invoices, receipts, credit notes, payments, refunds, and related events are linked through identifiable transaction relationships.

### Human Authorization

Economically significant actions remain subject to cryptographic authorization through blockchain wallets.

### Compatibility With Established Accounting

BIAF is designed to integrate with conventional:

- Double-entry accounting
- Charts of accounts
- Tax reporting
- Financial statements
- Audit and reconciliation processes

The framework is intended to complement existing accounting standards rather than replace them.

### Modular Architecture

BIAF is being developed progressively so that blockchain execution, accounting logic, reporting, audit, and future external-system integrations can remain conceptually separable.

### Privacy-Aware Development

Not all commercial or accounting information should necessarily be stored directly on a public blockchain.

Future development will therefore continue to evaluate appropriate boundaries between:

- On-chain economic commitments
- Cryptographic proofs / hashes
- Off-chain commercial information
- Business identity information
- Personally identifiable information

---

## Current Development Focus

The next major development phase focuses on **detailed commercial documents, packing-list information, and inventory-system integration**.

The objective is to extend the current BIAF document model beyond aggregate transaction values and associate invoices and receipts with structured information such as:

- Individual goods or services
- Product descriptions
- Quantities
- Units of measurement
- Unit prices
- VAT treatment
- Vendor information
- Client information
- Delivery / commercial information

Rather than necessarily storing all detailed information directly on-chain, BIAF will investigate the use of cryptographic hashes or references that allow detailed commercial documents to be securely associated with their corresponding blockchain record.

This could allow a document to be independently verified while preserving scalability and appropriate privacy.

---

## Inventory-System Integration

Structured commercial-document information may also provide a bridge between BIAF and inventory-management systems.

A future integration could allow verified commercial events to produce corresponding inventory movements, for example:

- Seller invoice → inventory reduction
- Buyer goods receipt → inventory increase
- Credit note / return → corresponding inventory reversal

The current objective is **not to transform BIAF into a complete ERP or warehouse-management system**.

Instead, BIAF is intended to explore how blockchain-verified commercial events can communicate with existing inventory or ERP systems through adapters, APIs, or standardized event structures.

---

## Research Context

BIAF is informed by ongoing academic research into:

- Blockchain-integrated accounting systems
- Distributed ledger technology and financial reporting
- Automated accounting
- Auditability and reconciliation
- Internally generated intangible assets
- Human supervision of automated systems
- Blockchain-based commercial infrastructure

Two academic articles relating to the project are currently pending publication.

Links and full citations will be added to this repository following publication.

---

## Public Demonstration

The public repository includes material demonstrating the current BIAF prototype and its operating workflows.

The demonstration illustrates how commercial documents, blockchain transactions, settlement, and conventional accounting outputs interact within the framework.

Additional demonstrations will be added as new modules are completed.

---

## Development Roadmap

### Completed / Current Core Architecture

The prototype currently includes:

- Invoice and receipt workflows
- Buyer and seller wallet interaction
- Cryptographic document acceptance
- Stablecoin settlement
- Partial payments
- Automated journal generation
- Accounts receivable and payable
- VAT accounting
- Trial balance generation
- Financial reporting logic
- Audit and reconciliation functionality
- CSV / accounting-data export
- Credit notes
- Credit application
- Refund workflows
- Credit-note accounting and audit logic

Additional independent testing of the existing implementation is ongoing.

---

### Phase 1 — Detailed Commercial Documents, Packing Lists and Inventory Integration

Develop structured commercial-document information associated with BIAF invoices and receipts.

Planned areas include:

- Goods and service descriptions
- Quantities and unit values
- VAT information
- Vendor and customer information
- Packing-list / delivery information
- Cryptographic association between detailed off-chain documents and blockchain records
- Document-integrity verification
- Conceptual and technical integration with external inventory-management systems

---

### Phase 2 — Equity and Corporate Accounting

Extend BIAF beyond commercial transactions into corporate and equity-related accounting.

Potential areas include:

- Corporate incorporation records
- Shareholder accounts / wallet identities
- Capital contributions
- Share issuance
- Ownership changes
- Equity transactions
- Distributions
- Related journal and reporting logic

The objective is to explore how verifiable corporate events can be connected to conventional equity accounting.

---

### Phase 3 — Payroll and Employee Accounting

Develop payroll-related transaction and accounting workflows.

Potential areas include:

- Salary expenses
- Employee liabilities
- Payroll settlement
- Taxes and deductions
- Employer obligations
- Corresponding accounting entries

Because payroll involves sensitive personal information, privacy and appropriate separation between public blockchain data and confidential employee information will be central design requirements.

---

### Phase 4 — Public Testnet Deployment

Following completion and validation of the major accounting modules, BIAF will move from its current local Hardhat environment to suitable public blockchain testnets.

Candidate infrastructure will be evaluated according to criteria including:

- Low transaction costs
- Transaction throughput
- EVM compatibility where advantageous
- Stablecoin infrastructure
- Wallet ecosystem
- Privacy and identity capabilities
- Developer tooling
- Suitability for commercial and accounting transaction volumes

The public-testnet phase will allow the framework to be evaluated under real blockchain-network conditions.

---

### Phase 5 — AI-Agent Integration

Once the underlying commercial and accounting architecture has matured and has been tested on public infrastructure, BIAF will investigate AI-agent integration.

Potential agent functions include:

- Procurement operations
- Sales processing
- Commercial-document preparation
- Transaction preparation
- Accounting classification
- Reconciliation
- Audit assistance
- Financial monitoring

AI agents are envisioned as operational participants rather than unrestricted autonomous actors.

Economically significant actions would remain subject to identifiable human supervision through mechanisms such as:

- Wallet signatures
- Cryptographic approvals
- Role-based permissions
- Transaction limits
- Human review

The objective is to combine machine-driven operational efficiency with identifiable human responsibility and auditability.

---

## Longer-Term Direction

The long-term objective of BIAF is to progressively expand blockchain-integrated accounting across the major components of a conventional accounting system.

This includes:

- Current assets
- Fixed assets
- Inventory
- Receivables
- Cash and settlement accounts
- Liabilities
- Equity
- Revenue
- Expenses
- Payroll
- Taxation
- Financial reporting
- Audit and reconciliation

The broader research question is whether blockchain infrastructure can become a verifiable economic-event layer beneath conventional accounting systems without requiring businesses to abandon established accounting principles, reporting structures, or supervisory controls.

---

## Repository Structure and Disclosure

This repository serves as the public development and research repository for BIAF.

It contains or will progressively contain:

- Prototype source code
- Smart-contract implementations
- User-interface components
- Accounting-engine components
- Architecture documentation
- Demonstration material
- Research context
- Development roadmap
- Testing material
- Future public-testnet implementations

The framework remains under active development, and individual components may be refactored or reorganized as the architecture evolves.

---

## Status

BIAF is an **active research and development project with a functional working prototype**.

The project has moved beyond its initial invoice-and-settlement proof of concept and currently supports a substantially broader commercial, accounting, reporting, credit-note, and audit workflow.

The current development focus is the integration of richer commercial-document information and inventory-related functionality.

Interfaces, architecture, accounting mappings, and implementation details may continue to evolve as the framework expands and undergoes further testing.

---

## License

Licensing arrangements for BIAF and its individual components remain under evaluation as the project develops.

Unless explicitly stated otherwise in a component-specific license, publication of source code in this repository should not be interpreted as granting rights beyond those provided by the applicable repository or file-level license.
