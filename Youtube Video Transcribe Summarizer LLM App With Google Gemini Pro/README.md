# 📹 YouTube Video Transcribe & Summarizer – LLM App with Gemini Pro

A generative‐AI project that enables users to input a YouTube video link, automatically extract the transcript, and use Gemini Pro to generate a structured summary of the content.

---

## 📌 Project Overview

This application builds an end-to-end workflow:

* Input a YouTube video URL.
* Extract or download the video’s transcript.
* Feed the transcript and user-prompt into Gemini Pro to generate a concise summary.
* Display the uploaded video thumbnail, the transcript (or key segments), and the generated summary for user review.
  The objective is to save users time by turning long video content into digestible summaries.

---

## 🧰 Tech Stack

* **Language:** Python
* **Libraries/Tools:** `youtube-transcript-api` (or equivalent), `google-generativeai` SDK, `Streamlit` or `Flask` for UI, `pandas` (optional for data handling)
* **Model:** Gemini Pro via Google Gen AI API
* **Environment:** Jupyter Notebook / Google Colab / Web App

---

## 🔄 Workflow Summary

### 1. Video Input & Transcript Extraction

* User enters a valid YouTube URL.
* The system extracts the video ID and uses a transcript library/API to fetch subtitles/transcript.
* Handles potential issues (no transcript available, auto-generated only, language options).

### 2. Prompt Construction & Model Inference

* Define a system prompt templating the behavior of the summarizer, e.g.:

  > “You are an expert summarizer. Given the transcript of a YouTube video, generate a summary that highlights the key points, structures the information in logical paragraphs, and does not add extraneous content.”
* Pass model input: [transcript text] + prompt to Gemini Pro.
* Retrieve output summary.

### 3. Presentation & UI

* Display video thumbnail (via `http://img.youtube.com/vi/{video_id}/0.jpg`).
* Show the generated summary and optionally the transcript or key bullet points.
* Provide UI input for users to add custom instruction/extra prompt (e.g., “Explain this as if for a beginner”).

---

## 📁 Project Structure

```
YouTube-Video-Transcriber-Summarizer/
│── data/
│   └── sample_videos/
│── notebooks/
│   └── summarizer_pipeline.ipynb
│── src/
│   ├── app.py
│   ├── transcript_extractor.py
│   ├── gemini_interface.py
│   └── ui.py
│── requirements.txt
│── README.md
```

---

## 📈 Key Findings

* Gemini Pro supports video understanding workflows when provided with transcripts or video input. ([Google AI for Developers][1])
* Quality of the summary strongly depends on the accuracy/completeness of the transcript and clarity of prompt instructions.
* Offering users a preview (video thumbnail + summary) improves usability and trust.

---

## 🚀 Future Improvements

* Extend to voice-only input: download audio, transcribe large segments, feed to model.
* Add question-answering interface on top: user can ask follow-up questions about the video.
* Support multiple languages: detect transcript language, translate content, summarise accordingly.
* Add export options: PDF summary, shareable link, or reading list.
* Deploy as mobile/web app with file upload, playback, and summary history.

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
