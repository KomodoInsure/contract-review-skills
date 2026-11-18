# AI model subprocessors

Scope: customer DPA or contract terms that reach third-party model or LLM providers acting as subprocessors, covering notice, objection and veto rights, retention and zero-retention, training, and processing region.

## Read first
- Identify each model vendor and what reaches it. That means which features send data, which data classes and how much (full records, or samples and minimized fields), the region and endpoint, and whether the customer can turn the feature off.
- Read the upstream terms actually in force for the provider's account, not the vendor's marketing page. Check training use, retention for abuse monitoring or logging, whether zero or reduced retention has been granted (it is often an approved exception, not a default), human review, region, onward subprocessors, breach notice, and the vendor's own right to change terms.
- A commitment the provider makes about subprocessors is true only when the provider's contract with each relevant subprocessor imposes it. "No subprocessor will…" covers hosting, storage, support and email vendors too, not just the model vendor.
- Read the customer's sector. Lending, insurance, health and public-sector customers often bring vendor-management requirements. Research whether applicable law actually requires a term, or whether it is an internal policy preference.

## What drives the decision
- **A promise upstream terms cannot support is the first problem.** If the vendor retains inputs for up to N days, a zero-retention promise puts the provider in breach at signing. Reject it or restate it accurately: the actual retention, its purpose, the continued protection, deletion afterwards, and no other use. Offer to pursue zero retention or minimize the data sent, and commit to zero retention only once it is obtained and verified for that vendor.
- **Notice length is mainly operational.** A long notice period freezes vendor changes for every customer, because the shared service moves at the pace of the longest notice. That matters most when a vendor deprecates a model or a security issue forces a quick switch. Counter to the standard period. An emergency-replacement exception is worth requesting.
- **An objection that operates as a veto breaks the multi-tenant model.** One customer cannot stop the provider using a vendor for everyone. Offer the usual exits: a good-faith discussion, then termination of the affected service with a refund of prepaid unused fees. Add a per-account AI disable switch, which lets the customer keep its data away from the new vendor without leaving. Remember that disabling removes value the customer paid for, so the refund exit still matters.
- **No-training commitments are usually supportable.** Accept them when every relevant subprocessor's terms say so. Draft them as a flow-down ("Provider will contractually require…") so the provider controls compliance and stays responsible.
- **Region:** accept only regions the vendor contract guarantees, including failover.
- **Facts that reverse the answer:**
  - Zero retention has been granted, so a vendor-specific commitment becomes accurate.
  - Single-tenant or bring-your-own-model deployments make a customer-specific veto feasible.
  - The vendor's terms permit training or human review, so even the no-training promise needs work.
  - Applicable law imposes a specific requirement (research needed).

## Common positions (negotiating context, not policy)
- Subprocessor notice of roughly 10 to 30 days is common in multi-tenant SaaS. Regulated customers often ask for 60 to 90.
- Objection rights usually end in termination of the affected service with a pro-rata refund, not a veto.
- Major LLM APIs commonly exclude training on API data. Abuse-monitoring retention measured in weeks is common, with zero retention available only to approved accounts or use cases.
- Customers commonly accept an accurate retention disclosure combined with a disable switch.

## Company position (fill in)
- Standard: ___ (notice period, objection mechanics, disclosed retention)
- Acceptable fallback: ___ (for example, longer notice for model-vendor changes only, or a disable switch plus a refund exit)
- Walk-away: ___ (for example, a veto over shared-service subprocessors, or promises beyond upstream terms)
- Who approves: ___
Apply these as policy only when the user supplies them.

## Worked example
Packet: an enterprise consumer-lending customer that bought the AI mapping feature makes three DPA edits:
- (a) 90 days' notice of new subprocessors instead of 30, and an objection stops Provider using that subprocessor for Customer data.
- (b) No subprocessor retains Customer Personal Data after a request completes.
- (c) No subprocessor trains on Customer Personal Data.

Facts: the model vendor does not train on API data but retains inputs and outputs for up to 30 days for abuse monitoring, and zero retention has not been obtained. The feature can be disabled per account. Policy: 30 days' notice; an objection leads to good-faith discussion, then termination of the affected Service with a refund of prepaid unused fees as the sole remedy; no veto; commitments must match subprocessor facts.

Decision:
- **(b): reject as drafted.** This is what drives the decision, because it is false for the model vendor on day one and arguably for storage subprocessors too. Offer accurate disclosure instead: model-vendor retention of up to 30 days solely for abuse monitoring, under confidentiality, then deleted. Add to that a disable switch and a commitment to seek zero retention.
- **(a) notice: counter to 30 days.**
- **(a) veto: reject.** Offer the policy's termination-and-refund exit, and point out that disabling the feature routes no data to a new model vendor.
- **(c): accept with conditions.** Confirm with the product owner that every subprocessor's terms exclude training, and draft it as a flow-down.

The answer reverses in either of these cases: zero retention is obtained, which supports (b) for the model vendor only; or the customer's regulator requires a specific right, in which case escalate rather than concede.

Related: [AI training and data use](ai-training-and-data-use.md), [customer AI addenda](customer-ai-addenda.md), [security commitments](security-commitments.md), [incident notice](incident-notice.md), [data, confidentiality and AI](../issues/data-confidentiality-and-ai.md).
