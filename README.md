# Probing Positional Bias and Orientation Effects in MLLMs

This repository contains the dataset and evaluation code for investigating the vulnerabilities of Multimodal Large Language Models (MLLMs) when processing abstract visual representations. Specifically, it provides the resources to reproduce the findings regarding the "capability floor," positional biases in multi-image prompts, and the effects of geometric transformations.

## Repository Structure

The repository is organized into the following main directories:

### 1. `Image/`
Contains the complete visual dataset used in the benchmark, divided into three sub-collections:
* **`Main_Corpus/`**: The core dataset of ~3,500 abstract, stylized images (e.g., Caricatures, Visual Puns, Symbolism) spanning four knowledge domains.
* **`Probe_I/`**: Multi-image prompt configurations (batch sizes $k=1$ to $k=6$) used to evaluate positional and attention-allocation biases.
* **`Probe_II/`**: Geometrically transformed image variants (incorporating a 2x4 rotation-mirror factorial design) used to test spatial robustness and reading-direction priors.

### 2. `Code/`
Contains the Jupyter notebooks required to execute the preprocessing, inference, and analysis pipelines.
* **`1 Visual Pun Detection.ipynb`**: The core MLLM inference engine. Automates batch querying across various APIs (e.g., Gemini, GPT, Claude) and categorizes images by domain and style.
* **`2 Data Analysis.ipynb`**: Aggregates the raw JSON inference data, utilizes LLM-as-a-judge scoring, and generates the statistical visualizations (dumbbells, heatmaps) presented in the study.
* **`3 Distribution of the attention.ipynb`**: Handles the geometric image perturbations, executes inference on the flipped/rotated datasets, and merges the results to quantify orientation effects.

### 3. `Labels/`
Contains the ground-truth annotations required for the LLM-as-a-judge evaluation.
* **`labels.json`**: The canonical reference file containing the acceptable answers for each Image ID in the main corpus.

## Getting Started

1.  **Clone the Repository:** Download the repository to your local machine.
2.  **Extract Datasets:** Ensure all multipart `.zip` files (particularly within the `Image/Probe_II/` directory) are extracted correctly into their respective folders.
3.  **Environment Setup:** The code requires a standard scientific Python environment (e.g., `pandas`, `numpy`, `matplotlib`) and API access to the respective MLLMs (e.g., `openai`, `google-genai`).

## Reference

*Citation details have been temporarily redacted to comply with double-blind peer review guidelines. The full citation and BibTeX will be updated upon the paper's acceptance.*
