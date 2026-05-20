# LLM Safety Prompt Robustness Evaluation (LLaMA2-7B)

This repository contains a controlled experiment to evaluate the **safety robustness** of **LLaMA2-7B** across different prompt types and transformations.

Instead of simply measuring refusal vs. compliance, this project analyzes how the model's behavior changes under various linguistic framings — including direct prompts, contextual high-risk scenarios, and adversarial/perturbed rephrasings.

---

## 🎯 Key Objective

To understand how **LLaMA2-7B**'s safety boundaries shift when prompts are:

- **Direct (Base)** prompts
- **Tier-2 Contextual** high-risk prompts
- **Perturbed / Rephrased** prompts

The goal is to study the **sensitivity of LLM safety mechanisms** to prompt framing, intent masking, and contextual manipulation.

---

## 📁 Repository Structure

```bash
ILINA_LLM_SAFETY/
├── prompts/
│   ├── base_prompts.json           # Standard baseline prompts
│   ├── perturbed_prompts.json      # Reworded / softened / adversarial variations
│   └── tier2_contextual_prompts.json # Higher-risk contextual prompts
│
├── results/
│   └── responses.csv               # All model responses + metadata
│
└── src/
    ├── run_exp.py                  # Main experiment runner
    ├── ollama_client.py            # Ollama API client for LLaMA2-7B
    ├── analyze_res.py              # Analysis and evaluation utilities
    └── utils/                      # Helper modules (loading, processing, etc.)
```
## 🔄 Workflow

Load prompt datasets from the prompts/ directory
Send prompts to LLaMA2-7B via Ollama
Collect and log detailed responses into results/responses.csv
Analyze response patterns across prompt categories


## 🔍 What This Project Explores

Sensitivity of LLM safety mechanisms to prompt framing
Differences in behavior between base, contextual, and perturbed prompts
How rewording and intent masking affect compliance/refusal rates
Early insights into prompt robustness in open-source LLMs


## 📊 Output
All experiment results are saved in:

results/responses.csv — Contains prompts, responses, categories, and metadata for downstream analysis.


## ⚠️ Notes

This project is intended for research and safety evaluation purposes only.

It aims to better understand model behavior under controlled conditions.

It is not designed to bypass or weaken safety alignments.

## 🚀 Getting Started
```bash
# Clone the repository
https://github.com/Jimmymugendi/AI-Safety-Prompt-Robustness-Evaluation-Framework.git
cd AI-Safety-Prompt-Robustness-Evaluation-Framework

```
