# Fine-Tuning a Large Language Model with PEFT

## Project Overview
This project involves fine-tuning a pre-trained large language model (LLM) using **Parameter Efficient Fine-Tuning (PEFT)** techniques, particularly **LoRA (Low-Rank Adaptation)**. The focus is on leveraging a minimal GPU resource environment, such as a T4 GPU on Google Colab, to fine-tune a model and deploy it with a user-friendly interface.

The main goals of this project include:
- Fine-tuning an open-source LLM using a dataset of instructions.
- Creating a scalable and interactive user interface (UI) with **Gradio**.
- Disscusing improvements in performance through model-centric and data-centric approaches.

### Dataset and Model
- Utilized the **FineTome Instruction Dataset**, hosted on Hugging Face.
- Fine-tuned **Llama-3 (1B and 3B parameters)** using LoRA to reduce memory and computational costs.

### Fine-Tuning Process
- Trained the LLM on Google Colab, periodically saving checkpoints to prevent data loss during session resets.
- Stored fine-tuned models on Hugging Face.

### User Interface
- Developed a **Gradio**-based application to allow users to interact with the fine-tuned model.
- Hosted the UI on **Hugging Face Spaces**, providing a serverless deployment platform.

## Scalability and Performance Improvements

### Model-Centric Approach:

A model-centric approach focuses on optimizing how the model is trained and fine-tuned. Tweaking hyperparameters like the learning rate, batch size, or the number of training steps we can make training more efficient and improve the model’s ability to recognize patterns. For instance, finding the right learning rate ensures the model learns steadily without missing important updates or getting stuck. Techniques like Low-Rank Adaptation (LoRA) can also speed things up, reducing memory use and training time while still boosting the model’s performance by focusing updates on specific parts of the model.

Other optimizations, like mixed-precision training, use lower precision numbers during calculations to save memory and time without significantly impacting accuracy. After training, compressing the model with techniques like quantization (using smaller numerical values) or pruning (removing less useful components) makes the model faster and more resource-efficient, which is especially helpful for running it on devices with limited computational power. Regularization methods, such as dropout, where some connections in the model are temporarily ignored during training prevent overfitting. This ensuring the model performs well on new, unseen data instead of just memorizing the training examples.

### Data-Centric Approach:

Improving the dataset is a key factor in enhancing the performance and generalization of a fine-tuned large language model. While the provided FineTome dataset is a strong starting point, exploring and integrating additional data sources can make the model more versatile and robust. By exposing the model to more diverse and high-quality examples, it can better handle a wider variety of instructions and edge cases.

New data sources can include datasets from platforms like Hugging Face, which hosts a wide range of open-source datasets tailored for different tasks. For example, instruction-tuning datasets such as Dolly 15k provide a good variety of prompts and outputs that align with the task of improving instruction-following. Adding such a dataset ensures that the model sees diverse phrasing, styles, and content, reducing overfitting to the structure or format of the original FineTome dataset. Domain-specific datasets are another valuable source of improvement. For instance, if the model is intended for specialized tasks like legal or medical document generation, incorporating datasets from those domains ensures it learns the appropriate terminology and context. Examples might include PubMedQA for medical questions or LegalBench for legal documents. This targeted data helps the model perform better in niche applications, making it more valuable for specific user groups.

## Deliverables
[Hugging Face](https://huggingface.co/spaces/gretaj/lora_model)
