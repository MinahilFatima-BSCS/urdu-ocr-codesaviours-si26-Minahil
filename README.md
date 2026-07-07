# Urdu OCR Project | Code Saviours SI-26 | Minahil Fatima

## Project Overview
This project aims to build an Optical Character Recognition (OCR) system that extracts text from printed Urdu document images.

## Objectives
- Collect and organize an Urdu OCR dataset.
- Fine-tune an OCR model.
- Deploy the model on Hugging Face Spaces.

## Technologies
- Python
- Google Colab
- Hugging Face
- GitHub


In this task, I learned that OCR is a technology used to convert text from images into editable digital text. I also understood that Urdu OCR is more challenging than English OCR because of its connected writing style, changing letter shapes, and similar-looking characters. Finally, I explored real-world applications of Urdu OCR, such as digitizing historical documents and converting printed documents into editable digital text, showing its importance in education, government, and business.
## Why We Need a Better Model

The baseline Tesseract OCR produced poor results on Urdu images. Although it recognized a few words correctly, many characters were incorrect or completely missing. Some images produced no output at all.

During testing:
- Several Urdu words were recognized incorrectly.
- Many characters were missing or replaced with incorrect ones.
- Some images produced completely blank OCR results.

Urdu is a cursive language with connected characters, complex ligatures, different fonts, and varying image quality. Because of these challenges, a general-purpose OCR engine like Tesseract is not accurate enough for Urdu text recognition.

This project aims to build a specialized Urdu OCR model that can recognize Urdu text with much higher accuracy than the baseline Tesseract OCR.
