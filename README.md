# AI-Powered PDF Parsing

## Project Overview
This project focuses on using AI and machine learning to extract structured data from PDF files (invoices/quotes), transforming it into JSON format, and generating editable and downloadable HTML templates. The system aims to streamline document processing by simplifying data extraction, providing an intuitive interface for users to view PDFs, review extracted data, and download HTML representations of the documents.

## Features
- PDF Upload: Upload a single PDF file (invoice/quote) for processing.
- PDF Viewer: Scrollable PDF viewer embedded in the web interface.
- AI-Powered Data Extraction: Automatically extract structured data from PDF files using AI models.
- JSON Representation: View extracted data in a readable and formatted JSON structure.
- HTML Generation: Convert extracted JSON data into a standardized, editable HTML template.
- Live HTML Editor: Edit the generated HTML template and preview live changes.
- Downloadable HTML: Download the edited HTML version of the invoice/quote.

## Technology Stack
- Frontend:
  - Streamlit (for the web interface)
  - PyMuPDF (Fitz) for PDF rendering
  - HTML/CSS for displaying and editing templates
- Backend:
  - Python (3.8+)
  - Google Generative AI (Gemini) for data extraction
  - Langchain for handling LLM prompts
  - Pandas for data handling
- Others:
  - JSON for structured data
  - Base64 for embedding PDFs

## Project Structure
```bash
├── Uploaded_Quotes/           # Folder to store uploaded quotes
├── Uploaded_Invoices/         # Folder to store uploaded invoices
├── app.py                    # Main application logic for handling invoices/quotes
├── README.md                  # Project documentation
├── requirements.txt           # Python dependencies
└── .env                       # Environment variables (e.g., API keys)
```

## Setup and Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/PDF-Parsing.git
   cd PDF-Parsing
   ```

2. Set up a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate     # On Windows: venv\Scripts\activate
   ```

3. Install the dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Set up environment variables:
   Create a `.env` file and add your Google Generative AI API key:
   ```bash
   GOOGLE_API_KEY=your-api-key-here
   ```

5. Run the application:
   ```bash
   streamlit run app.py
   ```

## Usage

1. Upload a PDF:
   - After launching the application, upload an invoice or quote PDF file through the file uploader interface.
   
2. View Extracted Data:
   - The system will display the uploaded PDF and the extracted JSON data side by side for easy comparison.

3. Generate HTML:
   - Click on the Generate HTML button to convert the extracted JSON data into an editable HTML template.

4. Edit HTML:
   - Modify the generated HTML template in the live editor, with a live preview of the changes.

5. Download HTML:
   - Once editing is complete, download the HTML file using the Download HTML button.

## Environment Variables

- `GOOGLE_API_KEY`: Your API key for Google Generative AI.

## File Upload Limitations
- Only one PDF file can be uploaded at a time.
- Supported file types: `.pdf`

## Contributing
We welcome contributions! If you’d like to contribute, please follow these steps:
1. Fork the repository.
2. Create a new branch for your feature/bugfix.
3. Commit your changes.
4. Push to your fork and submit a pull request.
