# Evaluation

## Overview

The proposed framework is evaluated using multiple complementary evaluation protocols covering retrieval quality, answerability prediction, generation quality, hallucination detection, calibration, and end-to-end system performance.

The evaluation combines both automated metrics and LLM-as-a-Judge assessment to provide a comprehensive analysis.

---

# Retrieval Evaluation

The retrieval module is evaluated using:

- Recall@5

The hybrid retrieval pipeline achieves high retrieval coverage, demonstrating effective retrieval of relevant supporting documents.

**Figure**

- Retrieval Recall@5

---

# Answerability Classification

The answerability classifier is evaluated using:

- ROC Curve
- Confusion Matrix

The classifier successfully distinguishes answerable and unanswerable queries while maintaining balanced predictive performance.

**Figures**

- ROC Curve
- Confusion Matrix

---

# End-to-End Decision Evaluation

The adaptive gating framework is evaluated as a complete decision system.

Metrics include:

- Decision Accuracy
- False Abstention Rate
- Unsafe Answer Rate
- Unsupported Claim Rate

**Figures**

- End-to-End Decision Confusion Matrix
- End-to-End Safety Metrics

---

# Generation Quality

Generated responses are evaluated using:

- BERTScore Precision
- BERTScore Recall
- BERTScore F1
- ROUGE-L

Additional analyses examine the relationship between generation quality and system confidence.

**Figures**

- BERTScore Component Spread
- BERTScore Distribution
- BERTScore vs ROUGE-L
- System Confidence vs Actual Generation Quality

---

# Hallucination Analysis

Hallucination behaviour is analyzed using the RAGTruth benchmark.

The evaluation investigates:

- Hallucination frequency
- Hallucination categories
- Predicted hallucination risk
- Risk distribution

**Figures**

- Label Distribution
- Hallucination Rate
- Predicted Hallucination Risk
- Hallucination Risk Boxplot

---

# LLM-as-a-Judge Evaluation

Beyond automatic metrics, generated responses are evaluated using an LLM Judge.

Each response is assessed across several quality dimensions:

- Decision Appropriateness
- Factuality
- Completeness
- Overall Response Quality

**Figures**

- Mean Scores
- Score Distribution
- Correlation Heatmap

---

# Calibration Analysis

Probability calibration is evaluated using:

- Reliability Diagram
- Calibration Bin Occupancy

These analyses verify that predicted answerability probabilities closely match empirical correctness.

---

# Ablation Study

An ablation study compares different adaptive gating policies.

Evaluated policies include:

- Full Adaptive Policy
- Conservative Gate
- Aggressive Gate
- Binary Gate
- No Gating

Performance is analyzed using both success and risk metrics.

**Figures**

- Success Metrics
- Risk Metrics

---

# Summary

The experimental results demonstrate that the proposed answerability-aware framework:

- Improves retrieval quality
- Produces reliable answerability estimates
- Generates more factually grounded responses
- Reduces hallucinations
- Improves decision reliability
- Supports safer deployment of Retrieval-Augmented Generation systems
