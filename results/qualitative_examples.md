# Qualitative Examples

This section presents representative examples illustrating how the adaptive gating framework behaves under different answerability conditions.

---

# Example 1 — High Answerability

## User Question

> What is the memory bandwidth of the NVIDIA H200 Tensor Core GPU?

### Retrieved Evidence

The hybrid retrieval module retrieves highly relevant documentation describing the GPU specifications.

### Gate Decision

✅ **Answer**

### Generated Response

The generator produces a grounded response supported by the retrieved evidence.

### Expected Behaviour

- High retrieval confidence
- High answerability probability
- Low hallucination risk

---

# Example 2 — Partial Evidence

## User Question

> Explain the hardware limitations of GPU X under mixed precision workloads.

### Retrieved Evidence

Relevant passages are retrieved, but important supporting information is missing.

### Gate Decision

🔍 **Request More Evidence**

### Expected Behaviour

The adaptive gate recommends additional retrieval instead of producing a potentially unsupported answer.

---

# Example 3 — Unanswerable Query

## User Question

> What security architecture will NVIDIA GPUs use in the next unreleased generation?

### Retrieved Evidence

No supporting evidence exists within the retrieved context.

### Gate Decision

🛑 **Abstain**

### System Response

> Insufficient evidence is available to answer this question with confidence.

### Expected Behaviour

The adaptive gate blocks generation, preventing hallucinated content.

---

# Summary

These examples illustrate the three possible outcomes of the proposed adaptive gating framework:

- ✅ Generate Answer
- 🔍 Request More Evidence
- 🛑 Abstain

The framework prioritizes factual reliability over always producing an answer.
