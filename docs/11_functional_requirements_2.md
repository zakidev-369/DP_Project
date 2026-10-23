# Functional requirements 2

These are acceptance criteria for the future implemented system. The mockup demonstrates interaction and does not satisfy capture or model requirements.

| ID / priority | Behaviour and acceptance | Owner / check |
| --- | --- | --- |
| FR06<br>Must | Track progress. Show queued, capturing, analysing, completed or failed. Timeout errors are visible; retries create new IDs. | Zaki<br>V06 |
| FR07<br>Must | Run experiments. Record split manifests, configuration, seed, dependency/model versions and per-label metrics for three modality conditions. | Akbar<br>V07 |
| FR08<br>Must | Track annotation. Every accepted example has provenance, coordinates, labels, annotator, review state and site group. Independently review at least 20%. | Akbar<br>V08 |
| FR09<br>Should | Filter results. Filter by label and review state, preserving data and showing a useful empty state. | Zaki<br>V09 |
| FR10<br>Could | Compare runs. Compare two versioned model outputs on the same saved capture. Defer if Must requirements need time. | Both<br>V10 |
