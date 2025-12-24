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

Our pipeline follows a unified fine-tuning framework:

1. **Exploratory Data Analysis (EDA):** Deep dive into the multilingual dataset to identify class imbalances and linguistic patterns.
2. **Instruction Augmentation:** Enhancing model inputs with specific instructions to improve context awareness.
3. **Weighted Loss Functions:** Implementing custom loss strategies to mitigate the effects of imbalanced data across the 22 available languages.
4. **Model Comparison:** Evaluating `Afro-XLMR` vs. `Twitter-RoBERTa` for multilingual polarization tasks.

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
