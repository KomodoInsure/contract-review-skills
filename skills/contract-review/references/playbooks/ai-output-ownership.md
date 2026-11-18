# AI output ownership

Use for clauses allocating ownership of AI outputs, prompts and inputs, fine-tuned or customer-specific models, derived improvements, templates and "learnings," and for whether the provider may produce similar outputs for others.

## Read first

- The inventory, item by item: customer inputs and prompts; outputs generated for the customer; customer-specific artifacts (fine-tunes, configurations, custom templates under an SOW); provider background (service, base and tuned models, template libraries, weights); usage data or metadata and its existing ownership clause; know-how. See [IP](../issues/intellectual-property.md).
- How outputs are produced: from the customer's data alone, from shared models and libraries, or from a third-party model. The same or substantially similar output can be generated for many customers.
- The upstream model terms: does the model vendor assign or disclaim output rights to the provider? The provider cannot assign what it never received.
- The definitions the clause relies on. Is "Outputs" defined, and does it exclude provider background? Do "improvements," "models," "learnings" or "derived from use" have determinate meanings?
- How confidentiality, data-use and training terms already treat outputs that contain customer data. See [data/confidentiality](../issues/data-confidentiality-and-ai.md) and [AI training and data use](ai-training-and-data-use.md).

## What drives the decision

Separate the customer's legitimate interest from the overreach. Customers usually need freedom to use, modify and commercialize what the tool produced for them and assurance that the provider will not claim it. Owning the provider's general improvements gives them nothing practical but would encumber the provider's product.

- **Outputs generated for the customer:** usually low cost to concede "as between the parties," as an assignment of whatever rights the provider has, with no warranty of protectability, novelty or uniqueness. Whether AI-generated output attracts copyright or other protection is unsettled and jurisdiction-specific. Contractual ownership does not create statutory rights, so research the point rather than promising exclusivity it cannot deliver.
- **Similar outputs for others:** an ownership clause without a reservation can be read to bar the provider from generating the same mapping, code or text for another customer. Add an express statement that outputs are not unique and that similar outputs generated independently for others are not the customer's.
- **Improvements, models, templates, learnings, metadata:** assignment of anything "derived from use" reaches the provider's shared models, tuning, libraries and metadata, which every customer's use improves. It conflicts with retained-IP and metadata clauses, cannot be performed for multi-tenant learning, and "learnings" is indeterminate. Reject it and address the underlying concern through confidentiality and data-use limits.
- **Customer-specific artifacts:** a model or template built only for one customer, solely from its data, is more negotiable. Exclusivity, a usage restriction, or deletion at exit usually serves the interest better than transferring weights that embed the provider's base model.
- **Inputs and prompts:** the customer normally keeps them. Check whether a "prompts" definition sweeps in provider-authored system prompts or templates.

Facts that change the answer: a custom deliverable the customer paid to own under an SOW; outputs that contain the customer's confidential data (treat them as customer data, but do not make them provider-unusable as patterns); a mandate that requires the provider to keep the right to reuse; upstream terms that withhold output rights.

## Common positions (negotiating context, not policy)

Many AI and SaaS terms say that, as between the parties, the customer owns its inputs and outputs, with the provider assigning any rights it has. They often add that outputs may not be unique and that the provider keeps the service, models, improvements and aggregated or de-identified usage data. Customer-specific fine-tunes are variously kept exclusive, deleted at exit or treated as provider property restricted to the customer's use. Assignment of general improvements to a single customer is rare outside bespoke development.

## Company position (fill in)

Apply only when the user supplies it. Standard: ___. Acceptable fallback: ___ (for example, customer-specific artifacts kept exclusive). Walk-away: ___ (for example, any assignment of models, libraries or metadata). Who approves: ___.

## Worked example

Packet: an enterprise customer ($400,000 a year) adds "As between the parties, Customer owns all Outputs. Provider hereby assigns to Customer all right, title and interest in Outputs and in all improvements, models, mapping templates and learnings derived from Customer's use of the Service." "Outputs" is not defined in the agreement. Metadata (de-identified aggregates) is provider-owned and used to tune suggestions; no model is trained on customer data. Policy: the customer may own the outputs generated for it, with the provider assigning whatever rights it has; the provider keeps the service, models, configurations, template library, metadata and know-how, and may generate similar outputs for others.

Decision: accept the first sentence with conditions; reject the second clause's improvements, models, templates and learnings. That clause drives the decision: it would hand one customer the shared tuning and template library that serve every customer and contradict provider ownership of metadata. Counter: define Outputs as the mappings and transformation snippets the feature generates for Customer, excluding the Service, models, configurations, the template library and Metadata; "Provider assigns to Customer whatever right, title and interest it has in Outputs"; add that Outputs may not be unique and that the provider may generate the same or similar outputs for others; preserve retained-IP and Metadata clauses. The ownership concession is within the agreement owner's authority; anything beyond it escalates. Before conceding, confirm the model vendor's terms give the provider output rights. Do not represent that the outputs are protectable. Reverse: a bespoke template built under a paid SOW from this customer's data alone could be assigned or made exclusive. Missing upstream output rights would limit the assignment to "whatever rights Provider has" and need disclosure.
