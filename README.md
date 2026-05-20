LLM Safety Prompt Robustness Evaluation (LLaMA2-7B)

This repository contains a controlled experiment designed to evaluate how the LLaMA2-7B model responds to different classes of prompts under a safety-aware testing setup. The focus is on understanding how prompt framing influences model behavior, particularly in scenarios involving sensitive or potentially unsafe requests.

Rather than only measuring whether a model refuses or complies, this project examines how robustness changes across prompt transformations, including contextual shifts and adversarial rephrasing.

Key Objective

To analyze how LLaMA2-7B behavior varies across:

Direct (base) prompts
Contextual high-risk prompts (Tier-2)
Rephrased / perturbed prompts

The goal is to study how safety boundaries shift depending on linguistic framing and intent masking.

Repository Structure
ILINA_LLM_SAFETY/
│
├── prompts/                          # Prompt datasets used in experiments
│   ├── base_prompts.json             # Standard baseline prompts
│   ├── perturbed_prompts.json        # Reworded / softened variations
│   └── tier2_contextual_prompts.json # Higher-risk contextual prompts
│
├── results/                          # Model outputs
│   └── responses.csv                 # Logged responses from experiments
│
└── src/                              # Core experiment pipeline
    ├── analyze_res.py               # Response analysis utilities
    ├── ollama_client.py             # Interface for LLaMA2 via Ollama
    ├── run_exp.py                   # Main experiment runner
    └── utils/                      # Helper modules (prompt loading, preprocessing)
  Workflow Overview
Load structured prompt sets from prompts/
Send prompts to LLaMA2-7B via Ollama API
Collect and log responses into structured CSV format
Analyze response behavior across different prompt categories
What This Project Helps Explore
Sensitivity of LLM safety mechanisms to prompt framing
Differences in response behavior between base vs contextual prompts
How rewording or perturbation affects model compliance/refusal patterns
Early-stage insights into prompt robustness in open-source LLMs
Output

All model responses are stored in:

results/responses.csv

This file forms the basis for downstream analysis and safety evaluation.

Notes

This project is intended for research and evaluation purposes only. It focuses on understanding model behavior under controlled conditions and does not aim to bypass or weaken model safety systems.
