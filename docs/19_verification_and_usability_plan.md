# Verification and usability plan

Checks V01–V16 in docs/verification_matrix.md define future implementation acceptance. They are not reported as passed. Prototype checks are recorded separately.

After consent, run a small formative usability exercise with 3–5 representative users. This is distinct from the initial needs discussions. Ask users to inspect one flag, dismiss a false alarm, export a result and explain the limitations.

Record task completion, time, mistakes and interpretation. Proposed goal: at least 80% task completion and correct recognition that flags require human review. Report actual counts and the small sample.

| Check | Requirements | Procedure and expected evidence |
| --- | --- | --- |
| V01 | FR01 | Allowed, malformed, credential-bearing and blocked URLs: Only valid approved targets create jobs. |
| V02 | FR02 | Known capture fixture: Screenshot, coordinates and extracted text agree. |
| V04 | FR04 | Confirm/dismiss/uncertain then reload: Review persists; original prediction is unchanged. |
| V05 | FR05 | Export and parse JSON: Required fields and review state match the screen. |
| V07 | FR07/NFR06 | Versioned experiment rerun: Same split manifest, versions, seeds and recorded metrics. |
| V08 | FR08 | Manifest and annotation audit: Complete records, no split leakage and at least 20% independent review. |
| V11 | NFR01 | Private IP, redirect, subresource and DNS changes: Network policy blocks disallowed destinations. |
