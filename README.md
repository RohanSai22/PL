Based on the provided code and project structure, here's a comprehensive README for the Memory Efficient Scientific Paper Analyzer project:

# Memory Efficient Scientific Paper Analyzer

## Overview

This project provides a robust and memory-efficient tool for analyzing scientific papers and documents. It can process various file types, extract key information, and generate summaries using advanced natural language processing and computer vision techniques.

## Features

- Supports multiple file formats (PDF, DOC/DOCX, TXT)
- Extracts and analyzes text content
- Processes images and generates captions
- Extracts and summarizes tables
- Generates overall summaries of the document
- Memory-efficient processing for large documents
- Outputs results in both JSON and Markdown formats

## Requirements

- Python 3.7+
- PyMuPDF (fitz)
- OpenCV
- NumPy
- Pillow
- pytesseract
- Transformers
- PyTorch
- pandas
- python-docx
- svglib
- reportlab
- yake
- camelot-py

## Installation

1. Clone the repository:
   ```
   git clone https://github.com/yourusername/memory-efficient-scientific-paper-analyzer.git
   cd memory-efficient-scientific-paper-analyzer
   ```

2. Create a virtual environment (optional but recommended):
   ```
   python -m venv venv
   source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
   ```

3. Install the required packages:
   ```
   pip install -r requirements.txt
   ```

## Usage

1. Run the main script:
   ```
   python main.py
   ```

2. When prompted, upload your scientific paper or document file.

3. The script will process the document and generate output files in the `extracted_data` directory.

4. The analysis results will be available in two formats:
   - `output.json`: Detailed JSON output of all extracted elements and summaries
   - `output.md`: A Markdown summary of the document analysis

## Class Structure

### `ContentType`
An enumeration of different content types that can be extracted from a document (e.g., Text, Visual, Quantitative).

### `FileType`
An enumeration of supported file types for input documents.

### `MemoryEfficientScientificPaperAnalyzer`
The main class that handles the document analysis process.

#### Key Methods:
- `__init__(self, input_path)`: Initializes the analyzer with the input document path.
- `analyze(self)`: Main method to start the analysis process.
- `_process_pdf(self)`: Handles PDF document processing.
- `_process_text(self, text, page_num)`: Processes and summarizes text content.
- `_process_images(self, page, page_num)`: Extracts and analyzes images from the document.
- `_process_tables(self, page_num)`: Extracts and summarizes tables from the document.
- `_create_output_file(self)`: Generates the final output files (JSON and Markdown).

## Output

The analyzer generates two types of output files:

1. `output.json`: A detailed JSON file containing:
   - File name
   - List of extracted elements (text, images, tables) with their types, content, summaries, and page numbers
   - Overall document summary

2. `output.md`: A Markdown file providing a human-readable summary of the document analysis.

## Limitations and Future Improvements

- Currently optimized for scientific papers; may need adjustments for other document types.
- Image and table extraction might not work perfectly for all document layouts.
- Could be extended to support more file formats and content types.
- Potential for implementing more advanced NLP techniques for better summarization.

## Contributing

Contributions to improve the analyzer are welcome. Please follow these steps:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/your-feature-name`)
3. Make your changes and commit them (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin feature/your-feature-name`)
5. Create a new Pull Request

## License

GNU General Public License (GPL)

## Contact

[Your Name] - maragonirohansai@gmail.com

Project Link: [https://github.com/yourusername/memory-efficient-scientific-paper-analyzer](https://github.com/yourusername/memory-efficient-scientific-paper-analyzer)
