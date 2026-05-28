
# Probe II: Geometric Robustness and Orientation Samples

This repository folder contains the geometrically transformed image datasets utilized in Probe II of the abstract visual reasoning benchmark. The data is specifically structured to evaluate whether Multimodal Large Language Models (MLLMs) degrade uniformly under spatial transformations or if they inherit human-like reading-direction priors from their training data.

## Experimental Design

To dissociate visual and textual disorientation, the dataset employs a 2x4 factorial design. Each original image from the core benchmark is subjected to horizontal mirroring crossed with four rotation states (identity, 90° left, 90° right, and inverted). This yields a total of 8 variants per image, spanning the full orientation-chirality cross-product.

## Directory Structure

The folder contains split ZIP archives and extracted directories corresponding to the transformation suite:

### Extracted Transformation Directories
*   **`left/`**, **`right/`**, **`Inverted/`**: Images subjected to pure rotation (90° left, 90° right, and 180° inversion).
*   **`flip/`**: Images subjected to horizontal mirroring without rotation.
*   **`flip_left/`**, **`flip_right/`**, **`flip_Inverted/`**: Images subjected to both horizontal mirroring and rotation.

### Compressed Archives
*   **`Orientation samples.zip.001`** to **`Orientation samples.zip.010`**: Multi-part ZIP archive files containing the complete geometric transformation dataset. Ensure all parts are downloaded into the same directory before extracting.

