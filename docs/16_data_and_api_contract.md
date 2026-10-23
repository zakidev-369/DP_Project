# Data and API contract

Capture records contain scan_id, approved target, timestamp, viewport, evidence references and regions. Each region includes region_id, bounding box in CSS pixels, visible text, selected DOM properties and zero or more supported labels. Review records preserve the original model result.

contracts/openapi.json specifies the planned boundary. Examples are synthetic. Failure and unsupported cases must not become successful clean results.

| Endpoint | Purpose | Result |
| --- | --- | --- |
| POST /scans | Validate and queue | 202 ID; 422 invalid target |
| GET /scans/{scan_id} | Progress and results | 200 state; 404 unknown scan |
| PATCH /scans/{scan_id}/findings/{finding_id}/review | Save reviewer decision | 200 saved; 404 unknown; 422 invalid |
| GET /scans/{scan_id}/report | Export completed scan | 200 JSON; 409 not completed |

- Job states: queued, capturing, analysing, completed, failed. A retry is a separate job.
- Multi-label outputs allow overlapping cues. Scores are not proof of deception or verified probabilities.
- Reviewer state is confirmed, dismissed or uncertain. It must not overwrite predictions.
