# AI training and data use

Scope: customer requests to limit how a provider uses customer data, covering no-training commitments, "provide and improve" purpose clauses, and the reach of those limits into derived, aggregated, usage data and metadata.

## Read first
- Map every data class and its definition: customer content or protected data, personal data, outputs generated for the customer, usage/telemetry, metadata, feedback and "derived" data. Check whether the definitions exclude each other or whether a redline makes them overlap. If metadata is "derived from" customer data and the customer-data definition now includes derived data, the provider's metadata right may disappear without anyone saying so.
- Establish what the product actually does. Find out which models exist, who trains them, on what data, and whether customer data is used for fine-tuning, evaluation sets, retrieval indexes, prompt caching, human review or debugging. Confirm with the product owner how metadata is produced: the aggregation level, minimum cohort sizes, whether raw strings (such as column headers or field names) survive, and whether it can identify the customer or individuals.
- Read upstream model-vendor terms. A no-training promise about "Provider" says nothing about subprocessors unless it is drafted to cover them, and a promise that covers them is only true if the vendor terms support it. See [AI model subprocessors](ai-model-subprocessors.md).
- Check whether the data is regulated (health, financial, children's data). Sector law can control de-identification and secondary use, so research the applicable rule rather than assuming the contract's definition settles it.

## What drives the decision
- **Routine:** no training or fine-tuning of any AI model on customer data, and limiting processing of customer data to providing the service to that customer. If the product already works this way, these commitments cost little and answer the customer's real security question. Keep narrow purposes the service needs: security, abuse prevention, support the customer requests, and compliance with law.
- **Changes risk:** extending the restriction to data "derived from" customer data, to "improving" models, or to "any other product or service". Any of these can capture de-identified metadata, aggregate analytics and product telemetry. Deleting "improve" from the purpose clause can do the same if metadata is created by processing customer data. The problem is the drafting technique, not the customer's goal. Answer it by excluding metadata expressly and keeping the training prohibition, not by rejecting the protection.
- **Outputs belong with the customer's data.** Transformed data or outputs the service generates for the customer can reasonably be protected like customer data. Metadata that is aggregated across customers cannot.
- **Facts that reverse the answer:**
  - The provider does train on customer data, uses it for evaluation sets, or keeps it in shared retrieval indexes. The no-training promise is then untrue and needs a product decision first.
  - Metadata keeps raw customer strings, works at single-customer granularity, or could re-identify. The customer's concern is then valid; tighten the metadata definition (aggregation, thresholds, no raw values) instead of defending it.
  - Regulated data is in scope with its own de-identification standard.
  - The customer's product is itself the training corpus, as in custom-model deals, which need a bespoke allocation.
- Check each "no use" clause for unintended reach: support tickets, logs, backups and security analytics all contain customer data.

## Common positions (negotiating context, not policy)
- Enterprise SaaS commonly commits to no training on customer content, often including the provider's model vendors. The provider usually keeps rights in aggregated, de-identified usage data that does not identify the customer.
- Customers increasingly ask for aggregation thresholds, a ban on re-identification, and a ban on disclosing usage data to third parties in a customer-identifiable form. These are usually tradeable.
- Some providers offer an opt-out from product-improvement uses of usage data for large customers. Few give up aggregate analytics entirely.

## Company position (fill in)
- Standard: ___ (for example, the training commitment, the purpose limit, and the metadata/usage-data rights retained)
- Acceptable fallback: ___ (for example, aggregation thresholds, a no-re-identification covenant, or per-customer opt-out)
- Walk-away: ___ (for example, any restriction on de-identified aggregate metadata)
- Who approves: ___
Apply these as policy only when the user supplies them. Otherwise label proposals as negotiating positions.

## Worked example
Packet: an enterprise customer (US health-benefits administrator, no PHI in scope) edits the purpose clause from "provide and improve the Service" to "provide the Service to Customer". It adds "Provider shall not use Customer Protected Data, or any data derived from it, to train, fine-tune or improve any AI model or any other product or service", and expands Customer Protected Data to "including all data derived from such data". Under the existing terms, Metadata (de-identified, aggregated usage data such as column-header frequencies) is provider-owned and is used to tune the AI mapping feature. The model vendor's terms prohibit training on API data. Policy: the agreement owner may accept a no-training commitment and a purpose limit, and Metadata rights must be preserved.

Decision:
- **Purpose limit:** accept with conditions. Add that Provider may create and use Metadata as defined, and keep security and legal-compliance purposes.
- **No-training sentence:** counter. Keep "shall not use Customer Protected Data to train or fine-tune any AI model", which is true for Provider and its model vendor. Strike "or any data derived from it", "improve" and "any other product or service", because together they bar using Metadata to tune Smart Mapping.
- **Definition:** counter. Protect outputs generated for Customer, but expressly exclude Metadata. As drafted, Metadata would become Customer Protected Data, which contradicts its own definition.

The derived-data reach is what drives the decision; the training ban itself is within policy. Proposed definition: "'Customer Protected Data' means data Customer submits to the Service and output the Service generates from it for Customer; it does not include Metadata." Offer to state Metadata's aggregation and no-re-identification limits in the contract. The answer reverses in any of these cases: Metadata keeps raw headers that are traceable to Customer, PHI enters scope, or the product owner cannot confirm that no customer samples are used for evaluation or tuning. Relinquishing Metadata needs escalation.

Related: [data, confidentiality and AI](../issues/data-confidentiality-and-ai.md), [SaaS](../contract-types/saas.md), [AI output ownership](ai-output-ownership.md), [customer AI addenda](customer-ai-addenda.md).
