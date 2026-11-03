# NotebookLM Q4 — observed evaluations

| Test | Observed result | Evidence | Limitation / verification |
|---|---|---|---|
| T01 Source-grounded Q&A | Answered intents, entities, page parameters and routes with visible citation markers | Q4_T01 screenshot | Not all clicked citation passages are independently checked |
| T02 Unsupported question | Stated café opening/closing hours were not in source materials; did not invent hours | Q4_T02 screenshot | Evidence of one refusal, not a guarantee against hallucination |
| T03 Default study guide | Generated six-page revision guide with cloud concepts, quiz and glossary | Study Guide PDF | Overweighted introductory concepts; uneven Week 1–8 coverage; answer key numbering confusing |
| T04 Mind map | Grouped fundamentals, service models, architecture, adoption, automation, DevOps, and data platforms | Expanded mind-map screenshot | Hierarchical overview does not establish depth or correctness of every subnode |
| T05 Quiz | Three answered questions were marked correct: IaaS, containerisation, rehosting | Three quiz screenshots | Only 3/6 questions reviewed; correctness needs validation against course lectures |

Source documents were uploaded to NotebookLM but deliberately not committed to this repository.
