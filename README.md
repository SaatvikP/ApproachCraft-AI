# ApproachCraft-AI: Fine-Tuning Phi-2 for Research Problem Solving

This project was completed as part of **CMPSC 497 - Spring 2025** final project at Penn State University.

## 📚 Project Overview
The goal of this project was to fine-tune an open-source large language model (LLM) to generate high-quality suggested approaches for given research problems.  
We fine-tuned the **Phi-2** model using a custom dataset built from real-world research papers in the AI-in-Education domain.

---

## 🗂 Files in This Repository
- `ApproachCraft_AI_DataGen.ipynb`  
  → Script to build the dataset by scraping paper titles and abstracts from arXiv based on custom queries.

- `ApproachCraft_AI_FineTuning.ipynb`  
  → Script to fine-tune Microsoft's Phi-2 model using LoRA, and evaluate the fine-tuned model on a test set using ROUGE and Semantic Cosine Similarity.

- `ApproachCraft_Report.pdf`  
  → Final project report describing dataset construction, model details, training process, evaluation, results, and future work.

---

## 🛠️ Methods Used
- **Dataset**:  
  2,000 paper titles and abstracts scraped from arXiv related to AI in education.

- **Model**:  
  Fine-tuning **Phi-2** (Microsoft's Transformer LLM) using **Low-Rank Adaptation (LoRA)**.

- **Training Details**:
  - Batch size: 4
  - Gradient accumulation: 4
  - Epochs: 3
  - Learning rate: 2e-4
  - Mixed precision (fp16) training

- **Evaluation Metrics**:
  - ROUGE-1, ROUGE-2, ROUGE-L (for content overlap)
  - Semantic Cosine Similarity (for meaning similarity)

---

## 📈 Results
| Metric | Score |
|:-------|:------|
| ROUGE-1 F1 | 0.2779 |
| ROUGE-2 F1 | 0.0607 |
| ROUGE-L F1 | 0.2569 |
| Average Semantic Cosine Similarity | 0.7199 |

The fine-tuned model demonstrated strong semantic understanding of research prompts with reasonable content structure overlap.

