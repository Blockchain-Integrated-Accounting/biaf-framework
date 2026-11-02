# BIAF Roadmap — Status at 2 November 2026

This roadmap supersedes the earlier quarter-by-quarter estimates. A past target date is not evidence of delivery. Status below distinguishes implemented local functionality from release review, independent assurance and future modules.

## Current position

The USDC prototype has a commercial/accounting core and a V4 packing-list/inventory extension. It runs on a local Hardhat chain. V4 functional implementation and developer/manual checks are complete for the agreed scope; documentation, repository review, commit and independent feedback are release steps still in progress.

| Workstream | Status |
| --- | --- |
| Invoice/receipt issuance, wallet interaction, acceptance and settlement | Implemented and exercised locally |
| Credit-note routes, allocation/refund and associated accounting/audit | Implemented and exercised locally |
| Journals, customer/supplier views, trial balance, VAT, P&L and balance sheet | Implemented within the prototype's accounting scope |
| Packing-list/service-detail drafts, PDF preparation and registry snapshots | Implemented |
| Issuance hash commitments and exact-file verification | Implemented; original issued PDFs stay unchanged |
| Discarding unissued draft/PDF pairs after live issuance checks | Implemented |
| Inventory valuation versions, carry-forward and external valuation JSON | Implemented |
| Reviewed opening/closing inventory adjustments, group-2 splits and linked-credit reclassification | Implemented |
| Optional inventory BDE | Implemented for aggregate declarations; details/evidence remain local |
| Scoped local backup/restoration and relevant search/filter/page controls | Implemented |
| V4 landing-page and header branding/copy | Implemented and checked |
| Final release documentation and private V4 commit | In progress |
| Independent V4 testing/feedback | Pending |
| Production security review / public-testnet validation | Not completed by local functional testing |

## V4 release boundary

V4 is not a complete ERP or perpetual IMS. Packing-list quantities do not automatically update stock balances. External valuation JSON is a reviewed input format, not a ready-made connection to an inventory vendor. CSV/JSON exports do not establish direct ERP compatibility.

Valuation approval, BDE and journal posting remain separate. The current inventory journal adjustments are not a full statutory fiscal closing, incorporation module or migration of every opening balance. Local reporting is not equivalent to publication of full financial statements on-chain.

Release work consists of documentation, an accurate completed/deferred checklist, final source/commit review, a reproducible version reference and independent feedback. New features should not be introduced merely to extend the release checklist; defects found during review remain actionable.

## Next module — V5 equity and corporate accounting

Planned scope includes incorporation, shareholder/partner identities and analytical accounts, capital subscriptions/contributions, related assets/cash, distributions and equity transactions. Inventory contributed at incorporation or introduced at first adoption must be coordinated with the equity workflow to avoid double-counting the same asset.

Chart-of-accounts management, postable account validation and entity-managed analytical depth should be designed together with this module. Existing customer/supplier analytical identifiers should not be renumbered merely to fill gaps.

Formal annual closing through result accounts and transfer/distribution of profit or loss needs an explicit design rather than being inferred from V4's periodic COGS adjustment.

## After equity — audit-console expansion

Extend the audit console to distinguish local approval, journal posting, optional on-chain declaration and their agreement for inventory/equity. This work was deferred until after equity so its status model is designed once. Existing audit checks and the general negative-COGS warning remain available in V4; a comprehensive new BDE status console is not claimed.

## Later accounting modules

- Payroll, employee liabilities, deductions, employer obligations and settlement, with confidentiality boundaries.
- Fixed-asset acquisition, depreciation/disposal and related accounting.
- Additional reporting and tax reconciliation appropriate to a declared jurisdiction/basis.
- Optional BDE publication of equity, balance sheet, P&L and fixed-asset values.

The black-and-gold monk will continue to distinguish optional BDE actions from off-chain export. Future publication is a declaration workflow; independent assurance is a separate question.

## Public testnet and infrastructure evaluation

After the principal module work and validation, evaluate suitable public testnets and deployment options. Criteria include execution cost, EVM compatibility, stablecoin infrastructure, wallet support, privacy boundaries, operational reliability and realistic transaction volumes. No completed public-testnet, L2 integration or production deployment is implied by this roadmap.

## External integration and supervised AI

Explore ERP/IMS adapters, explicit mapping contracts and interoperability tests. Automatic valuation or warehouse operations require their own scope and validation.

AI assistance may later support document preparation, classification suggestions, reconciliation and review. Supervision, identity/authority boundaries and transaction limits must be specified before operational automation is claimed. V4 does not depend on autonomous agents.

## Disclosure and evaluation

The public repository documents the research and provides demonstration material. The working implementation and setup guidance remain in the private repository. Any source-code release or license change requires an explicit project decision.

Functional tests, independent user testing, accounting review and security assurance are different kinds of evidence. Preserve that distinction when reporting progress or planning a release. Future dates will be assigned when scope and dependencies justify them.
