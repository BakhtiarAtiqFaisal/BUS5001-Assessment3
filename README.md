# BUS5001 Assessment 3 — Experiment Evidence

This repository documents two experiments for **BUS5001 Cloud Platforms and Analytics, Assessment 3**.

## Q3 — ESG message triage

- **LLM:** Google AI Studio, Gemini 3.8 Flash (as displayed during testing).
- **Prompt:** Revised instructions requiring exactly eight JSON fields: `issue_category`, `urgency`, `sentiment`, `followup_required`, `recommended_team`, `escalation_reason`, `data_sensitivity_risk`, and `brief_summary`.
- **Baseline:** Hugging Face zero-shot classification demo, using the same six candidate categories for all three cases.
- **Original results:** `Q3_ESG_Triage/Gemini_JSON/` contains the actual returned JSON; `Screenshots/` contains the original experiment screenshots. `experiment_log.txt` documents the tests and limitations.

| ID | Scenario | Gemini category | Zero-shot category (displayed score) | Agreement |
|---|---|---|---|---|
| T01 | Water leak | Water and facilities | Water and facilities (86%) | Yes |
| T02 | Supplier policy concern | Sustainable procurement | Sustainable procurement (64%) | Yes |
| T03 | Blocked accessible entrance | Accessibility and inclusion | Accessibility and inclusion (86%) | Yes |

**Interpretation:** The models agreed on the main category for all three selected messages. This is not an estimate of general-purpose accuracy; the tiny test set does not cover difficult edge cases. The zero-shot system only returns a category and ranking scores, whereas the LLM generated all eight required fields. Do not treat ranking scores as validated probabilities.

## Q4 — NotebookLM evaluation

- **Scenario:** Academic learning and revision for BUS5001 Cloud Platforms and Analytics.
- **Tests:** Source-grounded questions, unsupported café opening-hours question, default study-guide generation, expanded mind map, and multiple-choice quiz feedback.
- **Evidence:** `Q4_NotebookLM/Screenshots/`, `Q4_NotebookLM/Study_Guide/`, `qa_experiment_log.txt` and `quiz_experiment_log.txt`.
- **Preliminary observations:** The assistant recognised missing café opening hours and did not supply invented times. The study guide was helpful for introductory cloud fundamentals but did not comprehensively cover every selected lecture; its answer-key formatting was imperfect. The expanded mind map grouped major cloud topics; the quiz correctly marked three reviewed questions on IaaS, containerisation and rehosting.

## Scope, privacy and academic integrity

- All included screenshots and outputs are from the student's actual testing sessions; no classification results were fabricated.
- **Original university lecture and workshop PDFs are deliberately excluded.** Do not upload copyrighted source lecture files to a public repository without permission.
- The generated study guide may contain course-derived wording; this folder should be kept in a **private repository** shared only with authorised teaching staff, unless permission to publish is confirmed.
- No API keys, authentication tokens, or confidential student records should be committed.
- The Q1 chatbot demonstration video is submitted separately through Microsoft Stream/Echo365 as instructed.
- Final submitted report should include a link to this repository and an AI-use acknowledgement if required.
