# Classifying the Components of a Literature Review
This repository contains the official code, datasets, and experimental results for the paper: "Modelling and Classifying the Components of a Literature Review."

The project introduces the Sci-Sentence benchmark, a multidisciplinary dataset designed to identify the rhetorical roles of sentences in scientific literature reviews using Large Language Models (LLMs) based on Zero-Shot Learning(ZSL) and Finetuning.

## 📖 **Overview**
Writing a literature review is a cornerstone of scientific research, yet identifying the specific functional roles of sentences (e.g., identifying a research gap vs. describing a result) remains a challenge for automated systems. This project provides:

A novel 7-class annotation schema for literature review components.

The Sci-Sentence Benchmark (700 manually annotated + 2,240 augmented sentences).

Benchmarking scripts for Zero-shot and Fine-tuned LLMs.


##📊 **The Sci-Sentence Benchmark**
The dataset classifies sentences into seven distinct rhetorical categories:

##🚀 **Getting Started**
Prerequisites
Python 3.9 or higher

An OpenAI API Key (for GPT-based experiments) or HuggingFace access (for open source LLMs).

##📝 Citation
@article{bolanos2025modelling,
  title={Modelling and Classifying the Components of a Literature Review},
  author={Bolaños, Francisco and Salatino, Angelo and Osborne, Francesco and Motta, Enrico},
  journal={arXiv preprint arXiv:2508.04337},
  year={2025}
}

