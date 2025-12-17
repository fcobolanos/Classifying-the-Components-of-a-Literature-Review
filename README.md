# Classifying the Components of a Literature Review
This repository contains the official code, datasets, and experimental results for the paper: "Modelling and Classifying the Components of a Literature Review."

The project introduces the Sci-Sentence benchmark, a multidisciplinary dataset designed to identify the rhetorical roles of sentences in scientific literature reviews using Large Language Models (LLMs) based on Zero-Shot Learning(ZSL) and Finetuning.

## 📖 **Overview**
Writing a literature review is a cornerstone of scientific research, yet identifying the specific functional roles of sentences (e.g., identifying a research gap vs. describing a result) remains a challenge for automated systems. This project provides:

A novel 7-class annotation schema for literature review components.

The Sci-Sentence Benchmark (700 manually annotated + 2,240 augmented sentences).

Benchmarking scripts for Zero-shot and Fine-tuned LLMs.


## 📊 **The Sci-Sentence Benchmark**
The dataset classifies sentences into seven distinct rhetorical categories:
<img width="741" height="363" alt="Screenshot 2025-12-17 at 15 40 42" src="https://github.com/user-attachments/assets/c52e5aa3-76a6-45dd-90ca-20958246b120" />

Accesible [here](./datasets)

## 🤖 LLM-Based Data Augmentation
A significant challenge in scientific NLP is the scarcity of labeled data. To address class imbalance and increase the robustness of our classifiers, we implemented a Semi-Synthetic Data Augmentation pipeline:

1. Seed Selection: We started with the 560 sentences from the training and validation sets.
2. Prompt Engineering: We utilized Sonnet 3.0 to generate synthetic variations of minority classes (e.g., Extension or Limitation).
3. Quality Control: Synthetic sentences were filtered for linguistic coherence to ensure they maintained the technical tone of actual literature reviews.
4. Final Dataset: The resulting Sci-Sentence Augmented dataset contains 2,240 sentences, significantly improving the F1-scores of encoder fine-tuned models.


## 💻 Code Information
This section provides an overview of the technical implementation and the logic behind the classification pipeline.

Architecture: The project utilizes a pipeline that includes text preprocessing (tokenization, lemmatization), feature engineering, and classification.

Model Implementation: Detailed implementation of various machine learning models (e.g., SVM, Random Forest) and Deep Learning approaches (e.g., BERT-based transformers) used to categorize rhetorical moves.

Feature Engineering: Includes scripts for calculating TF-IDF vectors, word embeddings, and sentence-level features that capture the structural nuances of academic writing.

Evaluation Metrics: Scripts designed to generate confusion matrices, F1-scores, and precision-recall curves to validate model performance against the Sci-Sentence benchmark.

## 🚀 Usage Instructions

1. Prerequisites
Python 3.9 or higher

An OpenAI API Key (for GPT-based experiments) or HuggingFace access (for open source LLMs).

2. Data Input
Place any new literature review text files in the data/raw/ directory. The scripts are configured to output the classified sentences into the data/processed/ folder.

## 📝 Citation

If you use this code, the **Sci-Sentence** benchmark, or the findings from this project in your research, please cite the following paper:

Bolaños, F., Salatino, A., Osborne, F., & Motta, E. (2025). Modelling and Classifying the Components of a Literature Review. *arXiv preprint arXiv:2508.04337*. [https://doi.org/10.48550/arXiv.2508.04337](https://doi.org/10.48550/arXiv.2508.04337)

## ⚖️ License & Open Access

This project is fully **open-source** and **free to use** for both academic research and commercial applications. 

- **Code:** Licensed under the [MIT License](LICENSE). You are free to copy, modify, and distribute the code without restriction.
- **Datasets (Sci-Sentence):** Licensed under [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/). You are free to share and adapt the data as long as you provide appropriate credit (see [Citation](#citation)).

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

