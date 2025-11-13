# 🧮 Text to SQL LLM App – Querying SQL Database using Gemini Pro

A generative-AI project that transforms natural-language queries into SQL statements and executes them on a relational database using Gemini Pro as the language model.

---

## 📌 Project Overview

This project creates a pipeline where users can input a plain-English query (e.g., “Show me the top 10 customers by revenue last month”), the system uses Gemini Pro to generate a corresponding SQL query, executes it on a connected database, and returns the result in a user-friendly format.
It enables effortless data access for non-technical users and supports business-intelligence workflows.

---

## 🧰 Tech Stack

* **Language:** Python
* **Libraries:** `google-generativeai`, `sqlalchemy`, `pandas`, `streamlit` (or similar UI), `dotenv`
* **Model:** Gemini Pro via Google Cloud / Vertex AI or API endpoint
* **Environment:** Jupyter Notebook / Google Colab / Web App

---

## 🔄 Workflow Summary

### 1. Natural-Language Input

* User enters a question about data (e.g., “Which products had sales over $50k in March?”).
* The system parses or sanitises the question (optional).

### 2. Prompting & SQL Generation

* Construct a prompt containing schema information and the user’s query:

  ```text
  You are a SQL expert. Given the following database schema:

  Table: sales  
    - order_id (int)  
    - product_id (int)  
    - revenue (float)  
    - sales_date (date)  
  Table: products  
    - product_id (int)  
    - product_name (string)  

  Generate a valid SQL query to answer the user’s question: "{user_query}"
  ```
* Send prompt to Gemini Pro and receive generated SQL statement.

### 3. SQL Execution

* Use `sqlalchemy` to connect to the database (e.g., SQLite/MySQL/PostgreSQL).
* Execute the generated query and fetch results.
* Convert results into a `pandas` DataFrame for display.

### 4. Results Display

* Present the DataFrame or visualisation in Streamlit/app UI.
* Also show the generated SQL query for transparency.
* Provide error-handling if the query fails or schema mismatch occurs.

---

## 📁 Project Structure

```
Text-to-SQL-LLM-App-Gemini-Pro/
│── data/
│   └── sample_db.sqlite
│── notebooks/
│   └── app_demo.ipynb
│── src/
│   ├── app.py
│   ├── gemini_interface.py
│   ├── sql_executor.py
│   └── utils.py
│── README.md
│── requirements.txt
```

---

## 📈 Key Findings

* Gemini Pro effectively translated natural-language queries into syntactically correct SQL statements when prompted with schema context.
* Including schema definition and explicit instructions in the prompt significantly improved accuracy of the generated SQL.
* UI feedback (showing the SQL query and result) enhances user trust and transparency.
* The system lowers the barrier for non-technical users to query relational databases using plain language.

---

## 🚀 Future Improvements

* Add support for larger schemas (multiple tables, joins, aggregations, sub-queries).
* Introduce natural-language follow-ups (e.g., “Now filter by region = ‘Asia’”) and context tracking.
* Include schema introspection and automatic schema-extraction to build prompt dynamically.
* Add query safety checks (SQL injection prevention, cost estimation) before executing generated queries.
* Deploy as SaaS/web-service with user-authentication and query logging for enterprise usage.

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
