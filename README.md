# Qwen + LoRA Image Generation Pipeline

## Project Overview

This project explores controllable AI image generation using modern diffusion models, LoRA adapters, and ComfyUI workflows. The goal was to investigate how Low-Rank Adaptation (LoRA) modules can be combined with large multimodal image generation models to produce customized, high-quality synthetic images while maintaining efficient inference and experimentation.

The workflow leverages Qwen image generation models together with LoRA adapters inside ComfyUI's node-based interface, enabling rapid experimentation with prompts, styles, concepts, and generation settings.

---

## Objectives

- Explore diffusion-based image generation
- Understand and apply LoRA adaptation techniques
- Build reproducible image generation workflows
- Experiment with prompt engineering
- Evaluate the effect of different LoRA adapters on generated outputs
- Gain practical experience with modern open-source generative AI tools

---

## Technical Background

### Diffusion Models

Modern image generation models create images by gradually removing noise from a random latent representation. Through iterative denoising, the model learns to generate realistic and coherent images from text prompts.

### LoRA (Low-Rank Adaptation)

LoRA is a parameter-efficient fine-tuning technique that allows specialized knowledge or styles to be added to a base model without retraining the entire network.

Advantages:

- Lower memory requirements
- Faster experimentation
- Easy swapping between styles and concepts
- Modular deployment

### ComfyUI

ComfyUI provides a node-based workflow environment for diffusion models.

Benefits include:

- Visual workflow design
- Reproducibility
- Easy model integration
- Flexible experimentation pipelines

---

## System Architecture

Text Prompt
↓
Qwen Image Model
↓
LoRA Adapter(s)
↓
Diffusion Sampling Pipeline
↓
Generated Image

The workflow allows different LoRAs, prompts, and generation parameters to be combined and evaluated efficiently.

---

## Technology Stack

| Component | Purpose |
|------------|------------|
| Python | Backend environment |
| ComfyUI | Workflow orchestration |
| Qwen Models | Image generation backbone |
| LoRA | Efficient model adaptation |
| CUDA | GPU acceleration |
| Git/GitHub | Version control |

---

## Experimental Environment

### Hardware

Experiments were conducted on an HPC (High Performance Computing) cluster equipped with NVIDIA H100 GPUs.

Reasons for HPC usage:

- Faster image generation
- Larger model support
- Parallel experimentation
- Higher throughput during testing

### Software Environment

- Linux
- Python 3.10+
- CUDA-enabled GPUs
- ComfyUI
- Qwen Image Models
- LoRA Adapters

---

## Installation

### Step 1: Install ComfyUI

Clone and install ComfyUI:

```bash
git clone https://github.com/comfyanonymous/ComfyUI.git
cd ComfyUI
pip install -r requirements.txt
```

Official repository:

https://github.com/comfyanonymous/ComfyUI

---

### Step 2: Download Models

Download the required Qwen image generation models and place them inside:

```text
ComfyUI/models/checkpoints/
```

---

### Step 3: Download LoRAs

Place LoRA files inside:

```text
ComfyUI/models/loras/
```

---

### Step 4: Clone This Repository

```bash
git clone <your-repository-url>
cd <repository-name>
```

---

### Step 5: Load Workflow

Start ComfyUI:

```bash
python main.py
```

Open the provided workflow JSON file from this repository and verify that all required models are detected correctly.

---

## Running the Workflow

1. Launch ComfyUI
2. Load workflow JSON
3. Select Qwen checkpoint
4. Select LoRA adapter(s)
5. Configure prompt
6. Configure generation parameters
7. Execute workflow
8. Review generated outputs

---

## Example Workflow

Prompt
↓
Load Qwen Model
↓
Load LoRA
↓
Sampler
↓
Decoder
↓
Save Image

---

## Repository Structure

```text
.
├── workflows/
│   ├── workflow.json
│
├── outputs/
│   ├── generated_images/
│
├── assets/
│   ├── examples/
│
├── docs/
│   ├── screenshots/
│
└── README.md
```

---

## Learning Outcomes

Through this project:

- Gained practical experience with diffusion models
- Learned how LoRA adapters modify model behavior
- Built reproducible ComfyUI workflows
- Worked with GPU-based AI workloads on HPC infrastructure
- Explored prompt engineering techniques
- Evaluated controllable image generation pipelines

---

## Future Improvements

Potential extensions include:

- Training custom LoRAs
- Automated prompt optimization
- Benchmarking multiple diffusion backbones
- Multi-LoRA composition experiments
- Quantitative image quality evaluation
- Integration with additional multimodal models

---

## Disclaimer

This repository focuses on experimentation and workflow development. Users are responsible for obtaining any required models, LoRA adapters, and datasets in accordance with their respective licenses.

---

## Author

Samyak Jain

RWTH Aachen University

Focus Areas:
- Artificial Intelligence
- Computer Vision
- Generative AI
- Robotics
- Autonomous Systems