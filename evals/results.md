# Judgment eval results — 2026-11-17

One generation per arm per case; one blind model grade per answer (arm labels hidden). Solver and grader: `claude-opus-5-5` subagents in Claude Code. The skill arm read `SKILL.md` and the references it routed to; the bare arm read only the packet.

| Case | Skill: criteria | Skill: case | Bare: criteria | Bare: case |
| --- | ---: | :---: | ---: | :---: |
| governing-law-enterprise | 5/5 | pass | 4/5 | **fail** |
| liability-misrepresentation-renewal | 6/6 | pass | 6/6 | pass |
| dpa-customer-audit | 6/6 | pass | 6/6 | pass |
| governing-law-standard-customer | 5/5 | pass | 5/5 | pass |
| liability-cap-over-limit | 6/6 | pass | 5/6 | pass |
| dpa-regulated-bank-audit | 4/5 | pass | 4/5 | pass |
| **Total** | **32/33** | **6/6** | **30/33** | **5/6** |

Failed criteria:
- Skill, `dpa-regulated-bank-audit` #5: next steps did not offer the SOC 2 report under NDA as an interim measure.
- Bare, `governing-law-enterprise` #2 (critical): accepted New York by checking the playbook alone, without explaining why the change is substantively low-risk.
- Bare, `liability-cap-over-limit` #6: the customer reply disclosed the internal multiple ceiling and the insurance limit.
- Bare, `dpa-regulated-bank-audit` #4: stated specific regulatory citations as settled.

## Reading these results

With a complete packet (playbook excerpt, authority, tier and existing clause text), the bare model also reaches the right decision in most cases. An earlier probe on the same three source exercises, using a thinner packet with no playbook positions, showed the gap this work targets: the previous skill headlined every case as "do not accept, route to legal", weighted the cap and the gross-negligence change as heavily as the vague trigger, recommended aligning the DPA's governing law with the CSA, and granted a guarded customer audit right. In this run the skill named the driving issue in each case, kept the verdict separate from approval routing, and left the split governing law alone. The held-out variants, where the opposite answer is correct, also passed.

The first three cases are summarized in the skill's worked examples, so passing them is expected. Treat the held-out variants as the more informative signal. With six authored cases, a single generation and one model grader, these results show the skill can reach these decisions. They are not a reliability estimate or a legal-quality certification.

## Skill files evaluated (SHA-256)

```
91f6284051873490b706a037e494fed438e63145eda8b8999378a311423f4c42  SKILL.md
1c742b943bf6cc034e367373b5e15aaaeeaf26fdc4d83da0175e11529ce8a90c  agents/openai.yaml
a81829ea451918af257eca0d4bfbfc2df3c235c20062c54dd28dd2d15f643e55  references/contract-types/nda.md
93afdfc3dd9729bab7d63ae4c31dc6712ca964e9e8a4f4325136f31ca48931e5  references/contract-types/saas.md
ea7f7a3b3ad07d693e3c64134504e66d50ee2be0afc8743e3b2a1db87a29c023  references/contract-types/services.md
a4b8dedfa994b88dac5b38ed2e600e45c9d81f9bca4a04517224abe2713661a8  references/document-verification.md
84f64985703bc86f751f4267d05f07b7e43cf5b25fb6657874ad293f511f543f  references/examples/negotiation-rounds.md
f90f0c310c157a4d8d9451e18cf7683256b22eb22749e5f26165192eae06553a  references/examples/worked-reviews.md
cc6435f73b2f47d5b35868d0760761f10063502b4b6c096da9c885abdce427d0  references/issues/data-confidentiality-and-ai.md
f378c0b853ffce281758ce2a70f1de15a85b82636b06dee6c7a88e9632513649  references/issues/governing-law-and-disputes.md
e978ad60948dd1b53bc4c7f26b77c7da10b481236df5513878eb4e44b30592a9  references/issues/indemnification.md
088a223f42f6beaf3b62a04591f847c378ae064538566ced54eb55b35e04a97a  references/issues/intellectual-property.md
e2d87bd0368c1c19af701750b7255775b03a7505a8a53a593706a570719a3935  references/issues/liability-and-remedies.md
75d3dd2977549aa219bc7320dc123e1034c7d48aad7bcad593821e3f584a9aac  references/sources.md
```
