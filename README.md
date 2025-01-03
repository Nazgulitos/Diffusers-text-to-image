# PMLDL Assignment 3: Diffusion - Text-to-Image Generation

## Author
**Nazgul Salikhova**  
Email: [n.salikhova@innopolis.university](mailto:n.salikhova@innopolis.university)  
Group: B22-AAI-02  

---

## 🎯 Goal
The goal of this project is to fine-tune a diffusion model using an emoji dataset to enable text-to-image generation of new emojis based on text prompts.

---

## 📂 Dataset
The dataset consists of emojis downloaded from [Kaggle Emoji Image Dataset](https://www.kaggle.com/datasets/subinium/emojiimage-dataset). A subset of 2,000 images (mainly Windows emojis) was used for training.

---

## 🚀 Key Features
- Fine-tuning a **Stable Diffusion model** for emoji generation.
- Emoji dataset preprocessing, including cropping and augmentation.
- Text-to-image generation using custom prompts.

---

## 🛠️ Libraries and Tools
- **Diffusion Models**: Stable Diffusion (`CompVis/stable-diffusion-v1-4`)
- **Frameworks**: PyTorch, HuggingFace Diffusers
- **Libraries**: `torchvision`, `datasets`, `bitsandbytes`
- **Optimizer**: 8-bit Adam optimizer for memory efficiency
- **Scheduler**: Cosine learning rate scheduler with warm-up steps

---

## 📋 Project Workflow
1. **Dataset Preparation**:
   - Download emoji images and annotations.
   - Preprocess using a custom PyTorch Dataset class.

2. **Model Setup**:
   - Load pretrained Stable Diffusion components.
   - Fine-tune UNet with emoji images.

3. **Training**:
   - Train the model over 20 epochs with batched gradient accumulation.

4. **Inference**:
   - Generate images based on custom text prompts.
   - Display results and save them to a specified folder.

---

## ⚙️ Configuration
- **Image Size**: 256x256
- **Batch Size**: 4
- **Epochs**: 20
- **Learning Rate**: 1e-4

---

## 🧪 Results
Example Prompts:
- "Angry Unicorn"
- "Dancing Lemon with Sunglasses"
- "Cat with a Top Hat"
- "Jealous Face"

Generated emoji images were evaluated visually for their alignment with the prompts.

---

## 📜 References
- [HuggingFace Diffusers](https://huggingface.co/docs/diffusers/index)
- [Kaggle Emoji Image Dataset](https://www.kaggle.com/datasets/subinium/emojiimage-dataset)