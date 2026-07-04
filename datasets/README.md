# Datasets

This directory contains documentation for the benchmark datasets used to develop and evaluate the **Answerability-Aware Retrieval-Augmented Generation (AURA-RAG)** framework.

> **Important**
>
> The datasets are **not included** in this repository due to licensing restrictions and repository size limitations. Please download them directly from their official sources.

---

## Datasets Used

| Dataset | Purpose |
|----------|---------|
| TechQA-RAG-Eval | Retrieval-Augmented Generation evaluation on technical documentation |
| RAGTruth | Hallucination detection and claim-level hallucination analysis |

---

## Dataset Documentation

This directory includes:

| File | Description |
|------|-------------|
| `techqa_rag_eval.md` | Overview and usage of the TechQA-RAG-Eval benchmark |
| `ragtruth.md` | Overview and usage of the RAGTruth benchmark |

---

## Why These Datasets?

The proposed framework requires evaluating multiple aspects of Retrieval-Augmented Generation systems, including:

- Hybrid retrieval effectiveness
- Answerability prediction
- Adaptive decision making
- Hallucination mitigation
- Response quality
- Probability calibration

No single benchmark covers all of these evaluation dimensions. Therefore, two complementary datasets are used.

---

## Dataset Download

### TechQA-RAG-Eval

https://huggingface.co/datasets/nvidia/TechQA-RAG-Eval

---

### RAGTruth

https://github.com/ParticleMedia/RAGTruth

---

## Citation

If you use these datasets in your own research, please cite the original dataset authors according to their official documentation.
