# Release evaluation

The release candidate preserved core coverage while improving the measured drafting-quality score in this final development comparison. Its clearest observed gain was explaining more of the consequential changes in its proposed language. This is a bounded result, not evidence of reliable superiority across contracts.

## Final comparison

| Condition | Core contract coverage | Drafting quality | Overall |
| --- | ---: | ---: | ---: |
| Bare model | 100.00% (48/48) | 82.50% (33/40) | 92.05% (81/88) |
| Previous skill | 97.92% (47/48) | 80.00% (32/40) | 89.77% (79/88) |
| Released skill | 100.00% (48/48) | 90.00% (36/40) | 95.45% (84/88) |

Counts are passing criterion judgments, not independent contracts: each answer received two judgments. There were **four cases from two source families**, one generation per condition per case, **12 solver calls and 24 grader calls**. The released skill scored 7.5 percentage points above bare on drafting quality and 3.41 points above bare overall. Core coverage tied. Compared with the previous skill, the release gained 10 points on drafting quality and 5.68 points overall.

## What was tested

Two authored negotiations based on a professional-services form and two on a partnership form, each with a close or expansion mandate. The packets included the full standard form, fictional commercial terms, special terms, client instructions and negotiation history. Source versions and attribution are [listed separately](sources.md). These are not official CUAD, ContractNLI or RedlineBench scores.

Six existing core criteria per task tested the required substantive outcomes. Five additional quality criteria, fixed before the final run, assessed mandate fidelity, determinate drafting, rationale fidelity, delivery usability and connected operative effect. All arms received the same explicit request for an external edits/rationales block and a separate internal decisions list. The skill was not the only source of format instructions.

- Solver: `gpt-6.1-sol`, medium reasoning effort.
- Grader: `gpt-6.1-terra`, medium reasoning effort, two separate judgments per answer, without arm labels in grading prompts.
- Arms: bare minimal base instructions; prior concise negotiation skill; feedback-addressed release candidate.
- Loading: the complete markdown skill package was directly included in the skill-arm prompt. No tools, external research, automatic skill discovery or progressive reference routing were tested.
- Harness: isolated Codex CLI calls with matched minimal model instructions. “Bare” does not mean the absence of all platform instructions or an ordinary default Codex session.
- Scoring: boolean judgments against fixed criteria, averaged across both grades and tasks. Core and quality are shown separately; overall weights all eleven criteria equally.
- Integrity: frozen inputs and candidate files, no answer replacements, favorable regrading, optional sample extension or post-result candidate tuning.

## Strengths and remaining weaknesses

The release received full core credit on all four tasks. It handled scoped licence changes, change-order boundaries, post-term remedies, conditional third-party permissions, limited brand-use exceptions, data-sharing gates and agreed liability treatment. Full core credit does not certify every clause or every plausible dependency.

The quality gain was concentrated in rationale fidelity. The released skill still failed some checks for explaining additional remedies, takedown duties or proposed operational deadlines. A separate internal full-answer review also noted that the previous skill was more explicit about one payment-on-termination interaction. This remains a review concern; neither the model rubric nor the internal inspection establishes exhaustive correctness.

The released skill averaged **2,937.5 output tokens**, compared with **2,670.5** for bare and **2,871.75** for the previous skill. It was not shorter. No cost or latency advantage is claimed.

## How much confidence to place in this

These are familiar development cases, not a held-out confirmation set. They share two forms from one publisher; the labels are authored, not independently established legal ground truth. One generation per cell cannot estimate run-to-run reliability. Model judgments disagree on some criteria. The internal material review knew arm identities and was not independent blinded professional validation.

Selecting between the two original complete judgments for each answer gives an observed released-skill-minus-bare range of **0 to 6.82 percentage points overall**. This is a judgment-sensitivity range, not a confidence interval. It includes a tie. No claim of statistically significant or general superiority is supported.

Earlier development experiments included ties and regressions. This page presents the complete final release comparison, not a pooled account of all experiments. Different prompts, models, tasks or graders must not be compared cell for cell. Feedback from separate reviews informed changes but is not counted as independent validation here.

The candidate was selected under a rule fixed before execution: meet or exceed the previous skill on overall and drafting-quality scores, then pass an internal material review. It met that release rule. Selection among tested versions is not proof of the best possible skill.

## Per-case results

| Case | Condition | Core | Quality |
| --- | --- | ---: | ---: |
| psa_close | bare | 100.00% | 90.00% |
| psa_close | previous_skill | 100.00% | 90.00% |
| psa_close | release_candidate | 100.00% | 100.00% |
| psa_expand | bare | 100.00% | 80.00% |
| psa_expand | previous_skill | 100.00% | 80.00% |
| psa_expand | release_candidate | 100.00% | 90.00% |
| partner_close | bare | 100.00% | 80.00% |
| partner_close | previous_skill | 91.67% | 70.00% |
| partner_close | release_candidate | 100.00% | 90.00% |
| partner_expand | bare | 100.00% | 80.00% |
| partner_expand | previous_skill | 100.00% | 80.00% |
| partner_expand | release_candidate | 100.00% | 80.00% |

[Machine-readable counts and released-file hashes](results.json) support checking these summaries. This public repository intentionally excludes raw review packets, model transcripts, private research, reviewer identities and local environment details. It therefore supports auditing the reported arithmetic, not independently reproducing every model judgment from this repository alone.
