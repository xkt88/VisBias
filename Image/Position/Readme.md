
# Probe I: Positional Bias and Multi-Image Prompting Samples

This repository folder contains the image datasets and multi-image prompt structures used in Probe I of the abstract visual reasoning benchmark. This subset is designed to evaluate "positional bias" in Multimodal Large Language Models (MLLMs)—specifically, how a model's reasoning accuracy changes when multiple images are batched into a single inference prompt.

## Experimental Design

The dataset tests models by grouping images into sets (batch sizes $k=1$ to $k=6$). The core objective is to determine if attention is uniformly distributed across all images in a prompt, or if MLLMs exhibit a "primacy gradient" (favoring the first image) or "recency bias" (favoring the last image).

## Directory Structure

The folder is organized by the batch size ($k$) used during inference:

* **`batch_k1/`**: Single-image baseline samples.
* **`batch_k2/`**: Samples where 2 images are evaluated in a single prompt.
* **`batch_k3/`**: Samples where 3 images are evaluated in a single prompt.
* **`batch_k4/`**: Samples where 4 images are evaluated in a single prompt.
* **`batch_k5/`**: Samples where 5 images are evaluated in a single prompt.
* **`batch_k6/`**: Samples where 6 images are evaluated in a single prompt.

*Note: The images provided in these folders are representative examples of the batched configurations used to probe the MLLMs' attention allocation capabilities.*

