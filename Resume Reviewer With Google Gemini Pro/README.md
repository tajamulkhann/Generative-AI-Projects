# 📄 Resume Reviewer With Google Gemini Pro

An AI‐powered tool that uses Google’s Gemini Pro model to analyse a resume, provide detailed feedback, and suggest improvements for optimising candidate profiles.

---

## 📌 Project Overview

This project builds a complete pipeline:

* Upload a resume (PDF/DOCX/text).
* Use Gemini Pro to parse the resume content, extract skills, experience, and format.
* Provide structured feedback—highlight missing keywords, formatting issues, strength summary, proposal for improvement.
* Support candidates to refine their resumes for specific job themes or industries.

---

## 🧰 Tech Stack

* **Language:** Python
* **Libraries/Tools:** `google-generativeai`, `PyPDF2` or `pdfplumber`, `docx2txt`, `streamlit` (for UI)
* **Model / Service:** Google Gemini Pro (multimodal / document understanding)
* **Environment:** Jupyter Notebook / Google Colab / Web App

---

## 🔄 Workflow Summary

### 1. Resume Upload & Extraction

* User uploads resume file (.pdf, .docx, .txt).
* Extract raw text and key resume sections (e.g., Summary, Skills, Experience, Education).
* Pre-process text (remove non-printables, normalise whitespace).

### 2. Gemini Pro Prompting & Review

* Construct an instruction prompt:

  ```
  You are a senior hiring manager. Given the following resume content: {resume_text}, provide:  
  1) A short summary of candidate’s strengths.  
  2) Key missing skills or keywords related to job role {job_role} (if specified).  
  3) Formatting or structuring suggestions to improve readability.  
  4) A confidence score of the resume for that role.  
  ```
* Optionally accept `job_role` input from user for tailored feedback.
* Send the prompt (and text) to Gemini Pro and capture feedback output.

### 3. Feedback Display & Actionable Insights

* Show the results: strengths, missing keywords, formatting suggestions, score.
* Highlight parts of the resume that match job role keywords vs parts needing improvement.
* Enable the user to download a feedback report or resume-improved checklist.

### 4. UI/Interactivity

* Web interface (Streamlit): upload panel, job role dropdown/input, feedback display, download button.
* Optionally allow multiple resumes and comparison for improvement tracking.

---

## 📁 Project Structure

```
Resume-Reviewer-Gemini-Pro/
│── data/
│   └── sample_resumes/
│── notebooks/
│   └── review_pipeline.ipynb
│── src/
│   ├── app.py
│   ├── resume_parser.py
│   ├── gemini_interface.py
│   └── feedback_report.py
│── README.md
│── requirements.txt
```

---

## 📈 Key Findings

* Gemini Pro supports document comprehension and can generate helpful feedback when given well-structured prompts.
* Providing a specific target role (job_role) improves relevance of feedback and missing keywords list.
* Formatting suggestions help target clarity, while keyword matching aids scoring for Applicant Tracking Systems (ATS).
* The tool can accelerate candidate preparation and resume refinement, positioning applicants more competitively in job markets.

---

## 🚀 Future Improvements

* Add widely used job categories dropdown (data scientist, product manager), plus templates per category.
* Enable bulk resume review (upload multiple resumes, batch feedback).
* Add interactive editing: show parts of resume needing update and enable drag-&-drop correction.
* Integrate with LinkedIn or job board APIs to fetch target job descriptions and auto-match resume.
* Deploy as SaaS/web service with user login, analytics dashboard (resume improvement over time), and premium features (multiple reviews, recruiter keywords).
* Monitor feedback accuracy and bias (ensure inclusive and fair recommendations across demographics).

---

## 🧑‍💻 Author

**[Tajamul Khan](https://www.linkedin.com/in/tajamulkhann/) – Data Scientist & AI Engineer**

---

## Let's Connect <img src="https://github.com/JayantGoel001/JayantGoel001/blob/master/GIF/Handshake.gif" height="30px" style="max-width:100%;">

<div align="center">

<a href="https://www.linkedin.com/in/tajamulkhann/">
<img src="https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white">
</a>
<a href="https://www.instagram.com/tajamul.datascientist/" target="_blank">
<img src="https://img.shields.io/badge/Instagram-%23E4405F.svg?style=for-the-badge&logo=instagram&logoColor=white">
</a>
<a href="https://topmate.io/tajamulkhan" target="_blank">
<img src="https://img.shields.io/badge/Topmate-FF0000?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxMDAgMTAwIj48Y2lyY2xlIGN4PSI1MCIgY3k9IjUwIiByPSI0MCIgZmlsbD0id2hpdGUiLz48L3N2Zz4=&logoColor=white">
</a>
<a href="https://www.whatsapp.com/channel/0029VaYs05jJkK7JKCesw42f">
<img src="https://img.shields.io/badge/WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white">
</a>
<a href="https://t.me/tajamul_khan">
<img src="https://img.shields.io/badge/Telegram-26A5E4?style=for-the-badge&logo=telegram&logoColor=white">
</a>
<a href="https://substack.com/@tajamulkhan">
<img src="https://img.shields.io/badge/Substack-%23006f5c.svg?style=for-the-badge&logo=substack&logoColor=FF6719">
</a>
<a href="https://www.kaggle.com/tajamulkhan">
<img src="https://img.shields.io/badge/Kaggle-035a7d?style=for-the-badge&logo=kaggle&logoColor=white">
</a>
<a href="https://github.com/tajamulkhann">
<img src="https://img.shields.io/badge/Github-12100E?style=for-the-badge&logo=github&logoColor=white">
</a>
<a href="https://medium.com/@tajamulkhan">
<img src="https://img.shields.io/badge/Medium-12100E?style=for-the-badge&logo=medium&logoColor=white">
</a>
<a href="https://www.youtube.com">
<img src="https://img.shields.io/badge/YouTube-%23FF0000.svg?style=for-the-badge&logo=YouTube&logoColor=white">
</a>
</div>
