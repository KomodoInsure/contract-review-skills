# Services liability

Use when a draft treats professional services (implementation, migration, configuration, training, on-site work) differently from the subscription for liability: carving services out of the cap or damages exclusion, adding a services cap or remedy, or adding indemnities for personnel conduct on customer premises.

## Read first
- The SOW: deliverables, fixed fee or time-and-materials, on-site versus remote, customer dependencies, acceptance, and whether the work touches customer data or production systems (migrations, integrations, data cleansing). See [services](../contract-types/services.md).
- Whether the cap's fee base includes services fees and over what window; compute the general cap with and without them. Check whether "this Section" carve-outs remove only the monetary cap or also the damages exclusion ([damages exclusion carveouts](damages-exclusion-carveouts.md)).
- How services claims overlap existing tiers: a migration error that exposes or corrupts data can also be a security-section or confidentiality claim with its own tier ([liability triggers](liability-triggers.md), [data-breach costs](data-breach-costs.md)).
- Existing services remedies (re-performance, refund, warranty period) and any exclusive-remedy wording.
- Insurance by line: bodily injury and property damage on premises usually sit with general liability; errors in professional work with E&O, often on a shared aggregate. See [insurance alignment](insurance-alignment.md).

## What drives the decision
Separate personnel-conduct risk from professional-performance risk. Bodily injury, death or tangible property damage caused by staff on site is a discrete, fault-based, typically CGL-insured risk; an indemnity for it outside the cap is often routine if limited to the represented party's negligence or misconduct, proportionate to fault, and subject to normal indemnity procedure. Professional-performance risk is different: a carveout such as "the limitations do not apply to Professional Services" removes the cap and, if the whole section is disapplied, the consequential and lost-profit exclusion for anything connected with the work. For migration or configuration work, that reaches downstream business interruption and data loss, can bypass the agreed data tier, and is unbounded relative to a fixed fee.

Routine: re-performance or refund of fees for nonconforming services; services claims inside the general cap; a separate services cap expressed as a multiple of SOW fees if approved; on-site injury and property indemnity limited by fault. Risk-changing: any uncapped or exclusion-free services carveout; services warranties that promise outcomes ("migration will be error-free") rather than conformance to the SOW; vague scope ("arising from or relating to Professional Services") that can sweep in subscription claims. The customer's legitimate concern is usually that a fixed-fee remedy is worthless if the migration corrupts records; answer it with performance mechanics (source-data backup retained by customer, reconciliation and validation steps, acceptance testing before cutover) rather than unlimited liability.

Reverses when: the services are low-risk (training, advisory) and the cap base includes services fees; the business owner approves a defined services supercap; the injury indemnity is drafted beyond fault ("arising from presence on premises") or to cover the customer's own negligence, which turns a priced risk into an unbounded one. From the customer side, the same split shows where to push: fault-based injury indemnity uncapped, and a meaningful services remedy plus data-migration controls rather than a blanket carveout.

## Common positions
Negotiating context only, not the user's policy. Providers commonly keep services within the general cap and offer re-performance or refund; customers commonly seek uncapped bodily injury and property damage indemnities, which many providers grant when fault-based; separate services caps tied to SOW fees appear in larger implementations. Do not present these as approved positions.

## Company position (fill in)
- Standard: [services within the cap; remedy for nonconforming services]
- Acceptable fallback: [services cap basis; on-site injury/property indemnity terms]
- Walk-away: [uncapped or exclusion-free services carveouts; outcome warranties]
- Who approves: [role for any services supercap]

Apply these as policy only when the user supplies them; otherwise label any proposal a negotiating position.

## Worked example
Packet: new enterprise customer; subscription $300,000/year; fixed-fee $80,000 SOW including migration of legacy vendor records, two weeks on site. General cap: fees paid or payable in the prior 12 months, up to $380,000 if both subscription and SOW fees fall in the window (confirm the fees definition). Customer adds "The limitations in this Section 11 do not apply to Provider's performance of Professional Services" and a §12.4 indemnity for bodily injury, death or tangible property damage caused by Provider personnel's negligence or willful misconduct on Customer premises. Policy: services stay within §11; re-performance or refund of nonconforming services may be offered; the on-site injury/property indemnity may sit outside the cap as a CGL-insured risk ($1,000,000 per occurrence/$2,000,000 aggregate carried).

Decision: reject the §11 carveout; it is the driver. It removes the cap and the §11(c) consequential and lost-profit exclusion for all services work, so a migration error could expose Provider to uncapped downstream losses on an $80,000 fee, and data claims arising in the work would escape the 5.0x Increased Claims tier entirely. Counter: services remain within §11; Provider will re-perform nonconforming services or refund the fees paid for them (up to $80,000), and the SOW will include customer backup of source records and reconciliation before cutover. Accept §12.4 on substance with conditions: "to the extent caused by", standard notice/control/cooperation procedure, and expressly carved out of §11(a) (as drafted, §11(a) would still cap it, which the customer may not intend). Whether CGL responds to a given claim depends on policy wording. Escalate to the business owner only if the customer insists on a services cap above §11. Reverses if the business owner approves a defined services supercap or the indemnity is widened beyond Provider fault.
