
# Probe II: Geometric Robustness and Orientation Samples

This repository folder contains the geometrically transformed image datasets utilized in Probe II of the abstract visual reasoning benchmark[cite: 8]. The data is specifically structured to evaluate whether Multimodal Large Language Models (MLLMs) degrade uniformly under spatial transformations or if they inherit human-like reading-direction priors from their training data[cite: 8].

## Experimental Design

To dissociate visual and textual disorientation, the dataset employs a 2x4 factorial design[cite: 8]. Each original image from the core benchmark is subjected to horizontal mirroring crossed with four rotation states (identity, 90° left, 90° right, and inverted)[cite: 8]. This yields a total of 8 variants per image, spanning the full orientation-chirality cross-product[cite: 8].

## Directory Structure

The folder contains split ZIP archives and extracted directories corresponding to the transformation suite:

### Extracted Transformation Directories
*   **`left/`**, **`right/`**, **`Inverted/`**: Images subjected to pure rotation (90° left, 90° right, and 180° inversion)[cite: 8].
*   **`flip/`**: Images subjected to horizontal mirroring without rotation[cite: 8].
*   **`flip_left/`**, **`flip_right/`**, **`flip_Inverted/`**: Images subjected to both horizontal mirroring and rotation[cite: 8].

### Compressed Archives
*   **`Orientation samples.zip.001`** to **`Orientation samples.zip.010`**: Multi-part ZIP archive files containing the complete geometric transformation dataset. Ensure all parts are downloaded into the same directory before extracting.

