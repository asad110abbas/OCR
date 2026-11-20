# 👁️ BRIHA · Multi-Engine OCR Text Extraction

![Part of BRIHA](https://img.shields.io/badge/Part_of-BRIHA-8B5CF6?style=for-the-badge&labelColor=0B1024)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white) ![EasyOCR](https://img.shields.io/badge/EasyOCR-00B39F?style=flat-square) ![Tesseract](https://img.shields.io/badge/Tesseract-3D7DCA?style=flat-square) ![PaddleOCR](https://img.shields.io/badge/PaddleOCR-2932E1?style=flat-square) ![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat-square&logo=jupyter&logoColor=white)

> ⚡ **Part of [BRIHA](https://github.com/asad110abbas)** · Briha Research, built by Syed Asad Abbas.

Compares **three OCR engines side by side** (EasyOCR, Tesseract and PaddleOCR) on the same images, with
OpenCV pre-processing to improve accuracy. It also converts math formulas to LaTeX with **pix2tex**.

## Pipeline
```mermaid
flowchart LR
    A[Image / scanned page] --> B[OpenCV pre-processing<br/>grayscale · threshold · denoise · resize]
    B --> C1[EasyOCR]
    B --> C2[Tesseract]
    B --> C3[PaddleOCR]
    C1 & C2 & C3 --> D[Compare text + confidence]
    A --> F[pix2tex: formula → LaTeX]
```

## Highlights
- **3 engines, one notebook:** pick the best engine per document type
- **Pre-processing** with OpenCV and PIL for noisy scans
- **Visual inspection** with bounding boxes drawn using Matplotlib
- **Math OCR:** image of an equation → LaTeX (pix2tex)

## Run
```bash
pip install easyocr pytesseract paddleocr opencv-python pillow matplotlib pix2tex
```
Install the Tesseract binary for your OS, then open `OCR_Text Extraction.ipynb`.
