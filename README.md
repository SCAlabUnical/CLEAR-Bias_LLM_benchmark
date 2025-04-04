# Benchmarking Adversarial Robustness to Bias Elicitation in Large Language Models: Scalable Automated Assessment with LLM-as-a-Judge

## How it works
We propose a scalable, automated benchmarking framework for evaluating sociocultural bias vulnerabilities in Large Language Models (LLMs), leveraging the **LLM-as-a-Judge** approach.
- It introduces a two-step process:
  1. *Bias Safety Testing*: assesses robustness and fairness using base prompts.
  2. *Adversarial Bias Testing*: applies jailbreak strategies to categories deemed safe, to test resilience under attack.
- Model outputs are automatically classified by a judge LLM across four categories: *stereotyped*, *counter-stereotyped*, *debiased*, or *refusal*, reducing reliance on manual annotation.
- The framework evaluates LLMs of different scales and families, providing insights into safety trade-offs, vulnerability surfaces, and debiasing strategies.

- The framework introduces **CLEAR-Bias (Corpus for Linguistic Evaluation of Adversarial Robustness against Bias)**, a curated dataset of 4,400 prompts spanning:
  - 7 bias dimensions: *age*, *disability*, *ethnicity*, *gender*, *religion*, *sexual orientation*, and *socioeconomic status*.
  - 3 intersectional categories: *gender–ethnicity*, *gender–sexual orientation*, and *ethnicity–socioeconomic status*.
  - 2 task types: *Choose the option (CTO)* and *sentence completion (SC)*.
  - 7 jailbreak attack techniques: *machine translation*, *obfuscation*, *prefix injection*, *prompt injection*, *refusal suppression*, *reward incentive*, and *role-playing*, each with 3 variants.

- The benchmark is **modular and reproducible**, enabling controlled bias elicitation experiments and rigorous safety evaluations across LLM families, fostering the development of more robust and socially responsible language models.

## Key findings
- Bias robustness is not uniform: models are more resilient to some categories (e.g., religion) but more vulnerable to others (e.g., age).
- Larger models do not always guarantee higher safety; some small-scale models outperform larger ones in robustness and fairness.
- Jailbreak attacks remain effective against all tested models. Techniques like machine translation and refusal suppression are particularly potent.
- Medical domain LLMs tend to show lower bias safety, highlighting risks in domain-specific fine-tuning.

## How to cite
*Preprint coming soon.*

## Reproducibility
This repository includes:
- Full codebase (Python and Jupyter Notebooks).
- Scripts to replicate all evaluations, scoring, and adversarial tests.
- The **CLEAR-Bias** dataset is publicly available on [Huggingface](https://huggingface.co/datasets/RCantini/CLEAR-Bias)
