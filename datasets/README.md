# Datasets

This directory provides information about the benchmark datasets used to evaluate the **Answerability-Aware Retrieval-Augmented Generation (AURA-RAG)** framework.

> **Note**
>
> Due to licensing restrictions and repository size limitations, the datasets are **not included** in this repository. Please download them from their official sources before reproducing the experiments.

---

## Datasets Used

The project is evaluated using two publicly available benchmark datasets:

| Dataset | Purpose |
|----------|---------|
| TechQA-RAG-Eval | Retrieval-Augmented Generation evaluation |
| RAGTruth | Hallucination detection and analysis |

---

## Directory Structure

```
datasets/
│
├── README.md
├── dataset_download_links.md
├── ragtruth.md
└── techqa_rag_eval.md
```

---

## Why These Datasets?

These datasets complement each other by evaluating different aspects of Retrieval-Augmented Generation systems.

### TechQA-RAG-Eval

Used for evaluating:

- Hybrid Retrieval
- Answerability Classification
- Response Generation
- End-to-End RAG Performance

---

### RAGTruth

Used for evaluating:

- Hallucination Detection
- Hallucination Risk Prediction
- Claim-Level Support Analysis
- Safety Evaluation

---

## Dataset Preparation

The preprocessing pipeline includes:

1. Document Cleaning
2. Text Normalization
3. Text Chunking
4. BM25 Index Construction
5. Dense Embedding Generation
6. Hybrid Retrieval Indexing

---

## Download

Please refer to [**dataset_download_links.md**](dataset_download_links.md) for official download links.

---

## Citation

If you use these datasets in academic work, please cite the original dataset authors.
