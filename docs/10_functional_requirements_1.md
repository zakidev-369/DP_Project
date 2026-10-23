# Functional requirements 1

These are acceptance criteria for the future implemented system. The mockup demonstrates interaction and does not satisfy capture or model requirements.

| ID / priority | Behaviour and acceptance | Owner / check |
| --- | --- | --- |
| FR01<br>Must | Submit a target. Reject malformed URLs, credentials, non-HTTPS targets and hosts outside the configured allowlist. Valid requests return scan ID and queued status. | Zaki<br>V01 |
| FR02<br>Must | Capture evidence. Save 1366×768 screenshot, visible text, region coordinates, permitted DOM features, timestamp and viewport. Capture failures produce an error state. | Zaki<br>V02 |
| FR03<br>Must | Show findings. Display supported labels, evidence, model score and model version for each region. Scores are not labelled as calibrated probabilities. | Both<br>V03 |
| FR04<br>Must | Record review. Confirm, dismiss or mark uncertain with a note. Preserve original model output separately from the reviewer decision. | Zaki<br>V04 |
| FR05<br>Must | Export report. JSON includes target, status, timestamp, version, evidence references and review decisions. Failed scans remain explicit. | Zaki<br>V05 |
