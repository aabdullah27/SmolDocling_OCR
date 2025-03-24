# SmolDocling OCR Application

🚀 **SmolDocling OCR Application** is a Google Colab notebook that leverages the **SmolDocling-256M-preview** model for efficient **OCR and document conversion**. This lightweight model offers **fast and accurate** extraction of text, tables, code, formulas, and more—rivaling larger models like GPT-4 and Gemini while being significantly smaller (**256M parameters**).

## ✨ Features

- 📄 **DocTags Tokenization** – Efficient and structured document representation with **Docling** compatibility.
- 🔍 **OCR & Layout Preservation** – Extracts text while maintaining document structure and bounding boxes.
- 🖥️ **Code & Formula Recognition** – Converts **code blocks** (with indentation) and **math expressions** (to LaTeX).
- 📊 **Tables & Charts Processing** – Extracts structured data with **OTSL support**.
- 📑 **Figure Classification & Captions** – Links images with relevant captions.
- 📜 **Full-Page Processing** – Converts entire pages, including **text, code, equations, and figures**.
- ⚡ **Fast & Efficient** – Processes pages in **0.35 seconds on an A100 GPU**.

## 📌 Usage Guide

### 1️⃣ Setup & Authentication
Before running the notebook, set up authentication with **Hugging Face**:
```python
import os
os.environ["HF_TOKEN"] = "your_huggingface_token"
```

### 2️⃣ Upload Images
Use the upload interface to **drag and drop** single or multiple images for processing.

### 3️⃣ Select a Task
Choose from:
- Convert **pages** to Docling format
- Extract **tables** to OTSL
- Convert **formulas** to LaTeX
- Extract **charts** and **section headers**

### 4️⃣ Process the Images
Click **"Process Image(s)"** to run the model and extract the desired content.

### 5️⃣ View & Save Output
The results are displayed in **DocTags and Markdown formats**, with an option to **download**.

## ⚡ Model Overview

SmolDocling-256M-preview is a **multimodal Image-Text-to-Text model** for **document understanding**. Unlike traditional OCR models, it integrates advanced **layout analysis** and **content classification** while remaining **lightweight** compared to models like **GPT-4 (1.76T)** and **Gemini**.

### 📌 Technical Details:
- **Model:** `ds4sd/SmolDocling-256M-preview` (Hugging Face)
- **Developed by:** IBM Research, Docling Team
- **License:** Apache 2.0
- **Architecture:** Based on **Idefics3**, fine-tuned from **SmolVLM-256M-Instruct**
- **Frameworks Supported:** `Transformers`, `VLLM`, `ONNX`

## 🚀 Performance & Efficiency
- **Ultra-compact** at **256M parameters**, yet capable of **full-document conversion**.
- **Avg. 0.35s per page inference** on an **A100 GPU**.
- **Seamless Docling Integration** – Exports to **Markdown, HTML, JSON**.

## 📂 Repository Structure
```
├── SmolDocling_OCR.ipynb   # Google Colab notebook
├── README.md               # Documentation
├── examples/               # Sample input/output images (optional)
```

## 🛠️ Installation (For Local Use)

If you want to run this outside Colab, install the dependencies:
```bash
pip install torch transformers huggingface_hub docling-core
```

## 🌟 Acknowledgments
This project is powered by **SmolDocling**, a **Docling-compatible** model developed by IBM Research.

## 📜 License
This repository is licensed under the **Apache 2.0 License**.

---
💡 **Smol but mighty!** This notebook brings powerful document understanding to **lightweight AI models**, making **OCR and document conversion faster and more accessible**. 🚀
