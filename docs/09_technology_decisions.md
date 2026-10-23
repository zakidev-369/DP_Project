# Technology decisions

Three decisions compare three alternatives each. Selections are proposed and require a feasibility spike. Criteria are requirement fit, integration effort and operational complexity, not unmeasured speed claims.

| Decision | Alternatives and tradeoffs | Proposed choice |
| --- | --- | --- |
| API platform | FastAPI: Python schemas/validation [T01]. Django: integrated ORM/admin [T02]. Express: JavaScript middleware [T03], requiring a Python inference boundary. | FastAPI for direct Python integration. FR01–FR06. |
| Storage | SQLite: embedded local store [T04]. PostgreSQL: shared relational service [T05]. MongoDB: flexible documents [T06] with explicit application validation. | SQLite for one-machine pilot; private image files outside DB. Revisit PostgreSQL for concurrent use. |
| Capture | Playwright: Python and isolated contexts [T07]. Selenium: WebDriver ecosystem [T08]. Puppeteer: JavaScript browser control [T09], adding a runtime boundary. | Playwright in isolated worker with fixed viewport, bounded loads and request restrictions. |

- React and TypeScript are planned for the interface. The deadline demonstration is dependency-free HTML.
- Begin with fixed pretrained embeddings and lightweight classifier heads. Defer fine-tuning until a dataset pilot supports it.
- Queue capture and inference jobs, return a scan ID and poll status instead of blocking a long HTTP request.
