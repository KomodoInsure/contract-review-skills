# Judgment eval results — 2026-11-17 (playbooks, final)

One generation per arm per case and one blind model grade per case. The grader saw both answers as "Answer 1" and "Answer 2", with the order alternating by case. Solver and grader: `claude-opus-5-5` subagents in Claude Code (126 agents). The skill arm read `SKILL.md` and the references it routed to; the bare arm read only the packet. Rubrics were fixed before this run. One rubric (`sla-four-nines` #1) was revised after the previous run, as noted in the file.

## Summary

| Case group | Skill: criteria | Skill: cases | Bare: criteria | Bare: cases |
| --- | ---: | ---: | ---: | ---: |
| Playbook cases (18, in the skill) | 100/101 | 18/18 | 96/101 | 18/18 |
| Held-out variants (18, not in the skill) | 80/90 | 17/18 | 80/90 | 15/18 |
| Original cases (6) | 33/33 | 6/6 | 31/33 | 5/6 |
| **Total** | **213/224** | **41/42** | **207/224** | **38/42** |

Skill answers averaged about 6,570 characters, compared with about 5,620 for bare (+17%). On held-out cases the averages were 6,090 and 5,050.

## What the held-out variants show

The held-out variants are the informative signal, because they are not in the skill and many reverse the base case's answer (accept rather than counter). On them the skill passed 17 of 18 cases against bare's 15, and bare's three failures were substantive. On `warranty-documented-capability` it rejected an acceptable reporting commitment. On `data-loss-narrow-cover` it moved the carveouts to the wrong cap. On `change-of-control-competitor` it reopened a clause that matched the fallback.

Criterion totals tied (80/90). The skill lost its points almost entirely on proportionality: when a change already matched policy, it still produced long answers with fallbacks, watch-lists and extra tidying. Nine of its ten held-out misses were concision, "no new objections" or "minor tidying only" criteria. Its one held-out case failure, `change-of-control-competitor` (2/5), reopened a clause that matched the fallback. This is the clearest remaining weakness: the skill is calibrated to find problems and does not yet stop briefly when there are none.

## Per case

### Playbook cases
| Case | Skill | Bare |
| --- | ---: | ---: |
| indemnity-uncapped-breach | 6/6 pass | 5/6 pass |
| training-derived-data | 6/6 pass | 6/6 pass |
| insurance-requirements | 6/6 pass | 5/6 pass |
| trigger-negligence-law | 6/6 pass | 6/6 pass |
| breach-supercap-costs | 6/6 pass | 5/6 pass |
| ai-output-indemnity | 6/6 pass | 6/6 pass |
| model-vendor-retention | 6/6 pass | 6/6 pass |
| warranty-ai-accuracy | 6/6 pass | 6/6 pass |
| services-uncapped | 5/5 pass | 5/5 pass |
| breach-notice-suspected | 5/5 pass | 5/5 pass |
| portal-po-terms | 5/5 pass | 4/5 pass |
| data-loss-carveout | 5/5 pass | 5/5 pass |
| output-ownership-learnings | 5/5 pass | 5/5 pass |
| ai-use-addendum | 5/6 pass | 5/6 pass |
| change-of-control-consent | 5/5 pass | 5/5 pass |
| customer-indemnity-deleted | 5/5 pass | 5/5 pass |
| security-schedule-freeze | 6/6 pass | 6/6 pass |
| sla-four-nines | 6/6 pass | 6/6 pass |

### Original cases
| Case | Skill | Bare |
| --- | ---: | ---: |
| governing-law-enterprise | 5/5 pass | 4/5 **fail** |
| liability-misrepresentation-renewal | 6/6 pass | 6/6 pass |
| dpa-customer-audit | 6/6 pass | 6/6 pass |
| governing-law-standard-customer | 5/5 pass | 5/5 pass |
| liability-cap-over-limit | 6/6 pass | 6/6 pass |
| dpa-regulated-bank-audit | 5/5 pass | 4/5 pass |

### Held-out variants
| Case | Skill | Bare |
| --- | ---: | ---: |
| indemnity-defined-supercap | 5/5 pass | 5/5 pass |
| training-standard-tier | 5/5 pass | 5/5 pass |
| insurance-matching | 4/5 pass | 4/5 pass |
| trigger-confidentiality-gn | 4/5 pass | 5/5 pass |
| breach-costs-staff-time | 5/5 pass | 5/5 pass |
| ai-output-indemnity-conditional | 4/5 pass | 5/5 pass |
| subprocessor-us-only | 4/5 pass | 5/5 pass |
| warranty-documented-capability | 4/5 pass | 3/5 **fail** |
| services-separate-cap | 5/5 pass | 5/5 pass |
| breach-notice-within-policy | 5/5 pass | 4/5 pass |
| portal-po-mismatch | 4/5 pass | 4/5 pass |
| data-loss-narrow-cover | 5/5 pass | 4/5 **fail** |
| custom-deliverable-ownership | 5/5 pass | 4/5 pass |
| ai-disable-default | 4/5 pass | 5/5 pass |
| change-of-control-competitor | 2/5 **fail** | 3/5 **fail** |
| customer-indemnity-public-entity | 5/5 pass | 5/5 pass |
| security-schedule-aligned | 5/5 pass | 4/5 pass |
| sla-chronic-tighter | 5/5 pass | 5/5 pass |

## Failed criteria

- Skill, `ai-use-addendum` #5: Names only item 4 as what drives the decision and groups item 3 with the routine items, so it does not name both 3 and 4.
- Skill, `insurance-matching` #5: Too long for a clause that matches: a full table, six watch items and a 'what would change this' section.
- Skill, `trigger-confidentiality-gn` #5: It counters a change that is within authority: it makes acceptance of §7 conditional on a new clarifier and proposes revised §11(b) text, which the rubric expects not to happen.
- Skill, `ai-output-indemnity-conditional` #3: Proposes to the customer a new '[United States]' limit on copyright claims, which narrows scope beyond what the playbook's conditions require.
- Skill, `subprocessor-us-only` #5: Not concise: it has six sections, including repeated rationale, internal items, fallbacks and a what-would-change list, which go well beyond the verdict, driver and response that were asked for.
- Skill, `warranty-documented-capability` #4: Adds new objections: it tightens the acceptance-rate sentence, adds a check on order-form precedence, and raises possible misrepresentation exposure from the RFP.
- Skill, `portal-po-mismatch` #5: The plain-language opening works for a non-lawyer, but the answer is long and closes with an internal deal-desk legal note (Delaware law, §14.3, clicker authority) that an AE does not need.
- Skill, `ai-disable-default` #5: Not concise, because it adds full clause language, a separate customer reply and a long confirmations list that largely repeat the analysis.
- Skill, `change-of-control-competitor` #3: Goes well beyond minor tidying: it gives a full replacement clause, extends the trigger to asset sales, adds a sole-remedy ask and a public-announcement start for the window, and caps the effective date, which reopens the substance.
- Skill, `change-of-control-competitor` #4: Never says the 30-day notice is manageable; it treats the notice duty only as a breach risk tied to the undefined change of control.
- Skill, `change-of-control-competitor` #5: Not concise: six tidy items, a long replacement clause, a refund table with caveats and a separate decisions list.
- Bare, `indemnity-uncapped-breach` #5: The carve-out is correctly limited to §12.1 and §12.3 is replaced with a third-party indemnity, but the drafted cap is 3.0x fees only ($900,000), and the greater-of-$1,000,000 floor appears only as a fallback rather than as the counter's cap.
- Bare, `insurance-requirements` #6: Gives the $3M cap and warns against implying the $5M covers it, but never says the cap competes with other claims for the same shared aggregate.
- Bare, `breach-supercap-costs` #6: Puts direct-damages treatment and Increased Claims treatment in one row and never explains that one switches off the §11(c) exclusion while the other switches the cap.
- Bare, `portal-po-terms` #5: Not short: it adds lawyerly detail a non-lawyer doesn't need (the §11(b) multiple, the insurance aggregate, a missing amendment clause) and a four-step process that waits on the customer's reply.
- Bare, `ai-use-addendum` #5: Never says which items drive the decision; it gives a rationale for each item but does not name items 3 and 4 as the drivers.
- Bare, `governing-law-enterprise` #2 (critical): Gives Enterprise tier and US law and venue, but never calls New York a common, well-developed commercial jurisdiction, and it argues that the §11(b) cap and §11(c) exclusion may weaken under New York law instead of saying Provider's protections are not materially affected.
- Bare, `dpa-regulated-bank-audit` #5: Covers counsel review and the information needed from the bank, but makes no interim offer of the SOC 2 report under NDA and holds everything back until counsel answers.
- Bare, `insurance-matching` #5: Too long: it adds material that isn't needed, such as affiliate scope, procurement portals, a long list of possible future requests, and the SOC 2 facts.
- Bare, `warranty-documented-capability` #2 (critical): It routes the text to VP Sales but rejects sentence 2 on substance, calling it an ongoing reporting promise that 'stretches the capability exception' and countering it, instead of treating a commitment to share a measured figure as acceptable.
- Bare, `warranty-documented-capability` #4: Adds new objections to sentence 2 (no limit on frequency, confidentiality, control of methodology, the figure becoming a representation) and proposes a counter clause.
- Bare, `breach-notice-within-policy` #3: It never says that 'without undue delay' could require notice before 48 hours, and instead says the words add little real obligation, focusing only on the trigger risk.
- Bare, `portal-po-mismatch` #5: Usable but not short: it is long and includes lawyerly checks (CSA amendment clause, authority analysis, reviewing the buyer's Standard Terms) that go beyond what an AE needs.
- Bare, `data-loss-narrow-cover` #3 (critical): Fails because it rejects 'subject to Section 11(a)' as the wrong cap and rewrites the cap so that Increased Claims fall under §11(b) at about $900,000, instead of stating that both carveouts stay under the §11(a) cap of $180,000.
- Bare, `custom-deliverable-ownership` #5: X.2 leaves the payment condition as bracketed optional text, so the operative assignment trigger is not settled.
- Bare, `change-of-control-competitor` #3: Seven tidy items, including an exclusive-remedy and no-breach clause, non-refundable earned SOW fees, an effective-date cap and asset-sale coverage, go past minor tidying into new substantive asks.
- Bare, `change-of-control-competitor` #5: The verdict and refund are tight, but the seven-item tidy list with sub-bullets makes the whole answer long rather than concise.
- Bare, `security-schedule-aligned` #3: Treats the more-protective rule only as a floor that stops policy changes going below the Schedule; it never says the rule can import stricter Security Policy terms.

## Changes since the previous run

The same day's earlier run covered 24 cases (skill 131/134 and 23/24; bare 127/134 and 22/24). After it:
- The SLA playbook names the higher target together with the deleted sole-remedy clause as the driver, and the `sla-four-nines` rubric was revised to match.
- The data reference tells the reviewer to offer interim measures, such as the audit report under NDA, while escalating.
- `SKILL.md` tells the reviewer to size answers for non-lawyer readers.

All three affected cases passed in this run.

## Reading these results

The 18 playbook cases appear in compressed form as their playbook's worked example, so passing them is expected. With a full packet, the bare model reaches the right verdict in most cases. The skill's advantage is on the critical criteria: naming the driver, keeping separate effects apart, and getting cap arithmetic and the processor role right. This is one generation per cell, one model grader and authored labels. It shows the skill can reach these decisions, not that it reliably will, and it is not a legal-quality certification.

## Skill files evaluated (SHA-256)

```
4a442aa038dea449d7ae39fdd7dd04c1ed0ec82ff6734f7b7a6c9c3e0ee1aa57  SKILL.md
1c742b943bf6cc034e367373b5e15aaaeeaf26fdc4d83da0175e11529ce8a90c  agents/openai.yaml
a81829ea451918af257eca0d4bfbfc2df3c235c20062c54dd28dd2d15f643e55  references/contract-types/nda.md
f3655ce10c5a28dfd433f605031696b4c18d929abb36afb7f3c9ebbd3950a9c1  references/contract-types/saas.md
ea7f7a3b3ad07d693e3c64134504e66d50ee2be0afc8743e3b2a1db87a29c023  references/contract-types/services.md
a4b8dedfa994b88dac5b38ed2e600e45c9d81f9bca4a04517224abe2713661a8  references/document-verification.md
84f64985703bc86f751f4267d05f07b7e43cf5b25fb6657874ad293f511f543f  references/examples/negotiation-rounds.md
f90f0c310c157a4d8d9451e18cf7683256b22eb22749e5f26165192eae06553a  references/examples/worked-reviews.md
831052492687a2c8f524c7baf050f5fd2c97f2390fdb3ecca7f9d989530657a9  references/issues/data-confidentiality-and-ai.md
f378c0b853ffce281758ce2a70f1de15a85b82636b06dee6c7a88e9632513649  references/issues/governing-law-and-disputes.md
e978ad60948dd1b53bc4c7f26b77c7da10b481236df5513878eb4e44b30592a9  references/issues/indemnification.md
088a223f42f6beaf3b62a04591f847c378ae064538566ced54eb55b35e04a97a  references/issues/intellectual-property.md
e2d87bd0368c1c19af701750b7255775b03a7505a8a53a593706a570719a3935  references/issues/liability-and-remedies.md
3ce5561d4c7ac125101da13362de93d17a0d819beb1ed265565ab2d545ed3168  references/playbooks/README.md
e327f098ab4d296a53abdb8b7e8b122aeb2b0d6291f9aa3a42eea6a96e134218  references/playbooks/ai-model-subprocessors.md
049723b91b231d013d86f7e36a621bdc0b648ba35d11cfa17ca9cdad46e72008  references/playbooks/ai-output-indemnity.md
3e4e2cd20eb95ce7d3928a6a59858552b2e7e772874251084bfde32901f99d43  references/playbooks/ai-output-ownership.md
253ca5c211aafea027bd366d7be1e229c604a543b2ac1fbafd4f506e83d77d7e  references/playbooks/ai-training-and-data-use.md
22d6cf06dfb504b036188488ea06a3397071adebb1e16f677b125af9ee1347fe  references/playbooks/change-of-control.md
fc5195a1c327a71f9da0ed14d7c0ce6e05f0cee67c45ec4f638071e1361578b4  references/playbooks/customer-ai-addenda.md
f991c6718d2b4477c13be4e9be89c2e4f676608ad013d2725b15e65ea49a2483  references/playbooks/customer-indemnity.md
1d5e40cbaacff03dc6c718509e3ae2ef11f0fb1106540f9df0ffd0d9f074db36  references/playbooks/customer-paper-and-po-terms.md
7be765485abdb2d6568da8d7da143f676204d8bfcc2b3d6cc94945a3d9766dc4  references/playbooks/damages-exclusion-carveouts.md
eda21d07873e6c4888b53bdf9ae393ee3ccbb1e91a5dd4c10d6cabe64e5e98e0  references/playbooks/data-breach-costs.md
cea2285e1e1391d583018e541240ff3c8e69ce77540deeea234a777248db0254  references/playbooks/incident-notice.md
542b968c6c4be83a14e3ea4b089c7e9469d345eeecaea000923e6a6a0f6277ce  references/playbooks/indemnity-caps.md
c287d485f5204fac9c507bbe2765971610b609947e16a2d4732721dadb283c9a  references/playbooks/insurance-alignment.md
ee3640f471b9be695bc54c4adb54d7fc25ff97ab91f96bb565b1909970a21022  references/playbooks/liability-triggers.md
5ebaa034782707d40b420cd8767cd233e80dba4dfba52bbd9154c54f05c12338  references/playbooks/security-commitments.md
435b5aac3da074ca1392a127a1b3920d50d64be19af6e585165cbbaaf0345029  references/playbooks/services-liability.md
0962dad0d2c98883eb5581e8babf78fa61f982ac2f3891aad584ce321828102a  references/playbooks/sla-and-credits.md
0b03fa8a3a03781bed93250975b44461936d5be74d23f26c74c696b802e3ffa2  references/playbooks/warranties-and-ai-accuracy.md
75d3dd2977549aa219bc7320dc123e1034c7d48aad7bcad593821e3f584a9aac  references/sources.md
```
