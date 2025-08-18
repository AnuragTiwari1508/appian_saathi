# Appian Saathi

## Project Idea

**Appian Saathi** is a document processing platform designed to automate the extraction, classification, and summarization of information from financial and official documents. It leverages both PHP and Python (Flask) microservices to provide a seamless workflow for document upload, OCR, metadata extraction, classification, and summarization. The platform is intended for organizations or individuals who need to process large volumes of documents efficiently.

## Features
- **Document Upload:** Upload PDF documents via a web interface.
- **OCR Processing:** Extract text from scanned documents using OCR (Python Flask service).
- **Metadata Extraction:** Automatically extract key metadata from documents.
- **Document Classification:** Classify documents into categories using machine learning.
- **Summarization:** Generate concise summaries of document content.
- **Feedback System:** Users can provide feedback on processed results.
- **Multi-Component Architecture:** PHP for main web app and API, Python Flask for document processing.

## Project Structure
```
APPIAN-SAATHI-main (1)/APPIAN-SAATHI-main/APPian saathi/
├── composer.json, composer.lock         # PHP dependencies
├── config.php, index.php               # Main PHP entry points
├── Controllers/                        # PHP controllers
├── Database/                           # SQL schema and migrations
├── Document processor/                 # Python Flask microservice
│   ├── app.py, routes.py               # Flask app and routes
│   ├── templates/                      # Flask HTML templates
│   ├── uploads/                        # Uploaded documents
│   └── ...                             # Supporting Python modules
├── Frontend with DB/                   # Static HTML/JS frontend
├── Logs/, Models/, Public/, Routes/, Services/, Tests/, Views/
└── vendor/                             # PHP vendor dependencies
```

## Prerequisites
- **PHP >= 7.4**
- **Composer** (for PHP dependencies)
- **Python 3.8+**
- **pip** (for Python dependencies)

## Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/AnuragTiwari1508/appian_saathi.git
cd appian_saathi/APPIAN-SAATHI-main\ \(1\)/APPIAN-SAATHI-main/APPian\ saathi
```

### 2. Install PHP Dependencies
```bash
composer install
```

### 3. Install Python Dependencies
```bash
cd "Document processor"
pip install -r requirements.txt  # If requirements.txt is missing, install manually:
pip install flask transformers torch pytesseract pdfplumber pdf2image pymysql boto3 pillow
```

### 4. Start the PHP Web Server
```bash
php -S localhost:8000
```

### 5. Start the Python Flask Server
```bash
cd "Document processor"
python3 routes.py
# Flask will run on http://localhost:5000
```

### 6. Access the Application
- Main Web App: [http://localhost:8000](http://localhost:8000)
- Document Processor: [http://localhost:5000](http://localhost:5000)

## Notes
- Make sure both servers are running for full functionality.
- The `uploads/` and `vendor/` directories are excluded from version control via `.gitignore`.
- For production, use a proper WSGI server for Flask and a production-ready PHP server.

## Contributors
- [Anurag Tiwari](https://github.com/AnuragTiwari1508)

---
Feel free to open issues or contribute to the project!
