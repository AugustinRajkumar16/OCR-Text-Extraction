# OCR - Extract Text from Forms, Documents, and Bank Statements

## Overview

This project provides a comprehensive solution for extracting both printed and handwritten text from various scanned documents and forms. It also supports the extraction of structured information from financial documents such as bank statements, where personal details and transaction data are arranged in tabular formats.

The system handles a variety of document formats and export the extracted data into structured formats like JSON, CSV, or XLSX for further analysis and processing.

## OCR (Optical Character Recognition)

**OCR** (Optical Character Recognition) is the technology that enables machines to convert different types of documents (scanned paper documents, PDFs, or images) into machine-readable text. It is widely used for extracting text from scanned documents, digitizing printed books, invoices, or forms, and many more applications.

### Types of OCR Tools

1. **Tesseract OCR**  
   - **Overview**: One of the most popular open-source OCR engines developed by Google. Tesseract is highly flexible and supports many languages.
   - **Strengths**:
     - Works well with both printed and handwritten text.
     - Supports multiple languages and can be trained to recognize new languages.
     - Flexible configuration with options like page segmentation modes (PSM) and OCR engine modes (OEM).
   - **Limitations**:
     - Slower for large documents or high-volume tasks.
     - Requires some pre-processing (e.g., image cleaning) for optimal results.

2. **EasyOCR**  
   - **Overview**: An easy-to-use OCR tool developed by the Jaided AI team, supporting over 70 languages and specialized in multilingual text extraction.
   - **Strengths**:
     - Supports handwritten text better than many other OCR tools.
     - Easier to implement and use with pre-trained models, making it a great choice for beginners.
     - Excellent accuracy for various languages, including Asian scripts (e.g., Chinese, Japanese, Korean).
   - **Limitations**:
     - Slightly slower than Tesseract in some cases.
     - Customization options are limited compared to Tesseract.

3. **PaddleOCR**  
   - **Overview**: A highly efficient and accurate OCR tool developed by the PaddlePaddle team. It provides both lightweight and large OCR models for better performance across a wide range of devices.
   - **Strengths**:
     - High recognition accuracy for both printed and handwritten text.
     - Supports vertical and horizontal text extraction, making it useful for complex layouts.
     - Can extract multilingual text, including Chinese, English, and many others.
     - Designed for high-performance tasks; faster than many traditional OCR tools.
   - **Limitations**:
     - Requires more setup and has a steeper learning curve compared to EasyOCR.

### Good to Know

- **Accuracy vs Speed**: When choosing an OCR tool, consider the trade-off between speed and accuracy. Tesseract is versatile and can be fine-tuned, but PaddleOCR is faster for large-scale tasks.
  
- **Multilingual Support**: If your documents contain multilingual text, EasyOCR and PaddleOCR provide better out-of-the-box support compared to Tesseract.

- **Handwritten Text**: For handwritten documents, EasyOCR and PaddleOCR tend to perform better than Tesseract without custom training.

- **Customizability**: Tesseract is highly customizable with configuration options, which may be useful if you're working with diverse or non-standard documents.

- **Hardware Performance**: PaddleOCR is optimized for speed and can handle large documents efficiently. If you're processing many documents or need faster results, PaddleOCR might be your best option.

## Features

### 1.a. **Extraction of Printed and Handwritten Text:**

- Capable of extracting both handwritten and printed (typed) text from scanned documents or forms (e.g., surveys, invoices, applications).
- Extracted text is structured into a key-value format for easy processing.
- Supports a variety of document formats, such as PDF, PNG, JPG, TIFF, BMP.
- High accuracy for both printed and handwritten text detection using OCR techniques.

### 1.b. **Bank Statement Data Extraction:**

- Extracts personal details (e.g., name, bank name) from the top of bank statements.
- Extracts financial transaction data from table-based formats (e.g., date, transaction details, amount, balance).
- Organises personal details in key-value pairs and transaction data in a tabular format.
- Supports input document types like PDF, PNG, JPG, TIFF, BMP.
  
### 2. **Export Formats:**

- Export the extracted data in **JSON**, **CSV**, or **XLSX** formats.
- Flexible export options for personal details and transaction data.
- Includes detailed error handling and logging to capture any issues during the extraction process.

## Requirements

### **Input:**

- Scanned or image-based documents containing both printed and handwritten text (e.g., forms, applications, surveys).
- Bank statements or financial documents with personal details and tabular transaction data.

### **Output:**

- Key-value structured data for both handwritten and printed text from forms.
- Personal details and transactions from bank statements extracted into a key-value format (for personal details) and tabular format (for transactions).
- Exported to various file formats, including **JSON**, **CSV**, and **XLSX**.

## Prerequisites

Before running the project, make sure you have the following installed:

- Python 3.8+
- pip (Python package installer)

## Get the Source Code

You can get the source code in two ways:

- **Download as a ZIP file:** [Download here](https://github.com/AugustinRajkumar16/OCR-Text-Extraction/archive/refs/heads/main.zip), then extract it to a folder of your choice.
- **Clone the repository using Git:**

    ```bash
    git clone https://github.com/AugustinRajkumar16/OCR-Text-Extraction.git
    ```

## Install the Required Python Packages

In your project directory, install the necessary Python libraries:

```bash
    pip install pytesseract
    pip install easyocr
    pip install paddlepaddle paddleocr
```

## Running the program

1. To extract text from documents or forms, run the **Extraction_of_Documents_or_Forms.ipynb** notebook from the downloaded repository.
2. To extract table formats from documents like bank statements, run the **Extraction_of_Table_Formats.ipynb** notebook from the repository.

## Contributions

Contributions are welcome! Feel free to open issues, suggest improvements, or submit pull requests.