# Blockchain-Integrated Accounting Framework (BIAF)

**Verifiable accounting from blockchain events, with local records and optional on-chain declarations.**

BIAF is a research project exploring how commercial transactions recorded on a blockchain can be interpreted through conventional double-entry accounting. Its working prototype links invoices, receipts, acceptance, USDC payments, credit notes and refunds with buyer and seller journals, reports and reconciliation checks.

The blockchain preserves transaction history; accounting interpretation remains a distinct layer. Credit notes record subsequent returns and discounts without rewriting earlier events.

## Project status

**V4 functional scope implemented; release documentation and repository review in progress as of 2 November 2026.** The prototype runs in a local Hardhat environment. Functional checks have been performed during development; independent testing and feedback remain part of the release process. This is experimental research software, not a production-audited accounting product.

V4 extends the earlier commercial and settlement workflows with off-chain packing lists, cryptographically linked supporting PDFs, inventory valuations, local inventory postings and optional inventory Blockchain Domain Expansion (BDE).

## Demonstration and research

The existing prototype demonstration is available in [GitHub Releases](https://github.com/Blockchain-Integrated-Accounting/biaf-framework/releases/tag/v0.1.0). It illustrates the version recorded at that time and should not be read as a demonstration of every later V4 feature.

The BIAF paper received the **Best Cutting-Edge Technology Paper Award at ENTRenova 2026**. Publication links and full citations will be added when available.

## Current capabilities

| Area | Implemented prototype scope |
| --- | --- |
| Commercial documents | Wallet-based invoice and receipt issuance, per-seller document identities, document status and counterparty acknowledgment where required |
| Settlement | USDC payments, partial payments, outstanding balances and document-linked settlement |
| Credit notes | Buyer-requested and seller-initiated routes, approval/rejection, credit allocation, eligible refunds, remaining-credit tracking and corresponding accounting/audit logic |
| Supporting documents | Goods/service catalogue and drafts; locally prepared packing-list or service-detail PDFs for invoices, receipts and supported credit-note workflows |
| PDF verification | The exact PDF hash is committed at issuance; importing a different file fails even if its amounts match. Business details are captured from the local registry |
| Accounting | Buyer/seller journals, receivables/payables, VAT treatment, purchase classification, inventory-category reclassification, credit and payment entries |
| Inventory | Approved opening/adoption and closing valuations, version history, prior-closing carry-forward, explicit zero values, external valuation JSON input and reviewed local opening/closing postings |
| Reporting | Journal and counterparty views, trial balance, VAT report, P&L with periodic COGS, and a balance sheet based on posted journals |
| Optional BDE | On-chain publication and verification of approved aggregate inventory valuations, separate from local approval and journal posting |
| Review and backup | Audit checks, CSV reporting exports, scoped JSON backups/restoration, and exact original-PDF downloads |

### Packing lists and PDFs

Detailed item descriptions, quantities, units, prices and supporting business information stay in local files. The blockchain records the attachment commitment rather than the complete PDF.

A prepared PDF freezes its supporting draft. The seller may discard an unissued draft/PDF pair after the application checks its live issuance status; issued attachments remain unchanged. Buyer acknowledgment of a committed invoice PDF is distinct from payment. Receipt payment does not attest PDF review, and credit-note acknowledgment depends on the credit route.

The PDF's printed attachment reference helps users distinguish files. A written cross-reference to a commercial document is a navigation aid; verification still depends on the exact committed file hash. Hash verification establishes file integrity and association, not that goods were physically delivered or that the stated values are correct.

### Inventory and financial reporting

V4 accepts valuations supported by stocktaking or external calculations. Users declare the valuation method; BIAF does not calculate FIFO, weighted-average cost or LIFO, or validate their suitability for a reporting basis.

Approved valuations can supply the periodic COGS calculation. Separate reviewed postings reconcile journal inventory to the approved opening/closing categories. Local approval and optional BDE do not themselves create journal entries. Consequently, an approved valuation may affect the valuation-based P&L calculation before it appears in the posted-journal balance sheet; the application displays reconciliation information.

The inventory categories support aggregate accounting analysis. They are not a perpetual quantity-based warehouse system, and V4 does not automatically generate physical stock movements from packing-list lines.

## Blockchain Domain Expansion

BDE is the optional extension of blockchain records beyond transactional events to declared accounting values.

- **Available in V4:** aggregate inventory valuation declarations, with entity, period, balance type, registration time and version relationships. Category values, supporting notes and the declared valuation method remain local.
- **Planned:** optional BDE publication for equity, balance sheet, P&L and fixed assets. These publication workflows are not implemented in V4. Existing local financial reports are separate from future on-chain publication.

The black-and-gold monk marks optional BDE actions; the white monk marks off-chain exports. A wallet signature attributes a declaration to a wallet. It is not independent audit assurance or a guarantee of real-world accuracy.

## Design principles and boundaries

- **Accounting first:** supported economic events are interpreted through explicit accounting rules and mappings.
- **Human authorization:** on-chain actions require wallet authorization; local approvals and classification choices remain visible accounting decisions.
- **On-chain/off-chain separation:** execution, commitments and optional declarations are separated from local journals, business details, documents and reports.
- **Traceable adjustments:** credit notes preserve the commercial history; valuation replacement retains earlier approved versions and local posting corrections use reviewed differences.
- **Local operation:** the current UI and its records run locally. Blockchain commitments do not back up the local PDF files or all accounting choices.
- **Interoperability as a development direction:** CSV/JSON exports support review, backup and further processing. Direct ERP import requires system-specific mapping or an adapter; V4 does not provide a ready-made ERP connector.

The accounting mappings reflect the prototype's stated chart and reporting choices. The framework does not claim universal statutory, tax or regulatory compliance. A balanced report establishes arithmetic consistency, not completeness of all business records or audit assurance.

## Roadmap

| Stage | Status / direction |
| --- | --- |
| Commercial, settlement, credit-note and reporting core | Implemented and tested locally |
| V4 packing lists, PDF integrity, inventory valuation/accounting and inventory BDE | Functional scope implemented; release review and independent feedback pending |
| V5 equity and corporate accounting | Next development module: incorporation, partner/shareholder accounts and contributions, with coordinated opening-balance treatment |
| Audit-console expansion | Deferred until after the equity work to avoid duplicating inventory/equity BDE status work |
| Payroll and employee accounting | Later module, with appropriate confidentiality boundaries |
| Public testnet / network evaluation | Later phase after module validation; no public-testnet deployment is claimed for V4 |
| External ERP/IMS adapters and supervised AI assistance | Future work; no direct integration or autonomous operation is claimed |

See the [detailed roadmap](roadmap/roadmap-2026-27.md) and [architecture overview](docs/architecture.md). The roadmap uses delivery status and sequencing rather than treating earlier calendar estimates as completed work.

## Repository scope

This [public repository](https://github.com/Blockchain-Integrated-Accounting/biaf-framework) contains research and conceptual documentation, roadmap and demonstration materials. The working implementation is maintained in a [separate private repository](https://github.com/N-0-name983/BIAF), which requires access authorization.

Installation instructions, dependency lists, local test configuration and implementation review notes belong to that private repository. Public source-code release and licensing decisions will be made explicitly; this README does not promise that the private implementation will be published on a particular date.

## Limitations and participation

BIAF remains experimental and unaudited for production use. Local tests do not establish readiness for mainnet operation, independent security assurance or jurisdiction-specific compliance. Equity/incorporation, full annual closing and profit distribution, payroll, fixed-asset operations, automatic valuation engines and complete ERP/IMS integration remain outside V4's implemented scope.

Research feedback and collaboration are welcome through this repository's [issues](https://github.com/Blockchain-Integrated-Accounting/biaf-framework/issues). Reports should distinguish observed behavior from proposed accounting or workflow changes.

Licensing arrangements remain under evaluation. Refer to any applicable repository/file-level license; public visibility alone does not establish an open-source license grant.

Developed by **Andreas Georgiou** as part of blockchain-integrated accounting research.
