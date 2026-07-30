# HireSense AI

> **An AI-powered Resume Evaluation System using Groq LLMs, Pydantic, and Python**

HireSense AI is an intelligent resume evaluation system that automates the process of comparing resumes with job descriptions. Instead of relying solely on keyword matching, it uses Large Language Models (LLMs) to understand the context of both documents and generate an explainable compatibility score with detailed reasoning.

The project extracts structured information from resumes and job descriptions, performs semantic matching, and ranks candidates based on their suitability for a given role.

---

# Features

- Accepts any Job Description as text input
- Supports PDF and DOCX resumes
- Automatically extracts resume text
- Extracts structured information using **Pydantic**
- Parses:
  - Skills
  - Experience
  - Education
  - Projects
  - Certifications
- Performs semantic Resume ↔ Job Description matching using Groq LLMs
- Generates:
  - Overall Match Score
  - Matching Skills
  - Missing Skills
  - Experience Analysis
  - Final Hiring Verdict
- Ranks multiple candidates based on compatibility score
- Uses deterministic responses with **Temperature = 0**
- Uses JSON Mode for reliable structured outputs

---

# Tech Stack

- Python
- Groq API
- Pydantic
- PyPDF
- python-docx
- python-dotenv

---

# Project Structure

```
HireSense-AI/
│
├── resumes/
│   ├── resume1.pdf
│   ├── resume2.docx
│
├── resume_parser.py
├── README.md
├── requirements.txt
├── .gitignore
├── .env
└── pyproject.toml
```

---

# Workflow

```
Job Description
        │
        ▼
Extract Structured JD
        │
        ▼
Read Resume (PDF / DOCX)
        │
        ▼
Extract Resume Text
        │
        ▼
Parse using Pydantic Schema
        │
        ▼
LLM Semantic Matching
        │
        ▼
Generate
• Match Score
• Skill Analysis
• Experience Match
• Hiring Verdict
        │
        ▼
Rank Candidates
```

---

# Installation

Clone the repository

```bash
git clone https://github.com/Bhumi-2904/HireSense-AI.git
```

Move inside the project

```bash
cd HireSense-AI
```

Install dependencies

```bash
pip install -r requirements.txt
```

---

# Environment Variables

Create a `.env` file in the root directory.

```env
GROQ_API_KEY=your_groq_api_key
```

---

# Running the Project

Place all resumes inside the `resumes/` folder.

Update the Job Description inside:

```python
job_description = """
Your Job Description
"""
```

Run the project

```bash
python resume_parser.py
```

---

# Output

For every candidate, the system generates:

- Candidate Name
- Overall Match Score
- Matching Skills
- Missing Skills
- Experience Analysis
- Final Hiring Verdict

Candidates are automatically ranked from highest to lowest compatibility.

---

# Example

```
Processing: Resume_01.pdf

Score : 92%

Matching Skills:
✔ Python
✔ SQL
✔ Machine Learning

Missing Skills:
✘ AWS

Verdict:
Highly Recommended
```

---

# Why HireSense AI?

Traditional ATS systems mostly rely on exact keyword matching, which often misses relevant candidates.

HireSense AI uses Large Language Models to understand the semantic meaning of resumes and job descriptions, resulting in a more intelligent, explainable, and context-aware evaluation process.

---

# Future Improvements

- Retrieval-Augmented Generation (RAG)
- Interactive Web Dashboard
- Resume Feedback Suggestions
- Skill Gap Recommendations
- Batch Job Description Evaluation
- Recruiter Analytics Dashboard
- Candidate Chat Assistant

---

# Author

**Bhumi Kumari Sah**

Computer Science Engineering Student

GitHub: https://github.com/Bhumi-2904

LinkedIn: https://www.linkedin.com/in/bhumi-kumari-sah

---

## If you found this project useful, consider giving it a ⭐.
