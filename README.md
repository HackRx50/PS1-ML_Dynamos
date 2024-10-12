# Bajaj_Hack

# Table Detection & Line-Item Extraction
The goal of this project is to build an engine that processes hospitalization invoices in both image and PDF formats. The engine uses Optical Character Recognition (OCR) and Named Entity Recognition (NER) techniques to extract key information such as line items and their associated amounts. 
Input: The program accepts hospitalization invoices in both image (JPEG, PNG) and PDF formats.
Output: The extracted line items (services/products) and their corresponding amounts.

## How to run the kaggle notebook:

1. Make sure to use the GPU P100 as accelerator.
2. In the session options, turn on the internet.

## Using Qwen 2 VL model to solve this problem

The Qwen-2 VL model, a vision-language model, is utilized to address the challenge of extracting structured information from hospitalization invoices. This model effectively combines visual input (images of invoices) with natural language processing capabilities to perform OCR (Optical Character Recognition) and NER (Named Entity Recognition) tasks. Here's how the Qwen-2 VL model helps solve this problem:

#### 1. *OCR for Text Extraction*
Qwen-2 VL efficiently processes both printed and handwritten text in images or PDFs. It identifies key text regions in the invoice, such as item descriptions, dates, and amounts. The model can handle rotated or misaligned documents, ensuring accurate detection of text elements regardless of the invoice layout.


#### 2. Prompt and Message Structure
The model is given a structured task using a carefully crafted prompt. The system is instructed to extract specific entities from the invoice, such as item names and their corresponding final amounts. If no item names are detected, the model is instructed to extract only the final total amount from the invoice.

#### 3. *Handling Complex Layouts*
Invoices often contain tables with multiple rows and columns. Qwen-2 VL is capable of interpreting these layouts and extracting relevant information from tabular structures. Whether an invoice is in a simple or complex format (e.g., rotated tables or multi-column layouts), the model can parse the visual structure and extract the line-item details.
