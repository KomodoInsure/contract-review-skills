# Customer AI addenda and questionnaires

Scope: customer-drafted AI-use addenda, AI questionnaires and AI clauses. These cover disclosure of features and vendors, model-change notice, automated decisions about individuals, model and bias audits, contractual regulatory classification (such as EU AI Act roles), and disable switches.

## Read first
- Find out what each AI feature actually does. Establish its inputs, its outputs, who acts on them, whether a human reviews them, whether any decision concerns individuals, which models and vendors sit behind it, and whether it can be disabled per account. A questionnaire answer is a representation too, so answer from verified facts.
- Find the addendum's precedence over the main agreement, the DPA and the security terms, and look for overlap. Model-vendor notice and subprocessor notice should be one process, not two inconsistent ones.
- Separate the provider's own conduct from the customer's use of outputs. Many addenda make the provider answer for decisions the customer takes.
- Treat regulatory role and classification as legal questions that depend on the use case, the deployment, the market and current law. Do not answer them from the customer's label or from memory. Research current primary sources and route the question to counsel. See [sources](../sources.md).

## What drives the decision
- **Routine, when true:**
  - Listing AI features and model vendors.
  - Notice before adding or replacing a model vendor, matched to the subprocessor period.
  - A per-account disable switch.
  - A statement that the service does not make decisions with legal or similarly significant effects on individuals.

  Accept these with conditions that keep them accurate. Notice should cover vendor changes, not every model-version update from the same vendor. Disabling should be prospective, take effect only for features that support it, and carry no fee change unless agreed. The automated-decision restriction should cover the provider's use of AI, not the customer's downstream decisions. Where binding the roadmap is a concern, the fallback is to describe current functionality, give notice before any such feature is added, and keep it off by default.
- **Changes risk:**
  - **Customer-run model, bias or accuracy audits.** These touch shared systems and models the provider often does not own, and cannot be granted for an upstream vendor. Reject them, and offer documentation, evaluation summaries, assurance reports under NDA and the disable switch. The reasoning matches the customer-run audit example in [worked reviews](../examples/worked-reviews.md).
  - **Acknowledging a regulatory classification or role.** This imports regulatory duties by contract, whether or not the law applies, and works as an admission. Reject it. Offer compliance with AI laws applicable to the provider, each party's responsibility for its own obligations, and reasonable information the customer needs for its own compliance.
- **Facts that reverse the answer:**
  - A feature does decide or score individuals (hiring, credit, eligibility, pricing to consumers). The automated-decision clause is then untrue, and classification needs counsel's real analysis.
  - Counsel concludes that a law requires specific provider duties or audit access. Escalate instead of rejecting.
  - Single-tenant or customer-owned model deployments make testing feasible.

## Common positions (negotiating context, not policy)
- Providers commonly disclose AI features and model vendors, give notice of vendor changes on subprocessor timelines, and offer opt-outs.
- Third-party bias or accuracy audits are usually answered with documentation, model or system cards, evaluation results and certifications, not with access.
- Regulatory-role clauses are usually reframed as mutual compliance with applicable law plus cooperation.

## Company position (fill in)
- Standard: ___ (disclosure, notice period, disable switch, assurance materials offered)
- Acceptable fallback: ___ (for example, a roadmap notice for decision-making features, or extra evaluation reporting)
- Walk-away: ___ (for example, customer model testing, or contractual regulatory classification)
- Who approves: ___ (including whether product and counsel must sign off on AI statements)
Apply these as policy only when the user supplies them.

## Worked example
Packet: an EU-headquartered freight forwarder (US entity signing) sends a five-item addendum for an AI column-mapping feature that makes no decisions about individuals, uses a third-party model vendor, and can be disabled per account. Policy: disclose features and vendors with 30 days' notice of model-vendor changes; no customer audits or testing of models; offer documentation, evaluation summaries and SOC 2 under NDA; comply with AI laws applicable to Provider; no contractual classification.

Decision:
1. **Disclosure and 30-day notice of model-vendor changes: accept**, defining a change as adding or replacing a vendor and aligning it with the DPA.
2. **No significant-effect decisions about individuals: accept with conditions.** Limit it to Provider's use of AI, and confirm the product facts. The playbook is silent here, so route it for approval.
3. **Annual bias and accuracy audits: reject.** Offer the policy's materials instead.
4. **Acknowledging high-risk status and the obligations of a high-risk AI provider: reject.** This is what drives the decision. Replace it with mutual compliance with applicable law and reasonable information-sharing. Any view on whether or how the EU AI Act applies to a US provider here needs counsel and current research; do not state it as settled.
5. **Disable switch: accept.** Note that disabling is prospective, and that data already sent stays with the vendor for its disclosed retention period.

The answer reverses if the feature begins to make or materially inform decisions about individuals.

Related: [AI model subprocessors](ai-model-subprocessors.md), [AI training and data use](ai-training-and-data-use.md), [warranties and AI accuracy](warranties-and-ai-accuracy.md), [AI output indemnity](ai-output-indemnity.md), [data, confidentiality and AI](../issues/data-confidentiality-and-ai.md).
