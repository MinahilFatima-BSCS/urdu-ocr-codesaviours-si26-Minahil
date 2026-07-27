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
Gap Analysis
Image 58.png
Actual Text: لاہور: نجی یونیورسٹی کی طالبہ کی 'خود کشی' کی کوشش، دوسری منزل سے چھلانگ لگا دی۔ پولیس کے مطابق واقعہ بظاہر خودکشی کی کوشش لگتا ہے، طالبہ کی نازک فریکچر ہو گئیں جبکہ یونیورسٹی نے آن کیمپس کلاسز معطل کر دیں۔

Tesseract Output: ایور

لاہور: تجی یوٹیورسٹی کی طاليه کی 'خود کشی' کی کے مخابق ماقعہ بر خبدکامی کی

Issue:

"نجی" کو "تجی" پڑھا۔
"طالبہ" کو "طاليه" پڑھا۔
کئی الفاظ غلط recognize ہوئے۔
پورا متن مکمل recognize نہیں ہوا۔
آخری سطریں مکمل miss ہو گئیں.
Image 25.png
Actual Text: میں ہلاک ہونے والوں کی یاد میں اور ان کو

Tesseract Output: ھی اگ ہو وا ول کیا اوران

Issue:

زیادہ تر الفاظ غلط پہچانے گئے۔
الفاظ کی ترتیب بھی غلط ہوگئی۔
اصل جملہ صحیح طریقے سے recognize نہیں ہوا۔
Image 2.png
Actual Text: کی لوڈ شیڈنگ کے خلاف مظاہرہ کیا۔ پولیس تشدد سے ایک نوجوان

Tesseract Output: ا0 از
Issue:

تقریباً پورا متن recognize نہیں ہوا۔
صرف چند غیر متعلقہ حروف detect ہوئے۔
OCR اصل متن پڑھنے میں ناکام رہا۔
Image 64.png
Actual Text: عالیان ماں اپنے والدین کی اکلوتی اولاد تھی۔ اور اس کے والدین اس کی شادی سے پہلے وفات پا گئے۔ تو اس کی شادی کس نے کی اور ابلیشر کے ساتھ؟ ہمارے اور ان کے ماحول میں فرق ہے واحد۔

Tesseract Output: (No Output)

Issue:

OCR نے کوئی متن detect نہیں کیا۔
مکمل image پڑھنے میں ناکام رہا۔
Image 65.png
Actual Text: گی، ماموں صدر سے 4 دن ہسپتال رہے۔ امرحہ علی کی چھت سے گر کر ٹانگ کی ہڈی ٹوٹ گئی۔۔۔۔

Tesseract Output: (No Output)

Issue:

OCR نے کوئی متن detect نہیں کیا۔
مکمل image recognize نہیں ہوئی۔
Summary
Tesseract fails on Urdu because it struggles to recognize connected Urdu characters, different fonts, low-quality images, and complex layouts. It often produces incorrect words, misses many characters, or completely fails to detect text. Therefore, a dedicated Urdu OCR model is required for accurate Urdu text recognition.
## Why We Need a Better Model

The baseline Tesseract OCR produced poor results on Urdu images. Although it recognized a few words correctly, many characters were incorrect or completely missing. Some images produced no output at all.

During testing:
- Several Urdu words were recognized incorrectly.
- Many characters were missing or replaced with incorrect ones.
- Some images produced completely blank OCR results.

Urdu is a cursive language with connected characters, complex ligatures, different fonts, and varying image quality. Because of these challenges, a general-purpose OCR engine like Tesseract is not accurate enough for Urdu text recognition.

This project aims to build a specialized Urdu OCR model that can recognize Urdu text with much higher accuracy than the baseline Tesseract OCR.
URDU OCR
A fine-tuned TrOCR model for extracting printed Urdu text from images.
WHAT PROBLEM THIS SOLVES AND WHY IT MATTERS
Urdu OCR is a challenging problem because Urdu text has connected characters, complex letter shapes, different fonts, and a right-to-left writing direction. These challenges make it difficult for computers to accurately recognize Urdu text from images.
This project aims to automatically extract printed Urdu text from images. One real-world use case is digitizing Urdu newspapers, books, historical documents, and other printed material so that the content can become searchable, editable, and easier to preserve.
HOW IT WORKS
This project uses TrOCR, a Transformer-based Optical Character Recognition model designed to recognize text from images.
First, an image containing Urdu text is provided to the model. The model analyzes the visual patterns in the image and predicts the text that appears in it.
The original TrOCR model was fine-tuned for this project using a dataset of Urdu text images. Fine-tuning means taking an already trained model and training it further on a specialized dataset so that it can perform better on a specific task.
The dataset used in this project contains Urdu images from different categories, including newspapers, books, signboards, synthetic images, and other Urdu text sources. This helps the model learn from different image types, layouts, backgrounds, and text styles.
LIVE DEMO
The live Hugging Face Space demo will be added here after deployment.
HOW TO RUN IT LOCALLY
1. Clone the Repository
git clone YOUR_GITHUB_REPOSITORY_URL
cd YOUR_REPOSITORY_NAME
2. Install the Required Dependencies
pip install -r requirements.txt
3. Run the Application
python app.py
After running the application, open the local URL shown in the terminal.
DATASET DETAILS
The dataset contains approximately 180 Urdu text images.
The images were collected from different sources and categories, including:
Newspaper images
Book and document images
Signboard images
Synthetically generated Urdu text
Other Urdu text images
The dataset contains variety in:
Urdu fonts and text styles
Image sizes and resolutions
Backgrounds
Text layouts
Newspaper and document formats
Real-world signboards
Synthetic Urdu text images
The dataset was divided into training and testing subsets:
Total samples: 180
Training samples: 144
Testing samples: 36
The image paths and corresponding Urdu text labels were stored in a CSV file.
RESULTS
The model was fine-tuned on the Urdu OCR dataset during Week 4 of the project.
The final Week 4 accuracy was limited. The initial results were affected by the Urdu tokenizer vocabulary, as the original tokenizer did not properly contain the required Urdu characters. This caused incorrect predictions and, in some cases, repeated or meaningless characters.
To improve the model, Urdu characters, Urdu digits, and relevant punctuation were added to the tokenizer vocabulary before retraining.
The model still requires further improvement. With more time and resources, performance could be improved by:
Collecting a larger Urdu dataset
Adding more Urdu fonts and writing styles
Increasing the number of training images
Training for more epochs
Applying better image preprocessing
Using data augmentation
Performing additional hyperparameter tuning
Improving the tokenizer and Urdu vocabulary
CREDIT
Minahil Fatima
Built during the Code Saviours ML/AI Internship — Batch SI-26.
