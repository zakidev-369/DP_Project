# Objectives and scope

Multimodal recognition already appears in prior research [R04, R05, R09]. The engineering contribution is a focused web workflow with traceable evidence and reproducible experiments, rather than a claim to be the first multimodal detector.

Initial scope: English-language public pages, one captured desktop viewport, four observable cue categories and a reviewer who makes the final judgement. Regions may carry multiple labels. An empty label set does not establish that the whole page is free of deceptive design.

| Objective | Completion evidence |
| --- | --- |
| O1 Define the problem | 3–5 real user discussions or substantive client agreement, findings and prioritised requirements. |
| O2 Prepare data | 400–600 labelled regions including benign examples, deduplication and at least 20% independent review. |
| O3 Compare models | Text-only, image-only and multimodal runs using identical website-separated partitions. |
| O4 Integrate review | Target validation, capture, inference, evidence review and JSON export. |
| O5 Evaluate outcomes | Per-label precision/recall/F1, macro-F1, benign false positives, runtime and usability. |

- Included: confirmshaming, misleading choice wording, visual interference and urgency cues.
- Excluded: logins, purchases, form submissions, cancellation journeys, mobile apps, legal compliance decisions and exhaustive crawling.
- Failed captures and unsupported inputs must be explicit rather than displayed as clean results.
- Dataset size and success thresholds are proposed targets for supervisor confirmation after a pilot.
