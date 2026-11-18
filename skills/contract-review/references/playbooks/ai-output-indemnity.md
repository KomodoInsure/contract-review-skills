# AI output indemnity

Use when a customer asks the provider to defend or indemnify claims that AI-generated output, or the customer's use of it, infringes third-party rights; the same analysis applies in reverse for a customer reviewing a vendor's offer.

## Read first

- The existing IP indemnity: does "the Service" already reach outputs, and which rights, territory and exclusions (customer data, combinations, modifications) apply? A new output clause that sits beside it without matching exclusions widens both. See [indemnification](../issues/indemnification.md).
- What the feature produces and how it is used: short suggestions a user accepts, code, text, images or published content. Output that is functional, short or kept internal carries different claim risk from creative or redistributed output.
- The upstream model terms, in their actual text: who is protected (the provider only, or also the provider's customers), which rights (copyright only, or patent, trademark and trade secret too), conditions (unmodified output, safety filters or guardrails on, no knowing infringement, paid tier), exclusions (inputs, fine-tunes, combinations), the cap and the procedure (notice, control of defense). Also check whether the vendor may change those terms on notice. Read [AI model subprocessors](ai-model-subprocessors.md) for the vendor relationship.
- Liability treatment: whether indemnity is inside the general cap, a super-cap or uncapped, and whether the damages exclusion carves indemnity out. See [indemnity caps](indemnity-caps.md) and [damages-exclusion carveouts](damages-exclusion-carveouts.md).
- Who can approve a non-standard indemnity, and the customer's tier.

## What drives the decision

The question is whether the provider is promising protection it has backed upstream or controls itself. A provider that wraps a third-party model passes output risk through; its own indemnity is only as safe as the upstream promise. So the drivers are the gaps between what the customer asks for and what the provider receives:

- **Rights.** Copyright-only coverage is the usual upstream offer. "Any intellectual property right" adds patents and trade secrets, which nobody can screen output for. This is usually the largest gap.
- **Covered output.** "Any output" reaches output that a user edited, combined or derived from the customer's own inputs. An upstream promise limited to unmodified output, excluding claims caused by inputs, leaves those uncovered. "Customer's use of output" reaches any downstream use, including redistribution and combination with other products.
- **Who is protected.** If the upstream indemnity covers only claims brought against the provider, a claim brought against the customer, which the provider pays under its own indemnity, may fall outside it. Confirm before calling the flow-down matched.
- **Conditions the provider controls.** Filters or guardrails that must be on are an operational commitment: confirm they are always enabled for the feature. Do not push an upstream condition onto the customer if the customer cannot control it.
- **Cap.** Within the general cap the residual is bounded; an uncapped or super-capped output indemnity changes exposure much more than its wording suggests, because the damages exclusion often carves out indemnity.

Routine: a conditional indemnity that mirrors the upstream rights, conditions and exclusions, sits under the existing cap and uses the existing procedure. Risk-changing: broader rights, any output, use-based triggers, uncapped treatment, or a promise that survives loss of the upstream protection. Facts that reverse a refusal: upstream coverage that really is broad (all IP, claims against downstream customers); output the provider generates with its own models trained on licensed data; a customer that keeps output internal. Facts that harden it: generated code or content the customer ships to its own customers, a capped or narrow upstream promise, or an upstream that can withdraw coverage unilaterally. Whether AI output is protectable or infringing is unsettled and fact-specific; do not assure either side that the risk is remote. Research current law when the conclusion depends on it.

For a customer-side reviewer, the same map identifies what to ask for: the provider's actual upstream coverage, removal of conditions the customer cannot satisfy, and inclusion of output in the existing IP indemnity rather than a narrower side clause.

## Common positions (negotiating context, not policy)

Large model developers often offer output indemnities on paid or enterprise tiers, typically conditioned on safety features being enabled, no modification, no knowing infringement and exclusion of claims caused by inputs. Application vendors built on those models range from no output indemnity, through a matched flow-down, to coverage within the general IP indemnity. A broad, unconditional all-IP output indemnity from an application vendor is uncommon. "Every AI vendor covers outputs" describes a range, not a standard term.

## Company position (fill in)

Apply only when the user supplies it. Standard: ___ (for example, no output indemnity). Acceptable fallback: ___ (for example, a mirror of upstream rights, conditions and exclusions, under the general cap). Walk-away: ___. Who approves: ___.

## Worked example

Packet: an enterprise customer ($350,000 a year) adds "Provider will defend and indemnify Customer against any third-party claim alleging that any output of [the AI feature], or Customer's use of such output, infringes or misappropriates any intellectual property right." The model vendor indemnifies the provider only for copyright claims against unmodified output generated with filters on, excluding input-caused claims. The general cap applies to indemnity; the damages exclusion carves out indemnity. Policy: no output indemnity as standard; the business owner may approve a conditional one no broader than the upstream protection; the agreement owner may propose it subject to that approval.

Decision: counter; do not accept as sent. The driver is the gap between "any IP right... any output... or use" and the upstream copyright-only, unmodified-output protection: patent and trade-secret claims, edited or combined output, and input-caused claims would be the provider's own uninsured risk. Propose, subject to business-owner approval: defense and payment of third-party claims that output, as generated by the feature and not modified by anyone other than the provider, infringes a third party's copyright; excluding claims arising from Customer Protected Data or other customer inputs, combinations not supplied by the provider and use after the provider requests that the output stop being used; governed by the existing IP indemnity procedure and subject to the general cap. Before proposing, confirm that filters are always on and that the upstream promise covers claims against the provider's customers. If it does not, the matched counter still leaves a gap the business owner must accept knowingly. Anything broader goes beyond policy: escalate to the business owner, then outside counsel. Reverse: an upstream indemnity covering all IP and downstream customers would support broader rights. A standard-tier customer gets no redline.
