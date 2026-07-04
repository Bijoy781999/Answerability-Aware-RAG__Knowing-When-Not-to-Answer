# Datasets

This project evaluates the proposed **Answerability-Aware Retrieval-Augmented Generation (AURA-RAG)** framework using two publicly available benchmark datasets designed for retrieval-augmented generation and hallucination analysis.

> **Note**
> Due to licensing restrictions and repository size limitations, the datasets are **not included** in this repository. Please download them from their official sources.

---

# 1. TechQA-RAG-Eval

## Overview

TechQA-RAG-Eval is an enterprise-oriented benchmark developed for evaluating Retrieval-Augmented Generation systems on technical documentation.

It contains:

- Technical documents
- User questions
- Ground-truth answers
- Retrieved evidence

The dataset is used to evaluate:

- Retrieval quality
- Answerability prediction
- Response generation
- End-to-end RAG performance

---

## Usage in this Project

TechQA-RAG-Eval is used for:

- Hybrid Retrieval (BM25 + Dense Retrieval)
- Answerability Classification
- Retrieval Recall@K evaluation
- End-to-End Decision Evaluation
- BERTScore
- ROUGE-L
- LLM-as-a-Judge Evaluation

---

## Official Dataset

https://huggingface.co/datasets/nvidia/TechQA-RAG-Eval

---

# 2. RAGTruth

## Overview

RAGTruth is a benchmark specifically designed for hallucination detection in Retrieval-Augmented Generation systems.

Unlike traditional QA datasets, RAGTruth provides fine-grained hallucination annotations, allowing researchers to distinguish between:

- No Hallucination
- Evidence Conflict
- Evidence Baseless Information
- Subtle Conflict
- Subtle Baseless Information

---

## Usage in this Project

The dataset is used for:

- Hallucination Risk Estimation
- Claim-Level Support Analysis
- Hallucination Label Analysis
- Safety Evaluation
- Risk Prediction

---

## Official Dataset

https://github.com/ParticleMedia/RAGTruth

---

# Dataset Preparation

The preprocessing pipeline consists of:

1. Document Cleaning
2. Text Normalization
3. Chunking (360-word chunks)
4. BM25 Index Construction
5. Dense Embedding Generation
6. Hybrid Retrieval Indexing

---

# Directory Structure

```
datasets/

README.md
techqa_rag_eval.md
ragtruth.md
dataset_download_links.md
```

---

# Citation

Please cite the original dataset authors when using these datasets in academic work.
