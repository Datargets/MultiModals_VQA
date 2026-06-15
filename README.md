# Optimizing Multimodal Models for Medical Visual Question Answering

## A Comparative Study of LoRA and AdaLoRA on VQA-RAD and SLAKE-VQA

This repository contains the implementation and experimental framework for the paper:

**“Optimizing Multimodal Models for Medical Visual Question Answering: A Comparative Study of LoRA and AdaLoRA on VQA-RAD and SLAKE-VQA.”**

The study focuses on improving the efficiency and performance of large multimodal vision-language models for **Medical Visual Question Answering (Med-VQA)** using parameter-efficient fine-tuning strategies.

---

## Overview

Medical Visual Question Answering enables AI systems to interpret medical images and answer clinically relevant questions. This capability can support diagnostic reasoning, improve clinical decision-making, and assist healthcare professionals, particularly in resource-limited clinical environments.

However, fine-tuning large multimodal models for medical tasks is computationally expensive and often impractical. To address this challenge, this study evaluates **Parameter-Efficient Fine-Tuning (PEFT)** methods, specifically **Low-Rank Adaptation (LoRA)** and **Adaptive Low-Rank Adaptation (AdaLoRA)**, on multiple state-of-the-art multimodal models.

---

## Evaluated Models

The following multimodal models are evaluated in this study:

* **Idefics3-8B-Llama3**
* **Idefics2-8B**
* **LLaVA-1.5-7B**
* **Qwen2-VL-7B-Instruct**
* **Llama-3.2-11B-Vision-Instruct**

These models are fine-tuned and compared on medical VQA benchmarks using LoRA and AdaLoRA.

---

## Datasets

The experiments are conducted on two widely used Medical VQA datasets:

### VQA-RAD

VQA-RAD is a radiology-focused visual question answering dataset containing medical images paired with clinical questions and answers.

### SLAKE-VQA

SLAKE-VQA is a medical visual question answering dataset designed to evaluate multimodal understanding and clinical reasoning across different types of medical images and structured question-answer pairs.

---

## Methodology

The study follows a comparative experimental pipeline:

1. Preprocess medical image-question-answer pairs from VQA-RAD and SLAKE-VQA.
2. Fine-tune selected multimodal models using LoRA and AdaLoRA.
3. Evaluate model performance on Med-VQA tasks.
4. Compare accuracy across different models, datasets, and PEFT strategies.
5. Analyze the trade-off between computational efficiency and predictive performance.

---

## Key Innovation

The key contribution of this work is the application and comparison of **LoRA** and **AdaLoRA** for optimizing large multimodal models in Medical Visual Question Answering.

LoRA reduces the number of trainable parameters by injecting low-rank adaptation matrices into selected layers. AdaLoRA extends this idea by adaptively allocating rank during training, allowing the model to focus learning capacity on more important parameters.

This makes large multimodal models more practical for medical AI applications by reducing computational cost while maintaining strong performance.

---

## Main Results

The results show that AdaLoRA generally provides stronger performance than standard LoRA in the evaluated Med-VQA setting.

On the **VQA-RAD** dataset, **Idefics3-8B-Llama3** achieved:

| Dataset   | Model              | Fine-Tuning Method | Accuracy |
| --------- | ------------------ | -----------------: | -------: |
| VQA-RAD   | Idefics3-8B-Llama3 |            AdaLoRA |  **90%** |
| VQA-RAD   | Idefics3-8B-Llama3 |               LoRA |  **86%** |

These results suggest that adaptive rank allocation can improve Med-VQA performance while preserving the efficiency benefits of parameter-efficient fine-tuning.

---

## Contributions

* Comparative study of LoRA and AdaLoRA for Medical Visual Question Answering.
* Evaluation of multiple state-of-the-art multimodal models.
* Experiments on two benchmark datasets: VQA-RAD and SLAKE-VQA.
* Demonstration of efficient fine-tuning for large medical vision-language models.
* Analysis of performance and computational efficiency for clinical AI deployment.

---

## Research Significance

This work contributes to the development of efficient and accurate medical multimodal AI systems. By reducing the computational requirements of model adaptation, LoRA and AdaLoRA make large vision-language models more feasible for real-world medical applications, especially in environments with limited computational resources.

---

## Citation

If you use this repository or find this work helpful, please cite our paper:

```bibtex
  title   = {Optimizing multimodal models for medical visual question answering: A comparative study of LoRA and AdaLoRA on VQA-RAD and SLAKE-VQA},
  journal = {Computers in Biology and Medicine},
  volume  = {200},
  pages   = {111397},
  year    = {2026},
  doi     = {10.1016/j.compbiomed.2025.111397}
}
```

---

## Paper Information

**Title:** Optimizing Multimodal Models for Medical Visual Question Answering: A Comparative Study of LoRA and AdaLoRA on VQA-RAD and SLAKE-VQA
**Task:** Medical Visual Question Answering
**Datasets:** VQA-RAD, SLAKE-VQA
**Fine-Tuning Methods:** LoRA, AdaLoRA
**Models:** Idefics3-8B-Llama3, Idefics2-8B, LLaVA-1.5-7B, Qwen2-VL-7B-Instruct, Llama-3.2-11B-Vision-Instruct
**Status:** Published

---

## Keywords

Medical Visual Question Answering, Med-VQA, Multimodal Learning, Vision-Language Models, LoRA, AdaLoRA, PEFT, VQA-RAD, SLAKE-VQA, Medical AI, Clinical Decision Support
