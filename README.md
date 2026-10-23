# Multimodal AI for detecting deceptive design patterns

Diploma project by **Zaki Sadaqatzada (SE-2402)** and **Akbar Khalili (SE-2409)**, Software Engineering.

Supervisor: **Ахметжанова Шынар Егеубаевна**.

The proposed application helps web developers, designers and QA reviewers inspect suspected deceptive cues using screenshots, visible text and DOM features. It shows evidence for human review and compares text-only, image-only and multimodal models on unseen websites.

## Status for 24 October 2026

Analysis and design package with an offline demonstration. There is no trained detector, completed dataset, production capture service or measured detection accuracy in this submission. User discussions, supervisor feedback and a real YouTrack project require completion or links from the team.

## Scope

English-language public pages, one desktop viewport and four labels: confirmshaming, misleading choice wording, visual interference and urgency cues. Findings are suspected cues, not proof of intent or legal non-compliance. Login flows, purchases and multi-step cancellation patterns are excluded.

## Responsibilities

- Zaki: interface, capture worker, API, integration and system testing.
- Akbar: labels, dataset, baselines, multimodal inference and evaluation.
- Both: research, requirements, review, supervisor discussions and defense.

## Materials

- [Report PDF](submission/Pre_Defense_Report.pdf)
- [Presentation PDF](submission/Pre_Defense_Presentation.pdf)

- [Documentation index](docs/INDEX.md)
- [Editable diagrams and exports](diagrams/)
- [Offline demonstration](prototype/index.html)
- [Proposed API contract](contracts/openapi.json)
- [Owned task backlog](planning/task_backlog.md)
- [Submission steps](planning/submission_steps.md)
- [Supervisor feedback log](planning/supervisor_feedback.md)

## Run the prototype

Download or clone the repository and open prototype/index.html in a modern browser. No installation, keys or network access are needed. Choose a synthetic scenario, run it, inspect findings, record a review and export JSON. The target URL is illustrative and is not fetched. See [prototype checks](tests/prototype_checks.md).

## Planned implementation

React and TypeScript interface, FastAPI service, Playwright worker, SQLite metadata, private evidence files and Python model experiments. Pin versions after a feasibility spike. Add service setup and test commands when runnable service code exists.

## Tracking and review

YouTrack: **pending actual project link**. Transfer the backlog into real assigned tasks; local P labels are not YouTrack IDs. Link task IDs to branches, commits and pull requests. Obtain peer review before merging to main.

Each student uses their own account and records genuine incremental contributions. Do not backdate work or create artificial history. Create the immutable pre-defense-1 tag only after the accepted submission commit is reviewed.

## Public repository data policy

Do not commit credentials, GPA letters, personal contact details, identifiable interview notes or unreviewed third-party screenshots. Included interface examples and findings are synthetic. Check data and model licences before redistribution.

## Automated demonstration logic checks

With Node.js installed, run `node tests/prototype_logic.cjs` from the repository root. This uses built-in modules and a simulated DOM. It does not validate browser rendering, accessibility, live capture or model accuracy.
