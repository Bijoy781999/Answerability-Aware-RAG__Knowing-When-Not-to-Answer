# Dataset Download Links

This repository does **not** include the benchmark datasets used in the experiments.

Please download them from the official sources listed below.

---

# 1. TechQA-RAG-Eval

**Description**

Enterprise technical question-answering benchmark for evaluating Retrieval-Augmented Generation systems.

**Official Source**

https://huggingface.co/datasets/nvidia/TechQA-RAG-Eval

---

# 2. RAGTruth

**Description**

Benchmark dataset for hallucination detection and evaluation in Retrieval-Augmented Generation systems.

**Official Source**

https://github.com/ParticleMedia/RAGTruth

---

# Download Instructions

After downloading the datasets, organize them as follows:

```
data/
├── TechQA-RAG-Eval/
│   ├── documents
│   ├── train
│   ├── validation
│   └── test
│
└── RAGTruth/
    ├── annotations
    ├── responses
    └── metadata
```

> **Note:** The exact folder names and file structure may vary depending on the version obtained from the official sources. Refer to the documentation provided by each dataset for the latest organization.

---

# Why Are the Datasets Not Included?

The datasets are excluded from this repository because:

- They are publicly available from their original publishers.
- Redistribution may be restricted by their respective licenses.
- Including them would significantly increase the repository size.

---

# Citation

If you use these datasets in research or derivative work, please cite the original dataset authors according to their official citation guidelines.
