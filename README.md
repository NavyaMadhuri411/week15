# Experiment 15: Multimodal Prompting for Receipt Information Extraction

## Aim
The aim of this experiment is to explore image-based information extraction by converting a restaurant receipt image into structured JSON data and validating the logical consistency of its monetary values.

## Problem Statement
A restaurant receipt contains information such as the restaurant name, date, ordered items, prices, subtotal, tax, and total. Manually extracting this information can be time-consuming. This experiment uses Optical Character Recognition (OCR) to extract text from a receipt image, converts the extracted information into JSON, and checks whether the subtotal plus tax equals the receipt total.

## Technologies Used
- Python
- Pillow
- Tesseract OCR
- pytesseract
- JSON
- Base64 encoding

## Methodology
1. Generate a sample restaurant receipt image.
2. Encode the receipt image into Base64 format.
3. Decode the image and extract text using OCR.
4. Identify the restaurant name, date, ordered items, subtotal, tax, and total.
5. Convert the extracted information into a structured JSON object.
6. Validate the receipt by comparing subtotal plus tax with the total.
7. Save the receipt image, JSON result, and execution output in the outputs folder.

## Expected Output
The program generates a JSON object containing the extracted receipt information. It also prints a validation report showing the subtotal, tax, receipt total, and whether the values are consistent.

Example validation:

- Subtotal: 674.00
- Tax: 33.70
- Receipt Total: 707.70
- Consistent: True

## Conclusion
This experiment demonstrates a basic image-to-text information extraction pipeline using OCR, Base64 encoding, JSON formatting, and arithmetic validation. The implementation uses a simulated receipt and does not require a paid LLM API. It demonstrates the preprocessing and structured-output stages of a multimodal workflow; it does not use a vision-capable LLM to interpret the image.
