# Contract Review

A commercial contract-review skill for AI agents, built by KomodoInsure. Review the connected agreement, preserve approved positions, and draft changes sized to the client’s mandate.

## Install

```sh
npx skills add KomodoInsure/contract-review-skills --skill contract-review
```

For Codex specifically:

```sh
npx skills add KomodoInsure/contract-review-skills --skill contract-review --agent codex
```

Then ask your agent to use `contract-review` with the agreement, your represented party, deal facts and approved playbook. See [usage examples](docs/usage.md).

## Where it helps

- **Negotiation rounds:** distinguish a close-round repair from an expansion that needs new rights, remedies and transition protections.
- **Connected review:** follow definitions, document priority, caps, damages exclusions and post-termination obligations together.
- **Evidence and authority:** separate missing documents, unresolved decisions, proposed terms and approved positions.
- **Usable drafts:** provide anchored edits, external rationales and separate internal decisions; flag incomplete operative language.

Supporting references cover services, SaaS, NDAs, liability, indemnification, IP, data and confidentiality, plus playbooks for eighteen recurring SaaS and AI negotiation asks. The installed package contains guidance and hypothetical examples, with no external service or API-key requirement.

## Release evaluation

In our final four-case development comparison using **Sol 6.1 at medium effort**, the released skill retained **100% core coverage** and scored **90% on drafting quality**, compared with **100% and 82.5%** for the bare-model baseline. Overall rubric adherence was **95.45% versus 92.05%**.

These are model-graded results on familiar authored cases, not an independent legal-quality certification. The observed gain was concentrated in rationale completeness; some rationale failures remain, and judge-choice sensitivity includes a tie. Earlier development results were mixed. Read the [methodology, complete final comparison and limitations](docs/evaluation.md) before interpreting the numbers.

## Judgment evals

[Forty-two authored SaaS and AI cases](evals/README.md) test whether reviews reach the right substantive decision: six original cases, eighteen that exercise the [playbooks](skills/contract-review/references/playbooks/README.md), and eighteen held-out variants that change the deciding facts. In the [latest run](evals/results.md) the skill passed 41 of 42 cases (213/224 criteria) and the bare model passed 38 (207/224). On the held-out variants the skill passed 17 of 18 cases to bare's 15, with equal criterion totals. Its remaining weakness is over-elaborating when a change already matches policy.

## Scope

This is review guidance, not a company playbook or automatic legal approval. Current-law conclusions need appropriate research and professional judgment. Native Word redlines require a capable host document tool; the reported evaluation tested text proposals, not Word editing or automatic reference routing.

[Selected sources and attribution](docs/sources.md) · [MIT license](LICENSE)
