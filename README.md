# AGILMM

In order to deepen our comprehension of multimodal information, we have pioneered advancements in both model architecture and training methodologies, culminating in the development of AGILMM.

## Model Architecture

[![model architecture](/assets/img/model.png)]

Concerning the model architecture, we incorporated a combination of VIT (Vision Transformer), an adapter module, and LLM (Language and Vision Model) and We continued training the LLM model with a more extensive corpus. For the adapter component, we employed the Perceiver Resampler to effectively extract and compress visual features. The specific parameters for VIT and LLM are listed in the following table.

| Model        | Vision  |  Language  |
| :--------  | :-----  | :----:  |
| AGILMM | ViT-B/16|Bloom-7B|

Our training strategy consists of a three-stage process, which encompasses the following steps:

1. Image-Text Alignment Pretraining: We conducted alignment pretraining on an extensive dataset of image-text pairs, thereby establishing a correlation between the image encoder and the language LLM.
2. Multitask Pretraining: By rigorously training the model on a diverse array of visual tasks, we facilitated the learning of a broad spectrum of visual features and semantic knowledge.
3. Multimodal Instruction Fine-tuning: Utilizing our curated dataset, which comprises tasks related to Image-based text generation and  comprehension task , we fine-tuned the model to enhance its understanding of multimodal instructions, thereby further augmenting its performance.

By adhering to this three-stage training methodology, our AGILMM model has demonstrated exceptional performance on the MME leaderboard.