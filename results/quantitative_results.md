# Quantitative Results

## Retrieval Performance

The hybrid retrieval pipeline achieves strong retrieval effectiveness, ensuring that relevant supporting documents are available before generation.

| Metric | Result |
|---------|--------|
| Recall@5 (Validation) | 0.868 |
| Recall@5 (Test) | 0.946 |

---

# Answerability Classification

The Random Forest answerability classifier demonstrates reliable discrimination between answerable and unanswerable queries.

| Metric | Result |
|---------|--------|
| ROC-AUC | 0.764 |

---

# End-to-End Decision Performance

| Metric | Result |
|---------|--------|
| Decision Accuracy | 0.675 |
| Unsafe Answer Rate | 0.167 |
| False Abstention Rate | 0.420 |
| Mean Unsupported Claim Rate | 0.147 |

---

# Generation Quality

Generation quality is evaluated using semantic similarity metrics.

Evaluated metrics include:

- BERTScore Precision
- BERTScore Recall
- BERTScore F1
- ROUGE-L

Distribution plots and correlation analyses are provided in the evaluation figures.

---

# Hallucination Analysis

The framework evaluates hallucination behaviour using RAGTruth.

Evaluation includes:

- Hallucination Rate
- Label Distribution
- Risk Prediction
- Claim Support Analysis

---

# Calibration Analysis

Probability calibration is evaluated using:

- Reliability Diagram
- Calibration Bin Occupancy

The calibrated classifier produces confidence estimates that better align with observed empirical accuracy.

---

# LLM-as-a-Judge Evaluation

Generated responses are assessed using four complementary quality dimensions:

- Decision Appropriateness
- Factuality
- Completeness
- Overall Quality

These evaluations complement automatic metrics by providing a holistic assessment of response quality.

---

# Ablation Study

The adaptive gating mechanism is compared against multiple alternative policies.

The proposed adaptive policy consistently provides a favorable balance between:

- Retrieval effectiveness
- Generation quality
- Hallucination mitigation
- Decision reliability
- System safety
