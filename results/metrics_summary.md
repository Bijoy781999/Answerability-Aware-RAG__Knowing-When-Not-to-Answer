# Metrics Summary

## Retrieval

| Metric | Value |
|---------|------:|
| Recall@5 (Validation) | 0.868 |
| Recall@5 (Test) | 0.946 |

---

## Answerability Classification

| Metric | Value |
|---------|------:|
| ROC-AUC | 0.764 |

---

## End-to-End Decision Metrics

| Metric | Value |
|---------|------:|
| Decision Accuracy | 0.675 |
| Unsafe Answer Rate | 0.167 |
| False Abstention Rate | 0.420 |
| Mean Unsupported Claim Rate | 0.147 |

---

## Generation Quality

The project evaluates generation quality using:

- BERTScore Precision
- BERTScore Recall
- BERTScore F1
- ROUGE-L

Refer to the evaluation figures for score distributions and correlations.

---

## Hallucination Evaluation

The hallucination analysis includes:

- Hallucination Rate
- Predicted Hallucination Risk
- Hallucination Label Distribution
- Risk Distribution

---

## Calibration

Calibration quality is evaluated using:

- Reliability Diagram
- Calibration Bin Occupancy

---

## LLM-as-a-Judge

Responses are evaluated across four dimensions:

- Decision Appropriateness
- Factuality
- Completeness
- Overall Quality

---

## Ablation Study

Five decision policies are compared:

- Full Adaptive Policy
- Conservative Gate
- Aggressive Gate
- Binary Gate
- No Gate

The adaptive policy provides the best trade-off between reliability and hallucination mitigation.
