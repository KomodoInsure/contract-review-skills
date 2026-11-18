# Damages-exclusion carveouts

Use when a draft adds exceptions to the indirect, consequential or lost-profit exclusion (data loss, cover or replacement costs, confidentiality, gross negligence, indemnity, specific breaches), or deems a category of loss "direct".

## Read first
- The exclusion's exact structure. "Neither party is liable for indirect or consequential damages or lost profits, except for X" usually lets X recover lost profits too; check whether the exception reaches every excluded head or only some.
- Whether each carveout uses a defined term ("Customer Protected Data" versus an undefined "Customer Data") and whether "neither party" makes a provider-facing exception mutual.
- Which cap then applies: carving a loss out of the exclusion does not uncap it, and an uncapped claim can still be excluded. Map each carveout to the general cap or a supercap. See [liability](../issues/liability-and-remedies.md).
- Sole-remedy clauses (SLA credits for unavailability) and termination rights that a cover-cost carveout may appear to bypass. See [SLA and credits](sla-and-credits.md).
- The service's role: system of record, backup provider, or a processing or import layer whose customer keeps source records. This determines what "loss of data" realistically costs and who can restore it.

## What drives the decision
Separate cost-of-repair carveouts from consequence carveouts. Reasonable costs of restoring or reloading data from backups or source records, and reasonable costs of procuring replacement services for a bounded period, are measurable, mitigation-type losses that courts often treat as direct anyway; carving them out mostly clarifies and keeps them under the applicable cap. A carveout for "damages arising from loss or corruption of data", "breach of confidentiality" or "gross negligence" is different: it reopens everything downstream of the event, including the customer's lost profits, its own customers' claims, penalties and business interruption. For a customer whose business runs on the data (payroll, billing, healthcare), those downstream losses are the largest and least predictable exposure, and the general cap may then be the only limit. That consequence carveout is usually the decision point; the cover-cost carveout is a drafting matter.

For cover costs, specify trigger (for example, termination for the provider's uncured material breach), period, reasonableness and whether recovery is the excess over fees the customer would have paid. State that it does not displace an agreed SLA sole remedy, or decide expressly that it does. Make the cap applying to each carveout explicit.

Facts that reverse the answer: the provider is contractually the system of record or backup service (a broader data-loss remedy, perhaps supercapped, becomes more defensible); the data-loss carveout is limited to restoration costs; the customer keeps no source records; or the agreement uncaps the carveout at the same time (now both switches move and the issue escalates). A customer-side reviewer should seek restoration and cover costs as direct damages first, since they are commonly obtainable, and reserve a broader data-loss carveout for services that hold the only copy.

## Common positions (negotiating context, not policy)
Negotiated SaaS often excepts confidentiality breach, indemnity, gross negligence or wilful misconduct, and payment obligations from the damages exclusion, frequently pairing them with a supercap. Data restoration costs and 6–12 months of cover costs are commonly treated as direct damages. A general data-loss carveout is less common and is usually limited to a supercap. These are market observations, not the user's policy.

## Company position (fill in)
- Standard: ___ (permitted carveouts and the cap each sits under)
- Acceptable fallback: ___ (restoration, cover-cost period and qualifiers)
- Walk-away: ___
- Who approves: ___
Apply these as policy only when the user supplies them; otherwise label proposals as negotiating positions.

## Worked example
Packet: provider data-import CSA; enterprise payroll bureau importing client employee files; $250,000 annual fees. General cap is 12-month fees; Increased Claims (security-section breach from gross negligence or wilful misconduct) are capped at 5.0x; the exclusion excepts only indemnity obligations; SLA credits are the sole remedy for unavailability. Redline adds exceptions for "damages arising from loss or corruption of Customer Data" and "Customer's costs of procuring replacement services"; caps unchanged. Policy: restoration from backups or source records and up to 12 months of replacement services may be carved out, subject to the applicable cap; no lost profits or general data-loss carveout.

Decision: the data-loss carveout drives the decision. As drafted it lifts the lost-profit exclusion for data loss, exposing Provider to the bureau's missed-payroll, client and penalty losses up to the cap; it also uses an undefined term. Reject it and counter with "reasonable costs of restoring or reloading Customer Protected Data from Provider's backups or Customer's source records". Accept replacement services with conditions: reasonable, up to 12 months, and not displacing §13 for unavailability. Both stay capped: $250,000 under §11(a) (12-month fees), or $1,250,000 (5.0x) if the loss is an Increased Claim from a grossly negligent or wilful §4 breach; say so expressly. Reverses if Provider were the customer's system of record or backup service, or if the customer narrowed the carveout to restoration costs (then accept within policy).
