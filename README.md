# Urdu OCR — A Fine-Tuned TrOCR Model for Extracting Printed Urdu Text

Built during the Code Saviours ML/AI Internship (SI-26)

---

# Project Overview

Urdu OCR is a deep learning project that extracts printed Urdu text from images using Microsoft's TrOCR (Transformer-based Optical Character Recognition) model. The model has been fine-tuned on a custom Urdu dataset collected from multiple real-world sources.

Unlike traditional OCR systems, this project focuses specifically on Urdu, a cursive language that presents unique recognition challenges due to connected characters, varying fonts, and complex ligatures.

---

# Why This Project Matters

Optical Character Recognition (OCR) converts text from images into editable digital text. While OCR performs well for English, Urdu remains a difficult language because of:

- Connected cursive writing
- Multiple letter shapes
- Similar-looking characters
- Different writing styles
- Low-quality scanned documents

This project aims to improve Urdu text recognition using a Transformer-based OCR model.

### Real-world Applications

- Digitizing historical Urdu books
- Newspaper digitization
- Government document processing
- Educational resources
- Library archives
- Digital record management

---

# How It Works

This project uses **Microsoft TrOCR (Transformer OCR)**, a Vision Transformer (ViT) based OCR model.

Instead of recognizing characters one by one like traditional OCR systems, TrOCR learns visual patterns directly from images and generates complete text using a Transformer decoder.

### Fine-Tuning

The original **microsoft/trocr-base-printed** model was fine-tuned using a custom Urdu dataset consisting of printed Urdu images collected from multiple sources.

The workflow is:

1. Upload an Urdu image
2. Image is preprocessed
3. TrOCR extracts image features
4. Transformer decoder predicts Urdu text
5. Extracted text is displayed in the Gradio interface

This allows the model to recognize Urdu text more effectively than general-purpose OCR systems such as Tesseract.

---

# Technologies Used

- Python
- PyTorch
- Hugging Face Transformers
- Microsoft TrOCR
- Google Colab
- Gradio
- GitHub
- Hugging Face Spaces
- Pillow

---

# Live Demo

### Hugging Face Space

https://huggingface.co/spaces/Minahil-BSCS/urdu-ocr-codesaviours-si26-Minahil

### GitHub Repository

https://github.com/MinahilFatima-BSCS/urdu-ocr-codesaviours-si26-Minahil

---

# How to Run Locally

### Clone the Repository

```bash
git clone https://github.com/MinahilFatima-BSCS/urdu-ocr-codesaviours-si26-Minahil.git
```

### Move into the Project Folder

```bash
cd urdu-ocr-codesaviours-si26-Minahil
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Run the Application

```bash
python app.py
```

After running the application, Gradio will generate a local URL where you can upload an Urdu image and receive the extracted text.

---

# Dataset Details

The dataset contains **180 printed Urdu images** collected from different real-world sources.

### Sources

- Kaggle Urdu OCR Dataset
- Jang Newspaper
- Dawn Newspaper
- Urdu Books
- Urdu Signboards
- Synthetic Urdu Images

### Dataset Variety

The dataset includes:

- Different Urdu fonts
- Multiple font sizes
- Newspaper articles
- Printed book pages
- Signboards
- Clean and noisy images
- Simple and complex layouts

This diversity helps improve the model's ability to generalize across different printed Urdu documents.

---

# Model Training

### Base Model

```
microsoft/trocr-base-printed
```

### Training Configuration

| Parameter | Value |
|-----------|-------|
| Epochs | 3 |
| Framework | PyTorch |
| Model | TrOCR |
| Platform | Google Colab |

### Training Loss

| Epoch | Average Loss |
|--------|--------------|
| 1 | 1.7064 |
| 2 | 0.4783 |
| 3 | 0.4818 |

The training loss decreased significantly after the first epoch, indicating that the model successfully learned Urdu text patterns during fine-tuning.

---

# Results

The fine-tuned TrOCR model successfully extracts printed Urdu text from many test images through the Gradio application.

Compared with the baseline Tesseract OCR, the fine-tuned model produces noticeably better recognition on printed Urdu text.

Although the project achieved promising qualitative results, there is still room for improvement. With a larger dataset, more training epochs, and additional preprocessing techniques, the recognition accuracy can be further improved.

Future improvements include:

- Larger Urdu dataset
- More fine-tuning epochs
- Better image preprocessing
- Character Error Rate (CER) evaluation
- Word Error Rate (WER) evaluation
- Handwritten Urdu OCR support

---

# Gap Analysis

## Baseline: Tesseract OCR

During testing, Tesseract struggled to recognize Urdu text correctly.

Common issues included:

- Incorrect words
- Missing characters
- Blank outputs
- Poor handling of connected Urdu script
- Failure on complex layouts

Examples observed:

- "نجی" → "تجی"
- "طالبہ" → "طاليه"

Some images produced no OCR output at all.

These results demonstrate that traditional OCR engines are not well suited for Urdu.

---

# Why TrOCR Performs Better

TrOCR is a Transformer-based OCR model that learns contextual information rather than recognizing isolated characters.

Advantages include:

- Better handling of connected Urdu characters
- Improved recognition of complete words
- More robust to different fonts
- Better performance on printed Urdu documents

---

# Application Interface

The Gradio web application allows users to:

- Upload a printed Urdu image
- Process the image
- Extract Urdu text
- Display the recognized output instantly

*(Insert your application screenshot here.)*

---
<img width="1917" height="892" alt="App Working" src="https://github.com/user-attachments/assets/b6d72e03-610f-44e6-97c8-0c1b7ee6b96d" />

# Project Structure

```
urdu-ocr-codesaviours-si26-Minahil
│
├── app.py
├── requirements.txt
├── README.md
├── data/
├── notebooks/
├── model/
└── assets/
```

---

# Requirements

```
transformers==4.35.0
torch==2.0.1
gradio==3.50.0
Pillow==10.0.0
```

---

# Future Improvements

- Increase dataset size
- Improve preprocessing
- Evaluate using CER and WER
- Fine-tune for more epochs
- Support handwritten Urdu
- Improve recognition for noisy images
- Deploy optimized inference

---

# Credits

**Minahil Fatima**

Built during the **Code Saviours ML/AI Internship — Batch SI-26.**

Special thanks to Code Saviours for providing guidance and practical experience in Machine Learning and OCR development.
