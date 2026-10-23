# Existing system comparison

Four published research systems are compared using eight common criteria. Entries reflect cited descriptions, not independent reproduction. “Not established” means the reviewed source does not establish the feature. The proposal has not been benchmarked against these tools.

| Criterion | Mathur [R01] | AidUI [R04] | UIGuard [R05] | DPGuard [R09] |
| --- | --- | --- | --- | --- |
| Setting | Shopping web | Web/mobile screenshots | Mobile apps | Web/mobile UIs |
| Input | Crawled web text | Screenshot cues | UI properties and text | Multimodal UI input |
| Approach | Collection and expert analysis | Vision plus text cues | Knowledge-driven checks | Multimodal large-model reasoning |
| Output | Mined instances | Types and localised regions | Detected types | Detected patterns |
| Benign data | Not a matched classifier here | Benchmark-specific | Explicit benign UI data | Classifier stage described |
| Browser DOM fusion | Not proposed fusion | Not established | Mobile rather than web DOM | Not established |
| Multi-step coverage | Not comprehensive | Screenshot limitation | Screen context emphasis | Depends on supplied context |
| Transfer limit | Shopping/text scope | Category and data coverage | Mobile-to-web transfer | Service and prompt dependence |

- Proposed distinction: a local four-label web review workflow with aligned screenshot/text/DOM evidence and reviewer corrections.
- Published accuracy figures use different tasks and datasets, so they are not presented as a league table.
- Implementation and evaluation are required before claiming an advantage.
