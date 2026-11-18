# Data breach costs

Use when a draft defines breach-response or "Data Breach Costs", deems them direct damages, excepts them from the damages exclusion, or moves them under a security supercap or floor.

## Read first
- The trigger: which event (defined Security Incident, any unauthorized access, any breach of the security section) and which causal link to the provider's conduct ("caused by Provider's breach of Section 4", "arising from", "relating to"). See [liability triggers](liability-triggers.md) and [security commitments](security-commitments.md).
- The supercap: multiple, fee base and window, floor wording ("greater of"), and whether it replaces or adds to the general cap, applies per claim or in aggregate, and is shared with other increased categories. Compute it with the deal's fees.
- The damages exclusion and how the new definition interacts with it: listing costs as "direct" and "not excluded" are separate switches; check each listed head individually. See [liability](../issues/liability-and-remedies.md).
- The data actually processed (consumer, payment, health, government identifiers), which determines which response costs are customary or legally required, and the notice clause ([incident notice](incident-notice.md)).
- Insurance: cyber limit, whether it is a shared annual aggregate across customers, retention, and whether fines, penalties and notification costs are covered. See [insurance alignment](insurance-alignment.md).

## What drives the decision
Breach-response costs (legally required notices, credit or identity monitoring where customary, forensic investigation, call-centre support) are the predictable, documentable consequences of an incident; treating them as direct damages under a supercap is a routine clarification that mostly removes a dispute over labels, provided they are reasonable, documented and causally tied to the provider's breach. The risk allocation changes when the list reaches open-ended heads: the customer's lost profits or revenue, reputational harm, "all costs" or "including but not limited to", or third-party claims against the customer not routed through an indemnity procedure. Those reintroduce exactly what the damages exclusion removed, and even under a supercap they consume the limit meant for response costs. Fines and penalties sit in between: accept only to the extent imposed because of the provider's breach and where law permits recovery or insurance; some regimes or policies prohibit indemnifying penalties.

Read the trigger before the list. "Caused by Provider's breach of [security section]" is measurable; "any Security Incident" or "relating to Customer Data" makes the provider pay response costs for incidents it did not cause (customer credential compromise, customer-side misconfiguration). For a multi-tenant provider, check the cap against the insurance aggregate at portfolio level: one incident can trigger many customers' supercaps at once.

Facts that reverse the answer: the definition already excludes lost profits and limits fines (accept); the trigger is not causation-limited (counter even if every head is acceptable); the cap is uncapped rather than supercapped; the data class makes credit monitoring non-customary or requires other remedies (identity restoration, regulator-mandated programmes). For a customer-side reviewer, the same analysis shows which heads are worth fighting for: response costs and qualified fines are commonly obtainable; lost profits rarely are.

## Common positions (negotiating context, not policy)
Negotiated SaaS commonly places security or data-breach claims under a supercap of roughly 2–10x annual fees or a fixed amount, sometimes with a floor, and lists notification, monitoring (often 12–24 months), forensics and call-centre costs as direct damages. Fines are frequently accepted with legal-recoverability and causation qualifiers. Lost profits usually remain excluded. These are market observations, not the user's policy.

## Company position (fill in)
- Standard: ___ (supercap multiple, floor, which breaches qualify)
- Acceptable fallback: ___ (listed response costs and qualifiers; fines treatment)
- Walk-away: ___ (excluded heads; uncapped treatment)
- Who approves: ___
Apply these as policy only when the user supplies them; otherwise label proposals as negotiating positions.

## Worked example
Packet: provider CSA; enterprise retailer importing consumer order data; $200,000 annual fees. Increased Claims cap is 5.0x 12-month fees, in lieu of the general cap; currently limited to security-section breaches from gross negligence or wilful misconduct. Redline changes the cap to "the greater of $1,000,000 or 5.0x" and adds Data Breach Costs (notices, credit monitoring, forensics, call centre, fines and penalties, Customer's lost profits and revenue) for Security Incidents caused by Provider's breach of §4, as direct, not excluded and Increased Claims. Policy: up to 10.0x with a floor up to $1,000,000 within insurance; any §4 breach may be an Increased Claim; reasonable documented response costs (credit monitoring up to 12 months where customary) may be direct; fines only where caused by Provider's breach and legally recoverable; lost profits stay excluded.

Decision: item (vi), lost profits and revenue, drives the decision; strike it and keep §11(c) applying to it. Accept the floor: 5.0x of $200,000 is $1,000,000, so the cap is $1,000,000 today and the floor only matters if trailing fees fall below $200,000 (early term or reduced fees). Accept extending Increased Claims to Provider's breach of §4 as the causal trigger. Accept (i)–(iv) with "reasonable, documented" and "legally required" for notices, and credit monitoring "for up to 12 months where customary for the affected data" (consumer order data may not make it customary). Accept (v) only "to the extent imposed because of Provider's breach and recoverable under applicable law". The $1,000,000 cap is within the $5,000,000 cyber limit, but that limit is a shared annual aggregate with a $100,000 retention, and whether it covers fines is unverified. Reverses if the customer refuses to drop lost profits (outside policy: escalate) or if the trigger were "any Security Incident" rather than Provider's breach.
