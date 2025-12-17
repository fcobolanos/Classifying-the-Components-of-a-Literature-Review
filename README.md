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


## 🚀 **Getting Started**
Prerequisites
Python 3.9 or higher

An OpenAI API Key (for GPT-based experiments) or HuggingFace access (for open source LLMs).

## 📝 Citation
@article{bolanos2025modelling,
  title={Modelling and Classifying the Components of a Literature Review},
  author={Bolaños, Francisco and Salatino, Angelo and Osborne, Francesco and Motta, Enrico},
  journal={arXiv preprint arXiv:2508.04337},
  year={2025}
}

## ⚖️ License
This project is licensed under the MIT License.

