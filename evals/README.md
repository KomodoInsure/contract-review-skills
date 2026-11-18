# Judgment evals

Forty-two authored SaaS and AI review cases that test whether the skill reaches the right *substantive* decision for the right reason, not only whether it covers the right clauses. They live outside `skills/` so they are not installed with the skill.

- `cases/` contains the packets a solver sees. Every case reads `_provider-context.md` (a fictional provider's CSA excerpts, tiers, authority and security facts) plus its own deal facts, clause text, playbook excerpt and ask.
- `rubrics/` contains boolean grading criteria fixed before each run. Solvers must not see them.

| Case | Origin | Expected decision |
| --- | --- | --- |
| `governing-law-enterprise` | Adapted from an internal sales-enablement exercise | Accept New York law for an enterprise deal; Irish-law DPA is fine |
| `liability-misrepresentation-renewal` | Adapted from the same exercise | Don't accept as sent; the cap is fine, the vague "material misrepresentation" trigger is the issue |
| `dpa-customer-audit` | Adapted from the same exercise | Reject customer-run audits; offer SOC 2 under NDA, certifications, or dedicated hosting |
| `governing-law-standard-customer` | Held-out variant | Decline English law for a standard-tier customer |
| `liability-cap-over-limit` | Held-out variant | Defined triggers are fine; the 12x multiple is the issue |
| `dpa-regulated-bank-audit` | Held-out variant | Don't apply the no-audit policy blindly; regulation may require access, so escalate |


### Playbook cases

Eighteen cases, one per playbook in `skills/contract-review/references/playbooks/`. Each playbook's worked example is a compressed version of its case. Playbook authors saw the cases but not the rubrics. `_provider-context.md` gained a section of shared facts these cases use (AI feature, model vendor, services, insurance detail, uptime).

| Case | Playbook | Expected decision |
| --- | --- | --- |
| `indemnity-uncapped-breach` | indemnity caps | Uncap only the IP indemnity; reject the breach-of-agreement indemnity |
| `training-derived-data` | AI training and data use | Accept no-training; carve Metadata out of "derived data" |
| `insurance-requirements` | insurance alignment | Counter to coverage actually carried; don't confirm coverage |
| `trigger-negligence-law` | liability triggers | Accept the defined §4 trigger; negligence swallows the cap |
| `breach-supercap-costs` | data breach costs | Accept response costs; strike lost profits; floor controls the cap |
| `ai-output-indemnity` | AI output indemnity | Counter with a conditional indemnity mirroring upstream cover |
| `model-vendor-retention` | AI model subprocessors | The no-retention promise is false today; no veto |
| `warranty-ai-accuracy` | warranties and AI accuracy | Reject the RFP incorporation and the accuracy warranty |
| `services-uncapped` | services liability | Accept the on-site injury indemnity; reject uncapped services |
| `breach-notice-suspected` | incident notice | 48h after confirmation; no suspected-incident duty; customer gives notices |
| `portal-po-terms` | customer paper and PO terms | Click accept; the CSA's no-effect clause governs |
| `data-loss-carveout` | damages exclusion carveouts | Narrow data loss to restoration costs; still capped |
| `output-ownership-learnings` | AI output ownership | Customer owns outputs; Provider keeps improvements and models |
| `ai-use-addendum` | customer AI addenda | Accept disclosures; reject model audits and high-risk classification |
| `change-of-control-consent` | change of control | No consent; competitor-acquirer termination with pro-rata refund |
| `customer-indemnity-deleted` | customer indemnity | Reinstate a narrowed customer indemnity |
| `security-schedule-freeze` | security commitments | Accept met controls; no freeze; mind §4 incorporation |
| `sla-four-nines` | SLA and credits | Reject 99.99%; keep credits as sole remedy; chronic-failure exit |

### Held-out playbook variants

Eighteen variants, one per playbook, that are not in the skill. Each changes the facts that decide the case, and many reverse the answer (accept rather than counter), so they test whether the playbooks generalize instead of matching their own examples.

| Case | Base case | Expected decision |
| --- | --- | --- |
| `indemnity-defined-supercap` | indemnity-uncapped-breach | Accept: IP only uncapped; defined third-party indemnity at $1.5M |
| `training-standard-tier` | training-derived-data | No redline for standard tier; point to the Trust Center commitment |
| `insurance-matching` | insurance-requirements | Accept: limits match coverage carried |
| `trigger-confidentiality-gn` | trigger-negligence-law | Accept: defined §7 obligation and heightened-fault standard |
| `breach-costs-staff-time` | breach-supercap-costs | Accept the 8x cap and listed costs; strike employee time |
| `ai-output-indemnity-conditional` | ai-output-indemnity | Acceptable on substance; needs business-owner approval |
| `subprocessor-us-only` | model-vendor-retention | Accept exit and 30-day retention; US-only is false (EU ticketing) |
| `warranty-documented-capability` | warranty-ai-accuracy | Accept; the service-description change needs approval |
| `services-separate-cap` | services-uncapped | Counter 2x SOW cap to 1x, with approval |
| `breach-notice-within-policy` | breach-notice-suspected | Accept: within policy, processor role respected |
| `portal-po-mismatch` | portal-po-terms | Don't click: the PO adds an unordered item and net 90 |
| `data-loss-narrow-cover` | data-loss-carveout | Accept restoration; cut cover from 30 months to 12 |
| `custom-deliverable-ownership` | output-ownership-learnings | Assign the deliverable; carve out pre-existing tools |
| `ai-disable-default` | ai-use-addendum | Accept default-off; per-user opt-in isn't supported |
| `change-of-control-competitor` | change-of-control-consent | Accept: matches fallback; refund about $146,667 |
| `customer-indemnity-public-entity` | customer-indemnity-deleted | Don't force it; substitute a warranty and escalate |
| `security-schedule-aligned` | security-schedule-freeze | Accept; controls are met, so §4 incorporation is fine |
| `sla-chronic-tighter` | sla-four-nines | Low risk on history; needs business-owner approval |

The first three original cases also appear in compressed form in `skills/contract-review/references/examples/worked-reviews.md`, so they measure whether the skill applies its own examples. The three variants are not in the skill and check that the guidance generalizes, including cases where the opposite answer is right.

## Running

For each arm (skill, bare model), give a solver the case packet and ask it to write one answer per case. The skill arm reads `skills/contract-review/SKILL.md` and the references it routes to; the bare arm reads only the packet. Grade each answer against its rubric with arm labels removed. A case passes when every `[critical]` criterion and the rubric's overall threshold pass.

Results are recorded in [results.md](results.md). These are model-graded results on authored cases with one generation per cell; they show the skill can reach these decisions, not that it reliably will.
