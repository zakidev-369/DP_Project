# Non functional requirements



| ID / priority | Condition | Check |
| --- | --- | --- |
| NFR01<br>Must | Capture isolation. Check top-level navigation, redirects and subrequests against approved hosts and public destination IPs. Block private, loopback, link-local and metadata addresses. Disable downloads and form actions. Use an isolated worker and OS/container egress controls. | V11 |
| NFR02<br>Must | Bounded runtime. Proposed target: scan within 60 seconds on declared hardware. Enforce 30-second navigation and 90-second total job limits. Report p50/p95 and failures for 20 controlled scans. | V12 |
| NFR03<br>Must | Data minimisation. Public pages without login. Exclude input values, cookies and credentials. Keep raw captures out of Git and delete after a proposed 30-day retention period. | V13 |
| NFR04<br>Must | Traceability. Every export has capture ID, model version and timestamp; original predictions remain separate from review decisions. | V14 |
| NFR05<br>Must | Accessibility. Submit, review and export by keyboard. Label inputs, show focus, announce status and use text as well as colour. | V15 |
| NFR06<br>Must | Reproducibility. Pin dependencies, seeds and partitions. Record rerun variation rather than promise bit-identical GPU output. | V07 |
| NFR07<br>Should | Maintainability. Separate API, capture, inference and UI; link every Must requirement to a check and owned task. | V16 |
