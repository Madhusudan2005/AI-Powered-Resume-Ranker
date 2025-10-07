🤖 AI-Powered Resume Ranker
This project is an AI-powered tool designed to automatically screen and rank candidate resumes against a specific job description (JD) using Natural Language Processing (NLP) techniques. It was developed as part of an internship project for candidate screening automation.

The final output is a ranked list displayed on a local web server (Flask), providing HR teams with an objective, data-driven match score for each applicant.

✨ Features
PDF Text Extraction: Uses pdfplumber to reliably extract text from structured PDF resumes.

NLP Preprocessing: Employs SpaCy for robust cleaning, lemmatization, and stop-word removal.

Objective Scoring: Ranks resumes based on Cosine Similarity between the Job Description vector and the resume vector.

TF-IDF Vectorization: Utilizes Term Frequency-Inverse Document Frequency to prioritize specialized keywords relevant to the role.

Web Interface: Hosted via Flask, providing a clean, professional, and sortable ranking table.

HR Report: Allows downloading the final ranking data as a CSV file.

🛠️ Technology Stack
Core Logic: Python

Libraries: Flask, Pandas, Scikit-learn, SpaCy, pdfplumber

NLP Model: TF-IDF + Cosine Similarity

UI: HTML/CSS (Bootstrap 5)

🚀 How to Run Locally
1. Setup
Clone the repository and navigate into the project directory:

git clone <YOUR_REPO_URL>
cd AI-Powered-Resume-Ranker

2. Virtual Environment & Dependencies
It is highly recommended to use a virtual environment.

# Create and activate environment
python -m venv venv
# Windows
.\venv\Scripts\activate
# Linux/macOS
source venv/bin/activate

# Install required packages
pip install -r requirements.txt

# Download the required SpaCy model
python -m spacy download en_core_web_sm

3. Data Preparation
You must provide two inputs:

Job Description: The target JD is already provided in job_description.txt (Data Scientist role).

Resumes: Create a folder named resumes/ in the root directory and place all your sample candidate PDFs (.pdf files) inside it.

AI-Powered-Resume-Ranker/
├── app.py
├── ranking_engine.py
├── job_description.txt
└── resumes/
    ├── candidate_A.pdf
    └── candidate_B.pdf

4. Run the Application
Start the Flask server from your terminal:

python app.py

Open your web browser and navigate to: http://127.0.0.1:5000/

You now have all the necessary files structured for a professional GitHub repository! You can create your repository and upload these files. Good luck with your submission!
