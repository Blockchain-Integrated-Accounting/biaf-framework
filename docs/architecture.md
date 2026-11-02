# BIAF Architecture — V4

Status: local research prototype, 2 November 2026. This overview describes the implemented USDC V4 responsibilities and separates them from future modules. It does not assert production readiness or universal accounting compliance.

## Layers and responsibilities

| Layer | Current responsibility |
| --- | --- |
| On-chain execution | Commercial document identities/state, authorization, acceptance, USDC settlement, credit-note relationships, events, attachment hash commitments and optional aggregate inventory declarations |
| Accounting interpretation | Supported event-to-journal mappings, buyer classifications, VAT treatment, linked-credit accounting and explicit local inventory adjustments |
| Local persistence | Wallet/chain/ledger-scoped catalogue, drafts, valuation versions, PDF files and accounting records in browser storage |
| Reporting and reconciliation | Journal/counterparty views, trial balance, VAT, periodic COGS/P&L, posted-journal balance sheet and audit/reconciliation checks |
| Human interaction | Preparation, review, wallet signing, local valuation approval, classification decisions, explicit postings, BDE and backup/export |

Historical ETH-denominated prototypes informed the project. The maintained V4 implementation described here uses USDC-denominated commercial values and settlement on EVM execution infrastructure. Historical variants should not be assumed to have identical current feature coverage.

## Commercial lifecycle

A seller issues an invoice or receipt identifying the counterparty, amounts and description. Buyer acceptance and payment follow the rules of the document type. Receipts and invoices do not have identical acceptance/payment semantics.

Credit notes are subsequent linked events. Separate routes and credit purposes control acknowledgment, correction allocation, commercial credit and eligible refunds. A credit does not edit the earlier transaction history. The accounting layer applies the corresponding treatment based on the document's state and accepted/recorded transactions; mere issuance is not a universal instruction to recognize every document as a completed sale.

Wallet signatures identify the authorizing wallet. The local registry associates wallets with business details and analytical accounts; this is not an independent identity-verification service.

## Supporting PDF lifecycle

The seller maintains a local catalogue and editable supporting drafts. PDF preparation captures commercial lines, business-detail snapshots and the issuance context in a frozen file. The file receives a printed attachment reference; its exact bytes produce the hash committed at issuance.

A counterparty obtains the original file through an agreed channel and imports it against the loaded document. Verification checks the hash and corresponding context. Identical totals alone do not establish a match. A stored, verified reference helps identify the same file later.

The assigned BIAF document number is established during issuance. The committed PDF is not subsequently rewritten to add the number, acceptance or settlement status. Those facts are shown in the application. Manually written supporting references are aids to navigation and remain subject to verification.

Draft/PDF deletion before issuance requires a successful live check of the relevant attachment bindings. Issued files stay unchanged. The seller's restore input recovers a local copy for an already loaded document; it is not a reverse-document search.

This design proves the integrity/association of supplied bytes, not the physical delivery, legal validity or valuation accuracy of the underlying transaction.

## Inventory valuation, accounting and BDE

V4 records accountant-supplied opening/adoption and closing values by supported inventory category and reporting period. Method, basis and evidence metadata accompany local approval. Replacement preserves earlier approved versions; carry-forward references an approved preceding close. An external JSON valuation is loaded for review rather than automatically approved or posted.

Three operations remain distinct:

1. **Local approval** preserves the valuation version.
2. **Journal posting** explicitly records reviewed opening/closing adjustments.
3. **BDE** optionally registers the approved aggregate value and identifiers on-chain.

Item/category details and evidence do not become public merely because an aggregate is registered. A declaration's registration time is distinct from the reporting-period effective date and the local approval timestamp.

An approved valuation may supply periodic COGS before a related journal adjustment is posted. The balance sheet follows cumulative posted journals. Reconciliation information exposes this distinction. V4's inventory postings do not constitute complete incorporation, full opening-balance migration or formal annual closing and distribution.

## Data boundary

| Information | On-chain in V4 | Local / off-chain in V4 |
| --- | --- | --- |
| Commercial identity, parties' wallets, amounts, descriptions, state and events | Yes | Read and interpreted by the UI |
| Supporting PDF commitment | Exact file hash and document binding | Original file, embedded record and business details |
| Item descriptions, units, quantities and unit prices | Not as full packing-list data | Catalogue, draft and PDF |
| Journal construction and analytical classification | No | Yes |
| Valuation approval and category/evidence detail | No | Yes |
| Optional inventory BDE | Aggregate declaration, period/type/entity and version relationship | Approval record and detailed support |
| Financial statement preparation | No complete statement-publication workflow | Current local reports |
| Equity/payroll/fixed-asset module events and their BDE | Planned scope | Not implemented as full V4 modules |

Descriptions entered on-chain are visible within that chain's access model. Off-chain document design does not make on-chain descriptions confidential. The user decides what description to submit.

## Storage, backup and scope

Local storage is separated by relevant chain, ledger and wallet identifiers, within the browser origin. The same hostname/port and browser profile matter for recovery. Journal JSON, inventory JSON and original PDFs preserve different parts of the application; none is a complete substitute for the others or for blockchain history.

A restarted ephemeral development chain can reuse deterministic addresses while losing all earlier events. Local files surviving that restart do not prove issuance on the new history. Restore/import must not silently treat stale test events as current facts.

## Reporting, interoperability and limitations

Reporting uses the prototype's explicit accounting mappings and input completeness. Arithmetic balance does not certify completeness, compliance or independent assurance. VAT and tax-deductibility choices require accountable human interpretation.

CSV/JSON exports support review, backup and processing. Direct use in an ERP requires a mapped adapter or compatible importer and its own validation. V4 is not a perpetual IMS, automatic valuation engine or ready-made ERP connector.

Future work includes equity, coordinated audit status expansion, payroll, fixed assets, broader optional BDE publication, network/testnet evaluation and supervised assistance. See the [roadmap](../roadmap/roadmap-2025-26.md).
