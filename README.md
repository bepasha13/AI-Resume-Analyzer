Installation Guide: AI Resume Analyzer (Python + Flask + RoBERTa)
Project Overview
Tech Stack:
- Python 3.10+
- Flask
- SentenceTransformers (RoBERTa)
- Tailwind CSS
- PyMuPDF
- Transformers (for NER)
Prerequisites
- Python 3.10+ installed: https://www.python.org/downloads/
- pip should be working
- (Optional) Use a virtual environment for isolation
Installation Steps
1. Download the Project:
   - Unzip the project to your working directory.

2. Open Terminal / Command Prompt:
   cd Resume_Analyzer

   (Optional) Create virtual environment:
   python -m venv venv
   venv\Scripts\activate  (Windows)
   source venv/bin/activate (Linux/macOS)

3. Install Required Libraries:
   pip install -r requirements.txt

4. Download NLTK Stopwords (once):
   python
>>> import nltk
>>> nltk.download('stopwords')
>>> exit()

5. Run the Flask App:
   python app.py
   Open browser at: http://127.0.0.1:5000/
Project Pages
- /            → Main Resume Match Page
- /multi-jd     → Compare resume with 3 job descriptions
- /result       → See match score, skills, suggestions
Supported Formats
- Resume: PDF only
- JD: Text box input (paste from job sites)
Model Details
- RoBERTa Model: stsb-roberta-large
- NER Model: dslim/bert-base-NER
- Both models loaded from HuggingFace Transformers
Tips
- Resume should be a clean, readable PDF
- JD should be a full copy (from LinkedIn, etc.)
- Best run using Python 3.10
