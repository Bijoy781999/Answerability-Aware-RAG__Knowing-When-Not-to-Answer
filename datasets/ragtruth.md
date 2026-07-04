# RAGTruth

## Overview

RAGTruth is a benchmark dataset designed for evaluating hallucinations in Retrieval-Augmented Generation (RAG) systems.

Unlike traditional question-answering datasets, RAGTruth provides fine-grained hallucination annotations, making it suitable for evaluating factual reliability and unsupported generation.

---

## Purpose

In this project, RAGTruth is used to evaluate:

- Hallucination Detection
- Hallucination Risk Prediction
- Claim-Level Support Analysis
- Response Reliability
- Safety Evaluation

---

## Hallucination Categories

The dataset contains several hallucination categories, including:

- No Hallucination
- Evidence Conflict
- Evidence Baseless Information
- Subtle Conflict
- Subtle Baseless Information

These labels enable detailed analysis of hallucination behaviour beyond simple correct/incorrect evaluation.

---

## Usage in AURA-RAG

The dataset is used after response generation.

```
Generated Response
        │
        ▼
Claim-Level Analysis
        │
        ▼
Hallucination Risk Estimation
        │
        ▼
Safety Evaluation
```

---

## Evaluation Performed

Experiments include:

- Hallucination Label Distribution
- Hallucination Rate
- Predicted Hallucination Risk
- Risk Separation
- Hallucination Category Analysis

---

## Official Source

GitHub

https://github.com/ParticleMedia/RAGTruth

---

## License

Please refer to the official repository for licensing information.
