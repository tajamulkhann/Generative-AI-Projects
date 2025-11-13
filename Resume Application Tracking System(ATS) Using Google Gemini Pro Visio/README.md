# 📋 Resume Application Tracking System (ATS) Using Google Gemini Pro Vision

An AI-powered resume screening and tracking system designed to streamline recruitment via resume–job-description matching, keyword extraction, and candidate profiling.

---

## 📌 Project Overview

This system lets recruiters or job-seekers upload a job description plus a resume (PDF/DOCX). Leveraging Gemini Pro Vision, it parses the document, calculates a match score, identifies missing keywords, and generates a concise candidate summary. It supports efficient application tracking and helps both recruiters and applicants optimise their profiles for relevant roles.
([IJRASET][1])

---

## 🧰 Tech Stack

* **Language:** Python
* **Libraries/Tools:** `google-generativeai`, `PyPDF2`, `docx2txt`, `Streamlit`, `python-dotenv`
* **Model/Service:** Google Gemini Pro Vision (multimodal: text, PDF, images)
* **Environment:** Jupyter Notebook / Google Colab / Web App

---

## 🔄 Workflow Summary

### 1. Input & Upload

* Upload a **Job Description** (text)
* Upload a **Resume** in PDF or DOCX
* Extract text from resume via PyPDF2/docx2txt

### 2. Prompting & Model Inference

* Construct prompt template:

  ```
  As an ATS analyst, given the resume: {resume_text} and job description: {job_desc},  
  provide a JSON string: {"Match%": "...", "Missing Keywords": "...", "Candidate Summary": "..."}
  ```
* Send prompt (and resume data) to Gemini Pro Vision API
* Receive response: match score, keyword gaps, summary

### 3. Results & Dashboard

* Display match percentage
* List of missing keywords from job description
* Short candidate summary (experience, skills, fit)
* Option to track application status (applied, shortlisted, rejected)

### 4. Application Tracking Features

* Maintain list of applications with metadata: role, date, match score
* Filter/sort by score, status, keywords
* Export or download report of applications

---

## 📁 Project Structure

```
Resume-ATS-Gemini-Pro/
│── data/
│   └── samples/
│── notebooks/
│   └── prototype.ipynb
│── src/
│   ├── app.py
│   ├── resume_parser.py
│   ├── gemini_interface.py
│   └── tracker.py
│── README.md
│── requirements.txt
```

---

## 📈 Key Findings

* Gemini Pro enables extraction of contextual info (skills, experience) from diverse resume layouts, improving automation. ([Academia][2])
* Matching percentage + missing keywords metric provides actionable feedback to candidates and quick filtering for recruiters.
* Streamlit UI delivers a simple interface that bridges the gap between AI and everyday HR workflows.

---

## 🚀 Future Improvements

* Add **bulk upload** support (hundreds/thousands of resumes) and batch scoring.
* Integrate **long-context Gemini/vision** for scanned images of resumes or non-text formats.
* Expand tracking dashboard: analytics on match scores over time, role-fit clustering, recruiter feedback loop.
* Add **bias/fairness checks**: ensure under-represented candidates are not penalised by keyword-only matching.
* Deploy mobile/web interface where applicants get instant feedback & improvement suggestions.

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
