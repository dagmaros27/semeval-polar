# Detecting Online Polarization (SemEval-2026 Task 9)

This repository contains the system developed by the **Dagmaros** team for [SemEval-2026 Task 9: Detecting Multilingual, Multicultural, and Multievent Online Polarization](https://polar-semeval.github.io/).

Our work specifically investigates the performance gap between high-resource and low-resource African linguistic settings, focusing on **English, Swahili, and Amharic**.

## 📖 Introduction

**Online polarization**: the sharp division of opinions into opposing groups is a growing global concern. This project implements a system to detect and classify such polarization across diverse cultural contexts.

The core of our approach is a comparative analysis of domain-adaptive architectures. We demonstrate that while **Afro-XLMR** is essential for capturing the specific linguistic and cultural nuances of African languages, **Twitter-RoBERTa** provides surprisingly strong cross-lingual transfer for identifying specific polarization types.

### 🏆 Competition Results

Our system achieved the following average F1-scores on the official leaderboard:

* **Subtask 1 (Detection):** 0.78
* **Subtask 2 (Type Classification):** 0.54
* **Subtask 3 (Manifestation):** 0.53

---

## 🚀 Methodology
## Methodology

1. **Exploratory Data Analysis (EDA)**
   Conducted an initial analysis to understand label distributions, identifying significant class imbalance that informed our loss function strategy.

2. **Pipeline Construction**
   Developed a preprocessing pipeline that cleans text and applies **Instruction Augmentation**, prepending task-specific prompts to every input to guide the model's focus.

3. **Model Experimentation**
   Benchmarked various pre-trained Transformer encoders (including DeBERTa and Afro-XLMR) to identify the most effective backbones for English and African languages.

4. **Final Architecture & Optimization**
   Selected the top-performing models and fine-tuned them using a custom classification head with **Weighted Cross-Entropy Loss** to handle class imbalance effectively.

5. **Competitive Performance**
   The final instruction-tuned models achieved competitive results on the competition leaderboard.

> **Note:** A full breakdown of the methodology, ablation studies, and detailed performance benchmarks for all tested encoders can be found in the [Links](#🔗-links) linked at the end of this document.

---

## 📂 Repository Structure

* `data/`: Contains descriptions and samples of the data used.
* `notebooks/`: Jupyter notebooks for EDA, preprocessing, training, and evaluation.
* `figures/`: Visualizations of data distribution, model performance, and comparative analysis.
* `results/`: Detailed logs, prediction files, and F1-score breakdowns for the three subtasks.

---

## 🔗 Links

* **Report Paper:** [Read our System Description Paper here](https://drive.google.com/file/d/1EFIWaQhQYHeCI5vTopqkea8rICbtHZ4P/view?usp=sharing)
* **Competition Website:** [SemEval-2026 Task 9 - POLAR](https://polar-semeval.github.io/)
* **Leaderboard:** [Codabench Competition](https://www.codabench.org/competitions/10522/)
