# SLA and service credits

Use when a draft changes an availability target, measurement, exclusions, service credits, whether credits are the exclusive remedy, or termination for poor availability.

## Read first
- The target and its measurement period (monthly, quarterly), how availability is measured (whole service or component, synthetic or customer-reported), and exclusions (scheduled maintenance, customer-caused, third-party, force majeure). A target means nothing without them.
- Convert each target into allowed downtime: a 30-day month is 43,200 minutes, a 31-day month 44,640. 99.9% allows about 43 minutes a month; 99.95% about 22; 99.99% about 4.3; 99.5% about 3.6 hours. Annual figures (525,600 minutes) are useful for history but most SLAs are judged monthly.
- Actual history: monthly availability for at least the trailing 12 months, not only the average. An annual average can hide several failing months; ask operations for the monthly series before predicting how often credits or a chronic-failure trigger would fire.
- The remedy chain: credit schedule and cap, claim procedure, exclusive-remedy wording, termination rights and refunds, and how a non-exclusive unavailability claim would sit under the general cap and the consequential-damages exclusion. See [liability and remedies](../issues/liability-and-remedies.md) and [SaaS](../contract-types/saas.md).
- Ownership: SLAs are often commercial terms owned by sales, but exclusive-remedy, termination and refund language changes liability and exit and needs the legal owner's review.

## What drives the decision
Routine: credit tiers, credit amounts within the approved cap, reporting, claim windows, and a chronic-failure termination right with a refund of prepaid unused fees, where approved. With credits as the sole remedy, a higher target is mainly a pricing question: the cost of a miss is bounded by the credit cap. Compute that maximum (credit cap x monthly fee x 12) and let the commercial owner decide whether to price it.

Risk-changing: (1) deleting the exclusive-remedy clause or making credits "in addition to" other remedies. Every outage becomes a potential damages claim (lost bookings, cover costs, its own customers' claims), limited only by the general cap and whatever the damages exclusion catches. (2) A target the service does not meet on its record: combined with (1), it turns a near-certain monthly miss into a continuing breach. (3) A single-event termination trigger, which converts one bad incident into an exit right; weigh its threshold against history, and preserve the refund-only consequence. (4) Measurement changes that move the real target (component-level or customer-observed measurement, removal of maintenance exclusions).

Identify which change carries the risk. When a redline raises the target and removes exclusivity together, the pairing drives the decision. A target the service does not meet is cheap while credits are the sole remedy (it costs at most the credit cap), but once credits stop being exclusive it becomes a recurring breach. Name both and lead with the combination. Taken alone, the remedy change usually carries more risk than the number. Check history before treating a target as achievable: an average that already falls short of the proposed target means it would have been missed.

Facts that reverse the answer: monthly history comfortably above the proposed target and architecture to sustain it (a higher target becomes a priced concession); a premium or dedicated tier with its own SLA; a customer whose operations depend on uptime and pays for it; a termination threshold so far below actual performance that it is unlikely to trigger. For a customer-side review, the same arithmetic argues for a realistic target, credits that matter relative to fees, and a chronic-failure exit rather than an unattainable number.

## Common positions
Negotiating context only, not the user's policy. Multi-tenant B2B SaaS commonly offers 99.5% to 99.9% monthly availability, with 99.95% for premium tiers and 99.99% rare outside architectures built for it. Credits commonly range from about 5% to 25% or 30% of the monthly fee, often tiered, and are commonly the sole remedy for unavailability, paired with a chronic-failure termination right and refund of prepaid unused fees.

## Company position (fill in)
- Standard: [target, measurement, exclusions, credit schedule and cap, exclusive remedy]
- Acceptable fallback: [e.g., chronic-failure termination definition and refund]
- Walk-away: [e.g., non-exclusive credits; targets above demonstrated history]
- Who approves: [commercial owner for targets and credits; legal owner for remedy and termination language]

## Worked example
Packet: new enterprise customer, a US travel booking platform, $280,000 annual fees ($23,333 monthly). §13 is 99.9% monthly availability with credits up to 25% of the monthly fee as sole remedy. Trailing-12-month availability is 99.95%; worst month 99.86%. The redline raises the target to 99.99%, makes credits "in addition to any other remedies", and adds termination if availability falls below 99.5% in any month. Sales guidance: keep 99.9% and sole remedy; fallback chronic-failure termination (below 99.9% in three consecutive months or any four in twelve) with refund of prepaid unused fees; anything else needs business-owner approval.

Downtime: 99.9% allows 43.2 minutes in a 30-day month (44.6 in 31 days); 99.99% allows 4.3 (4.5); 99.5% allows 216 minutes (3.6 hours). History: 99.95% over 12 months is about 263 minutes of downtime, roughly 22 minutes a month on average; the worst month (99.86%) was about 60 minutes. The average month would have missed 99.99% about five times over; the worst month missed even 99.9%.

Decision: the 99.99% target together with the sole-remedy deletion drives the decision; reject both. With credits as sole remedy the 99.99% target costs at most $5,833 a month ($70,000 a year); without it, a target the service has not met becomes a breach in most months, exposed to damages up to the $280,000 general cap, subject to §11(c). Reject 99.99% on the history and offer 99.9% (any higher figure is the business owner's commercial call, priced against the credit maximum). Counter the 99.5% any-month termination with the guidance fallback: chronic-failure termination with refund of prepaid unused fees, credits remaining the sole monetary remedy. The single-month 99.5% trigger sits about 156 minutes above the worst recorded month, so if the customer prefers it, it is a reasonable alternative to take to the business owner, in place of (not in addition to) the fallback and with a refund-only consequence. Get the monthly series before offering the fallback: the average does not show whether three or four months fell below 99.9%. Reversal: sustained history at or above 99.99% with supporting architecture (target becomes a priced concession), or a dedicated deployment with its own SLA.
