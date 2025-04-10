# 🧾 Invoice Information Extraction using OCR + LayoutLMv3

> A real-world NLP + Computer Vision project to extract structured information from unstructured invoice images using a combination of **OCR (Tesseract)** and **transformer-based deep learning (LayoutLMv3)**.

---

## 📌 Problem Statement

Businesses often receive invoices in various formats (PDFs, images, scans), making it difficult to automatically extract structured data like invoice numbers, dates, seller information, and totals.  
Manual data entry is slow, error-prone, and unscalable.

This project aims to build a pipeline that can automatically extract key-value fields from invoice images, making the process fast, scalable, and intelligent.

---

## 🎯 Objective

- 🧠 Extract structured information from scanned/unstructured invoice images
- 🧾 Identify fields such as:
  - Invoice Number
  - Invoice Date
  - Seller & Client Info
  - Line Items
  - Net, VAT & Gross Totals
- 🔍 Use a combination of **OCR (Tesseract)** and **deep learning (LayoutLMv3)** for intelligent extraction
- 💾 Save outputs in structured formats like JSON or CSV
- ♻️ Design the pipeline to be modular and scalable

---

## 🛠️ Tools & Technologies

| Category           | Tech Stack                                   |
|--------------------|----------------------------------------------|
| OCR Engine         | Tesseract OCR                                |
| Deep Learning      | LayoutLMv3 (Transformer-based model)         |
| NLP + CV           | Hugging Face Transformers + FUNSD Dataset    |
| Programming        | Python, OpenCV, Regex, PyTorch, JSON         |
| IDE / Platform     | Jupyter Notebook, Anaconda, GitHub           |

This is a hybrid **Computer Vision + NLP project**, where:
- CV is used for reading document layouts and images
- NLP is used to identify and label fields within the text

---

## 🧠 Approach

### 🔹 Phase 1: OCR + Rule-Based Extraction
- Used **Tesseract OCR** to extract raw text from invoice images.
- Used Python + regex to extract specific fields like:
  - Invoice Number
  - Invoice Date
  - Seller & Client Info
  - Items & Totals

### 🔹 Phase 2: Deep Learning with LayoutLMv3
- Trained on **FUNSD** dataset using Hugging Face
- Preprocessed tokens, bounding boxes, and labels
- Fine-tuned `microsoft/layoutlmv3-base` for document understanding
- Performed inference on real invoice images

---

## 📦 Project Output

Sample extracted fields:

```json
{
  "invoice_number": "17045625",
  "invoice_date": "11/01/2017",
  "seller_name": "Bass-Petersen",
  "client_name": "Davidson-Martinez",
  "gross_total": "31.06",
  "vat_total": "2.82"
}

---

## 📌 Future Improvements

- 🏷️ Train on a **custom-labeled dataset** with specific fields like `invoice_number`, `net_total`, etc. for better accuracy  
- 📄 Extend the pipeline to support other document types like **receipts**, **purchase orders**, or **ID cards**  
- 🌐 Build a **Streamlit** or web-based app for uploading invoice images and viewing extracted results in real-time  
- 🧠 Fine-tune the model using **domain-specific invoices** from industries like e-commerce or logistics  
- ☁️ Deploy the solution using **Flask**, **FastAPI**, or **AWS Lambda** for scalable document automation  

---
