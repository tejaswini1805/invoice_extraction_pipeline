# 🧾 Invoice Extraction Pipeline

> A real-world NLP + Computer Vision project to extract structured information from unstructured invoice images using OCR and deep learning.

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
![Invoice Extraction Demo](output/sample_invoice_demo.png)

