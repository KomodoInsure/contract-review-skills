# Shared packet context (hypothetical)

All names, terms and policies are fictional. They adapt the reasoning of a SaaS provider's internal enablement training; they are not any company's actual playbook.

**Represented party:** Corvid Data, Inc. ("Provider"), a Delaware corporation selling a hosted, multi-tenant data-import service to businesses under its Cloud Service Agreement ("CSA"), with a Data Processing Addendum ("DPA") and a Mutual NDA.

**Reviewer and authority:** You are reviewing for Provider's agreement owner (deal desk counsel). The agreement owner may accept or counter any change that falls within the playbook below. Changes outside the playbook escalate to the business owner (VP Sales), then outside counsel. Only Provider executives sign; nothing is binding until signature.

**Customer tiers:** *Enterprise* customers (annual contract value at or above $100,000, negotiated paper) may negotiate legal terms. *Standard* customers (self-serve or below $100,000) sign the CSA as published; no legal-term redlines.

**CSA term buckets:**
- Commercial (sales negotiates): start date and term, invoice and payment periods, SLA, support, fees, publicity.
- Non-negotiable: service description, acceptable use, security policy (Section 4), warranties (Section 9).
- Legal (agreement owner negotiates within playbook): governing law and venue, indemnity, liability caps, insurance, protected data, metadata.

**Relevant standard CSA text:**
- §4 Privacy and Security: Provider maintains the safeguards in its Security Policy, notifies Customer of a Security Incident affecting Customer Protected Data within 72 hours of confirmation, and processes Protected Data only to provide and improve the Service.
- §9.1 Warranty: the Service will perform materially in accordance with the Documentation during the Term. §9.2 Disclaimer: except as expressly stated in this Agreement, Provider makes no warranties, express or implied, and does not warrant that Customer will achieve any particular result.
- §11 Limitation of Liability: (a) general cap: fees paid or payable in the 12 months before the claim; (b) Increased Claims (currently: breach of §4 resulting from gross negligence or willful misconduct) are capped at 5.0 times the fees paid or payable by Customer in the 12 months immediately before the claim, in lieu of (a); (c) neither party is liable for indirect or consequential damages or lost profits, except for indemnity obligations.
- §14.3 Entire Agreement: this Agreement is the parties' complete agreement and supersedes all prior proposals, statements and representations.
- §15 Governing Law: Delaware law; exclusive jurisdiction of the state and federal courts in Delaware.

**Security and compliance facts:** Provider completes an annual SOC 2 Type II audit by an independent auditor it selects, and an annual third-party penetration test. Reports are shared with customers and prospects under NDA. Provider can offer dedicated (single-tenant) hosting at additional cost. Insurance: $5,000,000 combined cyber and technology E&O.

## Additional facts used by the playbook cases

**More standard CSA text:**
- §4 also defines **Customer Protected Data** as data Customer submits to the Service. **Metadata** means de-identified, aggregated data about use of the Service (for example column-header frequencies and mapping-acceptance rates) that contains no Protected Data and does not identify Customer. Provider owns Metadata.
- §11(a) applies to all claims, including indemnity obligations, except Increased Claims under §11(b).
- §12.1 Provider defends Customer against third-party claims that the Service infringes a US patent, copyright or trademark or misappropriates a trade secret, and pays resulting damages and approved settlements. Exclusions: Customer Protected Data, combinations not supplied by Provider, and modifications not made by Provider. §12.2 Customer defends Provider against third-party claims arising from Customer Protected Data or Customer's breach of the Acceptable Use Policy.
- §13 SLA: 99.9% monthly availability; service credits up to 25% of the monthly fee are Customer's sole remedy for unavailability.
- §14.2 Assignment: neither party may assign without the other's consent, except either party may assign without consent to a successor in a merger, acquisition or sale of substantially all its assets.
- §14.4 Order documents: pre-printed or online terms in any purchase order, vendor registration or procurement portal have no effect, even if acknowledged or accepted.

**AI feature:** "Smart Mapping" suggests column mappings and generates transformation snippets. It sends Protected Data samples to a third-party LLM API ("Model Vendor", a listed subprocessor, US region). Model Vendor's terms: no training on API data; inputs and outputs retained up to 30 days for abuse monitoring (Provider has not obtained zero retention); Model Vendor indemnifies Provider for third-party copyright claims against unmodified outputs generated with its content filters on, excluding claims arising from inputs. Smart Mapping can be disabled per account. Provider does not train any AI model on Protected Data; it uses Metadata to tune mapping suggestions.

**Services:** Provider sells fixed-fee implementation under statements of work (SOWs), mostly remote, occasionally on site.

**Insurance detail:** the $5,000,000 cyber and technology E&O limit is a single annual aggregate shared across all customers and claims, with a $100,000 retention. Commercial general liability (CGL): $1,000,000 per occurrence, $2,000,000 aggregate. The broker has said customers can be added as additional insureds on CGL only, not on cyber or E&O.

**Operations:** trailing-12-month availability 99.95%; worst month 99.86%.
