# Implementation verification matrix

All checks are planned, not passed. Prototype checks are recorded separately.

| ID | Requirement | Procedure | Expected evidence |
| --- | --- | --- | --- |
| V01 | FR01 | Allowed, malformed, credential-bearing and blocked URLs | Only valid approved targets create jobs. |
| V02 | FR02 | Known capture fixture | Screenshot, coordinates and extracted text agree. |
| V03 | FR03 | Multiple-label and no-cue fixtures | Evidence and version match the contract. |
| V04 | FR04 | Confirm/dismiss/uncertain then reload | Review persists; original prediction is unchanged. |
| V05 | FR05 | Export and parse JSON | Required fields and review state match the screen. |
| V06 | FR06 | Timeout, worker failure and retry | Visible failure and new ID on retry. |
| V07 | FR07/NFR06 | Versioned experiment rerun | Same split manifest, versions, seeds and recorded metrics. |
| V08 | FR08 | Manifest and annotation audit | Complete records, no split leakage and at least 20% independent review. |
| V09 | FR09 | Label and review filters | Correct subset and empty state. |
| V10 | FR10 | Two model runs on one capture | Separate versions, if feature is implemented. |
| V11 | NFR01 | Private IP, redirect, subresource and DNS changes | Network policy blocks disallowed destinations. |
| V12 | NFR02 | 20 controlled scans | Report latency, failure and timeout measurements. |
| V13 | NFR03 | Inspect and expire captures | Forbidden fields absent and raw files deleted. |
| V14 | NFR04 | Trace export to records | Correct capture, model and review references. |
| V15 | NFR05 | Keyboard and assistive-technology review | Primary flow works without mouse or colour-only information. |
| V16 | NFR07 | Coverage audit | Every Must requirement has a check and owner. |
