# ViT-Llama-Latex-code-generator-
# ViT-Llama LaTeX Code Generator

A Vision-Language AI project that leverages **Qwen2-VL**, **Unsloth**, and **Hugging Face Transformers** for image-to-LaTeX generation.

The model is designed to understand visual mathematical expressions, formulas, and structured content from images and generate corresponding LaTeX code.

---

## Features

- Vision-Language Model (VLM) based architecture
- Uses Qwen2-VL-7B-Instruct in 4-bit quantization
- Efficient fine-tuning with Unsloth
- Memory-optimized training using BitsAndBytes
- Supports GPU acceleration
- Designed for mathematical OCR and LaTeX generation tasks
- Compatible with Google Colab and local GPU environments

---

## Tech Stack

- Python
- PyTorch
- Hugging Face Transformers
- Unsloth
- Qwen2-VL
- PEFT (LoRA)
- TRL
- BitsAndBytes
- Datasets

---

## Installation

### Clone Repository

```bash
git clone https://github.com/<your-username>/ViT-Llama-Latex-code-generator.git
cd ViT-Llama-Latex-code-generator
```

### Install Dependencies

```bash
pip install transformers torch pillow datasets

pip install --no-deps unsloth

pip install bitsandbytes accelerate peft trl triton cut_cross_entropy

pip install sentencepiece protobuf datasets huggingface_hub hf_transfer

pip install unsloth_zoo
```

---

## Model

The project utilizes:

```python
unsloth/Qwen2-VL-7B-Instruct-bnb-4bit
```

Features:

- 4-bit Quantization
- Reduced VRAM Usage
- Faster Training
- Faster Inference

---

## Loading the Model

```python
from unsloth import FastVisionModel

model, tokenizer = FastVisionModel.from_pretrained(
    "unsloth/Qwen2-VL-7B-Instruct-bnb-4bit",
    load_in_4bit=True,
    use_gradient_checkpointing="unsloth",
    device_map="auto",
)
```

---

## Project Workflow

1. Install dependencies
2. Load Qwen2-VL model
3. Prepare image-text dataset
4. Fine-tune using Unsloth
5. Generate LaTeX code from input images
6. Evaluate generated outputs

---

## Dataset

The project is designed for datasets containing:

- Mathematical equation images
- Formula screenshots
- Handwritten equations
- Printed mathematical expressions

Example format:

```json
{
  "image": "equation.png",
  "latex": "\\frac{a+b}{c}"
}
```

---

## Hardware Requirements

Recommended:

| Component | Requirement |
|------------|-------------|
| GPU | NVIDIA T4 / L4 / A100 |
| VRAM | 12GB+ |
| RAM | 16GB+ |
| Python | 3.10+ |

---

## Applications

- Mathematical OCR
- Equation Recognition
- Educational AI Systems
- Research Paper Digitization
- Formula-to-LaTeX Conversion
- Scientific Document Processing

---

## Future Improvements

- Support handwritten mathematical expressions
- Multi-language scientific notation
- Web deployment with Gradio
- Real-time formula recognition
- Larger Vision-Language Models

---

## Author

**Suraj Mishra**

Mathematics & Computing Student

Aspiring Data Scientist | AI/ML Enthusiast | Computer Vision Researcher

---

## License

This project is intended for educational and research purposes.
