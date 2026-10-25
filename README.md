# Talk to Me in Your Language
### SemEval 2027 Shared Task: Cross-Lingual Alignment and Steering (CLaS)

[![Task Website](https://img.shields.io/badge/CLaS-SemEval--2027-blue)](https://clas-semeval2027.github.io/clas.semeval2027/task/)
[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/downloads/)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)

This repository contains the codebase and experiments for participating in the **CLaS shared task at SemEval 2027**. 

The goal of CLaS is to control a language model's output language **without fine-tuning**, relying exclusively on **inference-time interventions** (e.g., activation steering, representation engineering, parameter interventions, or sparse autoencoders).

---

## Task Overview

Submissions are evaluated automatically on a private test set via reproducible code.

### Required Models
- [`meta-llama/Llama-3.1-8B-Instruct`](https://huggingface.co/meta-llama/Llama-3.1-8B-Instruct)
- [`CohereLabs/tiny-aya-global`](https://huggingface.co/CohereLabs/tiny-aya-global)
*(Additional models are optional).*

### Datasets & Benchmarks
- **FLORES-200 devtest subsets**: Used for identifying language-specific components, steering vectors, or probe data.
- **CLaS-Bench**: Benchmark used for validation and cross-lingual alignment evaluation.
- **Baseline**: A prompt-based steering baseline is provided by the organizers.

---
## Shared Task Tracks

| Track | Name | Source Languages | Target Languages |
| :--- | :--- | :--- | :--- |
| **T1** | **High-Resource Steering** | 10 high-resource (`ar`, `de`, `en`, `es`, `fr`, `ja`, `zh`, `ru`, `hi`, `ko`) | Same 10 high-resource |
| **T2** | **Low-Resource Steering** | 10 high-resource (from T1) | 10 low-resource (`cs`, `el`, `fa`, `vi`, `uk`, `mt`, `no`, `sw`, `th`, `tr`) | 


## Getting Started

### 1. Prerequisites & Environment Setup

Clone the repository and set up a Python virtual environment:

```bash
git clone https://github.com/Trier-CLaS-SemEval-2027/Talk-to-me-in-your-language.git
cd Talk-to-me-in-your-language

# Create and activate virtual environment
python3 -m venv .venv
source .venv/bin/activate

# Install dependencies 
# pip install -r requirements.txt
```

### 2. Environment Variables

Copy `.env.example` to `.env` and fill in your credentials (e.g. Hugging Face token for Llama 3.1):

```bash
cp .env.example .env
```
