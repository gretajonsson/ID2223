# Fine-Tuning a Large Language Model with PEFT

## Project Overview
This project involves fine-tuning a pre-trained large language model (LLM) using **Parameter Efficient Fine-Tuning (PEFT)** techniques, particularly **LoRA (Low-Rank Adaptation)**. The focus is on leveraging a minimal GPU resource environment, such as a T4 GPU on Google Colab, to fine-tune a model and deploy it with a user-friendly interface.

The main goals of this project include:
- Fine-tuning an open-source LLM using a dataset of instructions.
- Creating a scalable and interactive user interface (UI) with **Gradio**.
- Disscusing improvements in performance through model-centric and data-centric approaches.

---



### Dataset and Model
- Utilized the **FineTome Instruction Dataset**, hosted on Hugging Face.
- Fine-tuned **Llama-3 (1B and 3B parameters)** using LoRA to reduce memory and computational costs.

### Fine-Tuning Process
- Trained the LLM on Google Colab, periodically saving checkpoints to prevent data loss during session resets.
- Stored fine-tuned models on Hugging Face.

### User Interface
- Developed a **Gradio**-based application to allow users to interact with the fine-tuned model.
- Hosted the UI on **Hugging Face Spaces**, providing a serverless deployment platform.

### Scalability and Performance Improvements
#### Model-Centric Approach:

#### Data-Centric Approach:

---

## Deliverables
[Hugging Face](https://huggingface.co/spaces/gretaj/lora_model)
