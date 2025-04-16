# 🎨 Fine-Tuning Stable Diffusion with Custom Images

This repository contains all the code and configuration required to **fine-tune Stable Diffusion** using a small set of personal images. The goal is to train the model to generate custom outputs that resemble a specific person, object, or artistic style, depending on the images provided.

---

## 📌 Project Overview

Stable Diffusion is a powerful latent text-to-image diffusion model capable of generating photorealistic images from natural language prompts. By fine-tuning it on a custom dataset, we can teach the model to generate highly personalized content such as:

- AI-generated portraits of yourself
- Replications of a specific art style
- Custom-themed character generations

This repo supports basic fine-tuning and can be extended to use DreamBooth or LoRA for improved results on small datasets.

---

## 🧾 Features

- Fine-tune Stable Diffusion using your own images
- Generate outputs using natural language prompts
- Optionally integrate LoRA/DreamBooth for better memory and sample efficiency
- Simple setup using Jupyter notebook
- CUDA-compatible training for speed

---

## 📁 Project Structure

```
.
├── notebook441d321338.ipynb       # Jupyter notebook for fine-tuning and generation
├── images/                        # Your training images go here
├── output/                        # Folder to store generated images
├── model/                         # Stores fine-tuned model weights or checkpoints
├── requirements.txt               # Python dependencies
└── README.md                      # This file
```

---

## ⚙️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/stable-diffusion-finetune.git
cd stable-diffusion-finetune
```

### 2. Create and Activate a Virtual Environment

```bash
python -m venv venv
source venv/bin/activate      # On Windows: venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Download the Base Stable Diffusion Weights

You can download the official weights from [Hugging Face](https://huggingface.co/CompVis/stable-diffusion-v1-4) (requires an account and agreement to terms).

Place the weights in the `model/` directory.

---

## 🏃‍♂️ How to Fine-Tune

1. Place your custom images (e.g., portraits of yourself) inside the `images/` folder.
2. Open the `notebook441d321338.ipynb` in Jupyter Notebook.
3. Follow the steps to:
   - Preprocess images
   - Load base model
   - Fine-tune using your data
   - Save model checkpoints
4. After training, test image generation using prompts that include a custom token (e.g., `photo of sks person`).

---

## 🧪 Example Prompts

Try prompts like:

```
"A realistic photo of sks person in a cyberpunk city"
"A painting of sks person by Van Gogh"
"A photo of sks person wearing medieval armor"
```

> Replace `sks person` with your custom token used during fine-tuning.

---

## 🖼 Sample Outputs

| Prompt | Output |
|--------|--------|
| *A photo of sks person in a forest* | ![output1](output/sample1.png) |
| *A digital painting of sks person as a superhero* | ![output2](output/sample2.png) |

---

## 📦 Requirements

See [`requirements.txt`](requirements.txt), which includes:

- `torch`
- `transformers`
- `diffusers`
- `accelerate`
- `xformers` (optional)
- `bitsandbytes` (optional)
- `notebook`, `matplotlib`, `opencv-python`, and more

To install:
```bash
pip install -r requirements.txt
```

---

## 💡 Tips

- Use 10–30 images for best results. Keep backgrounds, lighting, and angles consistent.
- Training with LoRA or DreamBooth is highly recommended for fast and memory-efficient tuning.
- Run on a GPU with at least 12GB VRAM for optimal performance.

---

## 📄 License

This project is for educational and personal use only. The base Stable Diffusion model is licensed under the CreativeML Open RAIL-M license by Stability AI.

---

## 🙏 Acknowledgements

- [Stability AI](https://stability.ai/)
- [Hugging Face Diffusers](https://github.com/huggingface/diffusers)
- [DreamBooth](https://github.com/XavierXiao/Dreambooth-Stable-Diffusion)
- [CompVis Stable Diffusion](https://github.com/CompVis/stable-diffusion)

---

## ✨ Contact

Feel free to reach out or raise an issue for questions or collaboration!
