# Model experiments and evaluation

RQ1 Does multimodal fusion improve macro-F1 over the best unimodal model on unseen websites? RQ2 Which labels and conditions cause false positives? RQ3 Can reviewers interpret evidence and complete the workflow?

Use identical accepted samples and website-grouped partitions. Use TF-IDF plus a linear classifier as a simple text baseline. For the matched comparison, use the same fixed pretrained text and image encoders in all conditions: text-only, image-only, and concatenated text/image embeddings with normalised DOM features. Train comparable lightweight heads per label. Record encoder identity, licence and versions when selected.

Tune only on validation data. Fit vocabularies, scalers and dimensionality reduction only on training data. Select configuration before held-out testing. If necessary, use grouped cross-validation within training while preserving a final test set.

| Metric | Definition |
| --- | --- |
| Per-label precision/recall | TP/(TP+FP) and TP/(TP+FN); report support and zero-denominator policy. |
| Macro-F1 | Mean F1 across the four labels, accompanied by all per-label values. |
| Benign false-positive rate | Benign regions with any predicted label / all benign regions. Report counts. |
| Fusion improvement | Multimodal macro-F1 minus best unimodal macro-F1 on the same test split. Bootstrap by website where feasible. |
| Runtime and coverage | p50/p95, capture failures, unsupported inputs and declared hardware. |

- Provisional targets: macro-F1 at least 0.70 and benign false-positive rate at most 0.15. These are planning targets, not measured results or university rules.
- A negative fusion result is valid if methods and limitations are documented. Do not repeatedly tune to test errors.
