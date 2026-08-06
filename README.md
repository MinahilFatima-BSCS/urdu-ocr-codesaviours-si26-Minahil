# Urdu OCR — Printed Urdu Text Extraction Using Tesseract OCR

Built during the Code Saviours ML/AI Internship (SI-26)

---

# Project Overview

Urdu OCR is an OCR-based project that extracts printed Urdu text from images using **Tesseract OCR with Urdu language support**.

The project uses image preprocessing techniques with OpenCV and Tesseract OCR to convert Urdu image content into editable digital text.

Unlike English OCR, Urdu text recognition presents unique challenges due to connected characters, different letter shapes, varying fonts, and complex ligatures.

---

# Why This Project Matters

Optical Character Recognition (OCR) converts text from images into editable digital text. While OCR performs well for English, Urdu remains a difficult language because of:

* Connected cursive writing
* Multiple letter shapes
* Similar-looking characters
* Different writing styles
* Low-quality scanned documents

This project aims to improve Urdu text extraction using OCR techniques with Urdu language support.

### Real-world Applications

* Digitizing historical Urdu books
* Newspaper digitization
* Government document processing
* Educational resources
* Library archives
* Digital record management

---

# How It Works

This project uses **Tesseract OCR** with Urdu language support for printed Urdu text recognition.

The workflow is:

1. Upload an Urdu image
2. Image is loaded using OpenCV
3. Image is converted into grayscale format
4. Preprocessed image is passed to Tesseract OCR
5. Tesseract recognizes Urdu text
6. Extracted text is displayed in the Streamlit interface

The OCR pipeline uses the Urdu language model (`urd`) to improve printed Urdu text recognition.

---

# Technologies Used

* Python
* OpenCV
* Tesseract OCR
* pytesseract
* Streamlit
* Google Colab
* GitHub
* Pillow

---

# Live Demo

### Streamlit Application

https://m59vvf3kggcbxpiqrjyguz.streamlit.app/

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
streamlit run app.py
```

After running the application, Streamlit will generate a local URL where you can upload an Urdu image and receive the extracted text.

---

# Dataset Details

The dataset contains **180 printed Urdu images** collected from different real-world sources.

### Sources

* Kaggle Urdu OCR Dataset
* Jang Newspaper
* Dawn Newspaper
* Urdu Books
* Urdu Signboards
* Synthetic Urdu Images

### Dataset Variety

The dataset includes:

* Different Urdu fonts
* Multiple font sizes
* Newspaper articles
* Printed book pages
* Signboards
* Clean and noisy images
* Simple and complex layouts

This diversity helps evaluate OCR performance across different printed Urdu documents.

---

# OCR Implementation

### OCR Engine

```
Tesseract OCR
```

### Urdu Language Support

Tesseract Urdu language model:

```
urd
```

### Image Processing

The image preprocessing workflow includes:

* Reading image using OpenCV
* Converting image to grayscale
* Improving image readability
* Extracting Urdu text using pytesseract

Example:

```python
text = pytesseract.image_to_string(
    gray,
    lang="urd",
    config="--psm 6"
)
```

---

# Results

The Urdu OCR system successfully extracts printed Urdu text from multiple test images through the Streamlit application.

The system performs well on clear printed Urdu documents. However, recognition accuracy depends on:

* Image quality
* Font style
* Text layout
* Noise level

Although the project achieved promising results, further improvements can be achieved using advanced preprocessing techniques and deep learning-based OCR models.

Future improvements include:

* Larger Urdu dataset
* Better image preprocessing
* Character Error Rate (CER) evaluation
* Word Error Rate (WER) evaluation
* Handwritten Urdu OCR support

---

# Gap Analysis

## Baseline: Traditional OCR Challenges

During testing, OCR performance was affected by:

* Incorrect character recognition
* Missing characters
* Complex Urdu layouts
* Font variations
* Low-quality images

Some images produced incomplete or incorrect OCR output.

These results show that Urdu OCR remains challenging due to the complexity of Urdu script.

---

# Why Urdu OCR is Challenging

Urdu text recognition is difficult because:

* Characters are connected
* Same letters have different shapes
* Fonts vary significantly
* Printed quality affects recognition

Improving preprocessing and using specialized OCR models can enhance recognition accuracy.

---

# Application Interface

The Streamlit web application allows users to:

* Upload a printed Urdu image
* Process the image
* Extract Urdu text
* Display the recognized output instantly

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
└── assets/
```

---

# Requirements

```
opencv-python
pytesseract
streamlit
Pillow
```

---

# Future Improvements

* Increase dataset size
* Improve preprocessing
* Evaluate using CER and WER
* Use deep learning-based OCR models
* Support handwritten Urdu
* Improve recognition for noisy images
* Deploy optimized inference

---

# Credits

**Minahil Fatima**

Built during the **Code Saviours ML/AI Internship — Batch SI-26.**

Special thanks to Code Saviours for providing guidance and practical experience in Machine Learning and OCR development.
