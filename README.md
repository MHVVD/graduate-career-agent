# Gradpilot: Graduate Career Agent

An AI career coach that helps fresh graduates get jobs, internships and scholarships. It is a FastAPI web app with user accounts. A Llama 3.2 model (through the Hugging Face Inference API) powers chat coaching, CV tailoring, job-gap analysis and LaTeX CV generation.

**[Watch the demo](https://www.loom.com/share/fad7c1952eca40879a0ec6fd727c2015)**

## Features

### 1. Chat Coach
- **Interactive Career Advice**: Engage in a natural conversation with an AI career expert.
- **Personalized Guidance**: Get advice on job search strategies, interview preparation, and career planning.
- **Context-Aware**: The agent maintains conversation history to provide relevant follow-up responses.

### 2. CV Tailoring
- **Job-Specific Optimization**: Upload your CV (PDF) and a job description to receive a rewritten version of your CV.
- **Skill Highlighting**: The agent identifies and emphasizes skills relevant to the specific job opportunity.
- **Markdown Output**: The tailored CV is provided in a clean Markdown format, ready for editing.

### 3. Job Analysis
- **Gap Analysis**: Compare your CV against a job description to identify missing skills or qualifications.
- **Priority Scoring**: Receive a ranked list of missing skills (High/Medium/Low importance) to focus your upskilling efforts.
- **Requirement Extraction**: Automatically extract key requirements, tools, and qualifications from job postings.

### 4. Profile Insights
- **Skill Extraction**: Automatically extract and categorize skills from your CV into Technical, Soft, and Domain-Specific categories.
- **ATS Score Estimation**: Get an estimated ATS (Applicant Tracking System) compatibility score (0-100).
- **Improvement Suggestions**: Receive actionable feedback on formatting, keyword density, and structure to improve your ATS ranking.

### 5. Job Description Summarization
- **Structured Summary**: Convert lengthy job descriptions into concise summaries.
- **Key Information**: Quickly identify Key Responsibilities, Critical Skills, Company Expectations, and Cultural Attributes.

## Setup

1.  **Clone the repository**
    ```bash
    git clone https://github.com/MHVVD/graduate-career-agent.git
    cd graduate-career-agent
    ```

2.  **Install Dependencies**
    ```bash
    pip install -r requirements.txt
    ```

3.  **Environment Variables**
    Copy `.env.example` to `.env` and fill in your Hugging Face token and a JWT signing secret:
    ```
    HF_TOKEN=your_token_here
    SECRET_KEY=a_long_random_string
    ```

4.  **Run Locally**
    ```bash
    python main.py
    ```
    Visit `http://localhost:8000` in your browser, then register an account.

5.  **Run the end-to-end tests** (with the server running on port 8000)
    ```bash
    pytest test_auth.py test_chat.py
    ```

## Deployment
This project includes a `Dockerfile` and `Procfile` for easy deployment on platforms like Render or Heroku.

## Technologies
- Python (FastAPI, SQLAlchemy + SQLite, JWT auth)
- HTML/CSS/JS (vanilla)
- Hugging Face Inference API (Meta Llama 3.2 3B Instruct)
- LaTeX for PDF CV generation
