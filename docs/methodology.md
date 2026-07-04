# Methodology

## Overview

AURA-RAG introduces an **answerability-aware adaptive gating framework** that reduces hallucinations in Retrieval-Augmented Generation (RAG) systems by estimating answerability before generation.

Instead of generating an answer for every query, the system predicts whether sufficient evidence exists in the retrieved context and dynamically selects one of three actions:

- Answer
- Request More Evidence
- Abstain

This prevents unsupported responses and improves factual reliability.

---

# Overall Pipeline

The system consists of five major components:

1. Hybrid Retrieval
2. Answerability Feature Extraction
3. Adaptive Gating
4. Response Generation
5. Hallucination Risk Analysis

---

# 1. Hybrid Retrieval

Relevant context is retrieved using a hybrid retrieval strategy combining:

- BM25 lexical retrieval
- Dense semantic retrieval

The retrieval scores are combined using a weighted hybrid score.

This approach improves retrieval robustness for both keyword-heavy and semantic queries.

---

# 2. Answerability Feature Extraction

After retrieval, the system extracts several features describing the quality of the retrieved evidence.

Examples include:

- BM25 score
- Dense similarity score
- Context relevance
- Semantic similarity
- Query complexity
- Context coverage

These features are used as input to the answerability classifier.

---

# 3. Answerability Classification

A Random Forest classifier predicts the probability that a question can be answered using the retrieved context.

To improve probability estimates, isotonic regression is applied for calibration.

The calibrated probability is interpreted as the system's confidence in answering the query.

---

# 4. Adaptive Gating

The calibrated probability is compared against two decision thresholds.

The system selects one of three actions:

### High Confidence

Generate an answer.

### Medium Confidence

Request additional evidence or retrieval refinement.

### Low Confidence

Abstain from answering.

This adaptive gating mechanism prevents unsupported generations.

---

# 5. Response Generation

For answerable queries, retrieved passages are combined with the user question to construct a Retrieval-Augmented Generation prompt.

The prompt is processed using **FLAN-T5-Large**, producing context-grounded responses.

---

# 6. Hallucination Risk Analysis

Generated responses are further analyzed using claim-level support verification.

The system estimates hallucination risk by combining:

- Semantic similarity
- Lexical overlap
- Context support
- Evidence consistency

This produces a final hallucination risk estimate for every generated response.

---

# Advantages

Compared to conventional RAG pipelines, the proposed framework provides:

- Adaptive decision making
- Improved factual grounding
- Lower hallucination rates
- Better calibration
- Safer response generation
- Reduced unsupported answers

---

# System Flow

Input Question

↓

Hybrid Retrieval

↓

Answerability Feature Extraction

↓

Random Forest Classifier

↓

Probability Calibration

↓

Adaptive Gating

↓

Answer Generation

↓

Hallucination Risk Analysis
