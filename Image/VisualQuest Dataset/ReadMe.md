
# VisualQuest Dataset

The VisualQuest dataset is a benchmark designed to rigorously evaluate multimodal large language models (MLLMs) on abstract visual reasoning tasks[cite: 7]. It tests reasoning capabilities that require the integration of symbolic, cultural, and linguistic knowledge[cite: 7]. Unlike existing benchmarks focused on realistic image classification or direct captioning, this corpus comprises 3,551 non-photographic, stylized images[cite: 7].

---

## Dataset Composition

The dataset is organized into four major categories, each emphasizing a distinct type of background knowledge[cite: 7]:

*   **Public Figures (1,024 images):** Includes authors, actors, scientists, and other notable personalities[cite: 7].
*   **Popular Culture (690 images):** Features films, television shows, anime, video games, and iconic cities[cite: 7].
*   **Linguistic Expressions (954 images):** Represents idioms, proverbs, and phrases[cite: 7].
*   **Literary Works (883 images):** Depicts novels, fairy tales, fictional characters, and deities[cite: 7].

To abstract the visual information and move beyond simple object recognition, the images are rendered using ten distinct non-realistic presentation methods[cite: 7]: 
*   Caricature (959)[cite: 7]
*   Illustration (829)[cite: 7]
*   Visual Pun (692)[cite: 7]
*   Emoji Combination (655)[cite: 7]
*   Minimalism (149)[cite: 7]
*   Symbolism (128)[cite: 7]
*   Memoji (89)[cite: 7]
*   Cartoon (45)[cite: 7]
*   Surrealism (4)[cite: 7]
*   Iconography (1)[cite: 7]

---

## Data Structure

Each image in the dataset is stored in a dictionary-like structure, utilizing the `Image ID` as the primary key[cite: 7]. 

*   **Image ID**: A unique string key ranging from "0000" to "3551"[cite: 7].
*   **Ground Truth**: Contains one or more valid, correct answers for the image (e.g., "Bruce Lee; Li Xiaolong")[cite: 7].
*   **Category**: The semantic knowledge domain of the image[cite: 7].
*   **Question**: A specific, concise query paired with the image to guide the model[cite: 7].
*   **Presentation Method**: The artistic rendering style of the image[cite: 7].
*   **Recognition Vector**: A binary array recording the baseline recognition results from 10 contemporary MLLMs[cite: 7].
*   **Recognition Count**: An integer from 0 to 10 indicating the total number of baseline MLLMs that successfully recognized the image[cite: 7].

---

## Reference

If you utilize this dataset in your research, please cite the following paper:

> Xiao K, Yang L, Tulajiang P, et al. VisualQuest: A Benchmark for Abstract Visual Reasoning in MLLMs[C]//Chinese Conference on Pattern Recognition and Computer Vision (PRCV). Singapore: Springer Nature Singapore, 2025: 414-428.
