# 📰 News Reporter AI Agent Using CrewAI

A generative-AI project focused on automating a virtual news-desk crew that autonomously researches, drafts, and publishes news content using CrewAI’s multi-agent framework.

---

## 📌 Project Overview

This project builds a system of interconnected agents — each assigned a specialized role (e.g., researcher, writer, editor, publisher) — to streamline the news-reporting workflow from source discovery to article publication. Using CrewAI, the agents collaborate and orchestrate tasks such as scanning news feeds, drafting articles, reviewing output, and publishing to web platforms. The goal is to deploy an autonomous “news-team” that produces timely, coherent, and topic-relevant content with minimal manual intervention.

---

## 🧰 Tech Stack

* **Language:** Python
* **Libraries & Frameworks:** CrewAI (agent orchestration), LangChain or similar for tool integration, web-scraping tools (RSS feeds, APIs), publishing tools (Medium API, blog CMS)
* **Environment:** Jupyter Notebook / Google Colab / Cloud
* **Modeling:** Large Language Models (LLMs) for generation, supported by retrieval/search tools for sourcing content

---

## 🔄 Workflow Summary

### 1. Source Collection & Monitoring

* Agents ingest news content via RSS feeds, APIs or search tools.
* Filter and prioritise articles based on topic relevance, freshness and source credibility.

### 2. Content Drafting

* The “Reporter” agent synthesises content from collected sources, constructs draft articles focused on the target topic.
* Ensures logical structure, coherence and fact-based narrative.

### 3. Review & Editing

* An “Editor” agent reviews the draft for tone, clarity, accuracy and formatting.
* Applies guardrails: citation integrity, neutrality, readability.

### 4. Publishing

* The “Publisher” agent uploads the article to the selected platform (e.g., Medium, blog) via API, formats properly for web.
* Optionally triggers social-media posting or newsletter distribution.

### 5. Feedback & Iteration

* Capture metrics: article engagement, publishing latency, revision count.
* Agents refine prompts, tools and workflows based on feedback loops for continuous improvement.

---

## 📁 Project Structure

```
News-Reporter-AI-Agent-CrewAI/
│── data/
│   └── sources/
│── notebooks/
│   └── pipeline.ipynb
│── src/
│   ├── agents.py
│   ├── tasks.py
│   └── tools.py
│── requirements.txt
│── README.md
```

---

## 📈 Key Findings

* Agent orchestration via CrewAI enables modular design: each role (researcher, writer, editor) encapsulated separately, improving maintainability and clarity.
* Prompt design and task definition (via YAML/agent config) critically influence output quality and workflow robustness.
* Reliable source filtering and retrieval ensure the generated content stays current and credible.
* System demonstrates how generative AI can automate end-to-end content production, although human review may still be beneficial for high-stakes publishing.

---

## 🚀 Future Improvements

* Integrate multimedia elements (images, video clips) — e.g., automatically generate featured image or video summary.
* Expand platform outputs: auto-social posting, email newsletters, RSS feed generation.
* Implement advanced monitoring and analytics: track article performance, user engagement, and feed next-cycle improvements.
* Introduce user-interactive input: let end-users specify topics, tone, style and have the agent crew tailor output accordingly.
* Add fallback/human-in-loop mechanisms and audit logs for production-grade reliability (safe-guards against hallucinations).

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
