
# VisualQuest: Full Image Corpus

This root directory contains the complete image repository for the **VisualQuest** benchmark, originally introduced by Xiao et al. (2025). The corpus is designed to evaluate abstract visual reasoning in Multimodal Large Language Models (MLLMs) through highly stylized, non-photographic imagery. 

To facilitate both the main benchmark evaluation and the specific capability probes described in the original study, the image files are organized into three distinct sub-directories.

---

## Directory Structure

### 1. `Main_Corpus/` (Core Benchmark Dataset)
This folder contains the foundational dataset of over 3,500 abstract images. The images span four knowledge domains (Public Figures, Popular Culture, Linguistic Expressions, and Literary Works) and are rendered in ten distinct visual styles (e.g., Caricature, Minimalism, Visual Pun). These images serve as the baseline for evaluating standard MLLM recognition and reasoning.

### 2. `Probe_I/` (Positional Bias Samples)
This folder contains the multi-image prompt configurations used to test attention allocation and positional bias. The images are organized by batch size ($k=1$ through $k=6$). This subset is used to determine if models exhibit primacy or recency biases when processing multiple abstract images in a single inference prompt.

### 3. `Probe_II/` (Orientation & Geometric Robustness)
This folder contains the geometrically transformed variants of the core images. It utilizes a 2x4 factorial design (horizontal mirroring crossed with standard, 90° left, 90° right, and inverted rotations). These files are used to test whether MLLM reasoning degrades under spatial disorientation or exhibits human-like reading-direction biases.

---

## Usage Notes

* **Image Formats:** All images are provided in standard `.jpg` or `.png` formats.
* **ID Mapping:** The filenames in these directories correspond directly to the `Image ID` keys used in the accompanying `labels.json` and inference tracking files.
* **Extraction:** For the Probe II data, ensure all multipart ZIP archives are downloaded into the same directory before extracting.

---

