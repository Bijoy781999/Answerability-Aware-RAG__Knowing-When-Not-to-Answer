# Evaluation Summary

## Overview

The proposed **Answerability-Aware Retrieval-Augmented Generation (AURA-RAG)** framework was evaluated across multiple dimensions, including retrieval effectiveness, answerability prediction, generation quality, hallucination mitigation, probability calibration, and end-to-end decision making.

The evaluation combines benchmark datasets, automated metrics, calibration analysis, and LLM-as-a-Judge assessment to provide a comprehensive understanding of system performance.

---

# Retrieval Performance

The hybrid retrieval pipeline combines BM25 lexical retrieval with dense semantic retrieval to improve document coverage.

### Evaluation Metric

- Recall@5

### Result

The retrieval module demonstrates high recall, indicating that relevant supporting documents are successfully retrieved before generation.

**Figure**

- Retrieval Recall@5

---

# Answerability Classification

The answerability classifier predicts whether the retrieved evidence is sufficient to answer a query.

### Evaluation

- ROC Curve
- Confusion Matrix

The classifier effectively separates answerable and unanswerable questions while maintaining reliable probability estimates after calibration.

**Figures**

- ROC Curve
- Confusion Matrix

---

# End-to-End Decision Quality

The adaptive gating mechanism determines whether the system should:

- Generate an answer
- Request additional evidence
- Abstain

The evaluation measures both decision accuracy and system safety.

**Figures**

- End-to-End Decision Confusion Matrix
- End-to-End Safety Metrics

---

# Generation Quality

Generated responses are evaluated using semantic similarity metrics.

Evaluation includes:

- BERTScore Precision
- BERTScore Recall
- BERTScore F1
- ROUGE-L

Additional analyses investigate the relationship between system confidence and answer quality.

**Figures**

- BERTScore Component Spread
- BERTScore Distribution
- BERTScore vs ROUGE-L
- System Confidence vs Actual Generation Quality

---

# Hallucination Analysis

Hallucination behaviour is evaluated using the RAGTruth benchmark.

The analysis measures:

- Hallucination frequency
- Label distribution
- Predicted hallucination risk
- Risk separation

**Figures**

- RAGTruth Label Distribution
- Hallucination Rate by Label
- Mean Predicted Hallucination Risk
- Hallucination Risk Boxplot

---

# Calibration Analysis

Reliable confidence estimation is essential for adaptive decision making.

The classifier is evaluated using:

- Reliability Diagram
- Calibration Bin Occupancy

These analyses demonstrate improved agreement between predicted confidence and empirical correctness.

---

# LLM-as-a-Judge Evaluation

Beyond automated metrics, generated responses are assessed using an LLM Judge.

Evaluation dimensions include:

- Decision Appropriateness
- Factuality
- Completeness
- Overall Quality

Correlation analysis demonstrates consistency among these evaluation dimensions.

---

# Ablation Study

Different gating strategies are compared to understand the contribution of adaptive decision making.

Policies include:

- Full Adaptive Policy
- Conservative Gate
- Aggressive Gate
- Binary Gate
- No Gate

Results show the proposed adaptive policy provides the best balance between answer quality and system safety.

---

# Conclusion

The experimental results demonstrate that integrating answerability prediction, probability calibration, and adaptive gating enables more reliable Retrieval-Augmented Generation by reducing hallucinations while maintaining high retrieval effectiveness and response quality.
