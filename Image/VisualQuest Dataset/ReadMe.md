# VisualQuest Dataset

The VisualQuest dataset is a benchmark designed to rigorously evaluate multimodal large language models (MLLMs) on abstract visual reasoning tasks. It tests reasoning capabilities that require the integration of symbolic, cultural, and linguistic knowledge. Unlike existing benchmarks focused on realistic image classification or direct captioning, this corpus comprises 3,551 non-photographic, stylized images.

---

## Dataset Composition

The dataset is organized into four major categories, each emphasizing a distinct type of background knowledge:

* **Public Figures (1,024 images):** Includes authors, actors, scientists, and other notable personalities.
* **Popular Culture (690 images):** Features films, television shows, anime, video games, and iconic cities.
* **Linguistic Expressions (954 images):** Represents idioms, proverbs, and phrases.
* **Literary Works (883 images):** Depicts novels, fairy tales, fictional characters, and deities.

To abstract the visual information and move beyond simple object recognition, the images are rendered using ten distinct non-realistic presentation methods: 
* Caricature (959)
* Illustration (829)
* Visual Pun (692)
* Emoji Combination (655)
* Minimalism (149)
* Symbolism (128)
* Memoji (89)
* Cartoon (45)
* Surrealism (4)
* Iconography (1)

---

## Data Structure

Each image in the dataset is stored in a dictionary-like structure, utilizing the `Image ID` as the primary key. 

* **Image ID**: A unique string key ranging from "0000" to "3551".
* **Ground Truth**: Contains one or more valid, correct answers for the image (e.g., "Bruce Lee; Li Xiaolong").
* **Category**: The semantic knowledge domain of the image.
* **Question**: A specific, concise query paired with the image to guide the model.
* **Presentation Method**: The artistic rendering style of the image.
* **Recognition Vector**: A binary array recording the baseline recognition results from 10 contemporary MLLMs.
* **Recognition Count**: An integer from 0 to 10 indicating the total number of baseline MLLMs that successfully recognized the image.

---

## Reference

If you utilize this dataset in your research, please cite the following paper:

> Xiao K, Yang L, Tulajiang P, et al. VisualQuest: A Benchmark for Abstract Visual Reasoning in MLLMs[C]//Chinese Conference on Pattern Recognition and Computer Vision (PRCV). Singapore: Springer Nature Singapore, 2025: 414-428.
