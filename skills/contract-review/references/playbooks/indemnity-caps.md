# Indemnity caps

Use when a draft removes an indemnity from the liability cap, sets a separate indemnity cap, or adds a new indemnity (breach of agreement, data, confidentiality, law, AI output) whose cap treatment follows from existing exceptions.

## Read first
- Every indemnity in the agreement, by party: who is protected, from what claimant (third-party only, or the protected party's own losses), the causal trigger, covered losses and exclusions. See [indemnification](../issues/indemnification.md).
- How the cap clause refers to indemnities. An exception for "obligations under Section 12" or "indemnity obligations" captures every present and future indemnity placed there, not only the one the parties discussed.
- The damages exclusion. If it already excepts "indemnity obligations", any new indemnity is also free of the consequential and lost-profit exclusion: adding an indemnity flips two switches at once. See [liability](../issues/liability-and-remedies.md).
- Sole-remedy and supercap clauses (SLA credits, security supercap) that a broad indemnity could bypass; whether defense costs erode the cap; and the fee base for any separate cap.
- Insurance: limit, aggregate (per customer or shared across the book), retention and exclusions such as contractual liability or IP. See [insurance alignment](insurance-alignment.md).

## What drives the decision
Classify each indemnity before discussing the number. A third-party claim indemnity tied to a defined event (IP infringement by the service, a Security Incident caused by breach of the security section, bodily injury, violation of a specified law) prices a bounded, usually insurable risk; uncapping or supercapping it is a quantity question. An indemnity for "breach of this Agreement", "any act or omission", or "all losses arising out of or relating to" performance is a different instrument: it typically reaches first-party losses, converts every warranty and service failure into an indemnity claim, and, when indemnities are excepted from the cap and the damages exclusion, makes the whole contract uncapped and opens lost profits. That trigger, not the cap wording, usually drives the decision; it also overrides negotiated sole remedies and supercaps elsewhere.

When an uncapping exception is acceptable for one indemnity but drafted by section number or category, the fix is to name the specific indemnity, not to reject the exception. Check the paired customer indemnity: a mutual "indemnities are uncapped" exception also uncaps the customer's obligations, which the provider may want and the customer may not (see [customer indemnity](customer-indemnity.md)).

Facts that reverse the answer: the broad indemnity is limited to third-party claims from defined events with a separate cap (now a quantity question); the customer is on non-negotiable standard terms; the "uncapped" indemnity's risk is unbacked by insurance or upstream indemnity (for example, an AI-output IP claim the model vendor excludes); or the customer-side reviewer represents a buyer whose real exposure is a specific third-party risk the provider will cover in a defined form.

## Common positions (negotiating context, not policy)
Enterprise SaaS frequently leaves the provider's IP infringement indemnity uncapped or under a high supercap; other provider indemnities (data breach third-party claims, confidentiality, violation of law) are often under a supercap in the 2–5x fees range or a fixed amount. General breach-of-contract indemnities are commonly resisted by providers and are rare in negotiated SaaS paper. Customers often ask for defense costs outside the cap; providers often agree only for IP. Use these as context; do not present them as the user's standard.

## Company position (fill in)
- Standard: ___ (which indemnities are uncapped; which sit under which cap)
- Acceptable fallback: ___ (separate cap multiple, floor, fee base, required defined-event and third-party limits)
- Walk-away: ___
- Who approves: ___
Apply these as policy only when the user supplies them; otherwise label proposals as negotiating positions.

## Worked example
Packet: provider CSA, enterprise customer, $300,000 annual fees paid in advance. General cap is 12-month fees ($300,000) and applies to indemnities; damages exclusion excepts "indemnity obligations". Redline (1) excepts "Provider's obligations under Section 12" from the cap; (2) adds §12.3: Provider indemnifies and holds harmless Customer from all losses "arising out of or relating to Provider's breach of this Agreement". Policy: IP indemnity may be uncapped for enterprise; other indemnities must cover third-party claims from a defined event, under a separate cap up to 3.0x trailing fees with a floor up to $1,000,000 within insurance; no general breach indemnity.

Decision: §12.3 drives the decision. Through the "indemnity obligations" exception it escapes the damages exclusion, and through change (1) it escapes the cap: every breach, including SLA and warranty failures, becomes uncapped first-party liability including lost profits, beyond the $5,000,000 shared insurance aggregate. Reject §12.3. Accept change (1) on substance only as to §12.1 (IP); redraft to name §12.1. If the customer needs protection for a specific risk, offer a third-party claim indemnity for a defined event (for example, Security Incidents caused by Provider's breach of §4) under a separate cap of the greater of $1,000,000 or 3.0x trailing-12-month fees, which is $1,000,000 at $300,000 (3.0x is $900,000); state whether it stacks with the general cap and whether defense costs erode it. Customer note: IP protection is uncapped as requested; a general breach indemnity would displace the negotiated liability framework, so offer the defined protection instead. Reverses if §12.3 were already limited to third-party claims from a defined event, or if the customer were on standard terms (no legal redlines). Insisting on a general breach indemnity escalates to the business owner.
