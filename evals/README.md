# Judgment evals

Six authored SaaS review cases that test whether the skill reaches the right *substantive* decision for the right reason, not only whether it covers the right clauses. They live outside `skills/` so they are not installed with the skill.

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

The first three cases also appear in compressed form in `skills/contract-review/references/examples/worked-reviews.md`, so they measure whether the skill applies its own examples. The three variants are not in the skill and check that the guidance generalizes, including cases where the opposite answer is right.

## Running

For each arm (skill, bare model), give a solver the case packet and ask it to write one answer per case. The skill arm reads `skills/contract-review/SKILL.md` and the references it routes to; the bare arm reads only the packet. Grade each answer against its rubric with arm labels removed. A case passes when every `[critical]` criterion and the rubric's overall threshold pass.

Results are recorded in [results.md](results.md). These are model-graded results on authored cases with one generation per cell; they show the skill can reach these decisions, not that it reliably will.
