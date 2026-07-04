# TechQA-RAG-Eval

## Overview

TechQA-RAG-Eval is a benchmark dataset developed for evaluating Retrieval-Augmented Generation (RAG) systems on enterprise technical documentation.

The dataset contains technical documents, user questions, supporting evidence, and reference answers, enabling evaluation of both retrieval and generation quality.

---

## Purpose

Within this project, TechQA-RAG-Eval is used to evaluate:

- Hybrid Retrieval
- Answerability Prediction
- Context Selection
- Response Generation
- End-to-End RAG Performance

---

## Evaluation Tasks

The dataset supports evaluation of:

- Retrieval Recall@K
- Answerability Classification
- Generation Quality
- Decision Making
- System Reliability

---

## Dataset Characteristics

- Enterprise technical documents
- Question-answer pairs
- Ground-truth answers
- Supporting evidence
- Retrieval evaluation benchmark

---

## Usage in AURA-RAG

The dataset is used throughout the pipeline:

```
Documents
      │
      ▼
Hybrid Retrieval
      │
      ▼
Answerability Classification
      │
      ▼
Adaptive Gating
      │
      ▼
Grounded Response Generation
```

---

## Evaluation Metrics

Experiments on this dataset include:

- Recall@5
- ROC-AUC
- Decision Accuracy
- BERTScore
- ROUGE-L

---

## Official Source

Hugging Face

https://huggingface.co/datasets/nvidia/TechQA-RAG-Eval

---

## License

Please refer to the official dataset repository for licensing information.
