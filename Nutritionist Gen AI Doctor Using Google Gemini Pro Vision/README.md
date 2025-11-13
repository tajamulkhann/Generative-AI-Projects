# 🍎 Nutritionist Gen AI Doctor Using Google Gemini Pro Vision

An AI-powered nutrition assistance system that uses the Gemini Pro Vision multimodal model to analyse food images, assess nutritional content, and provide tailored dietary recommendations.

---

## 📌 Project Overview

This project builds a complete workflow for a generative AI nutrition assistant: image ingestion (meal photos), visual analysis via Gemini Pro Vision, nutritional feature extraction (calories, macronutrients, micronutrients), and user-friendly diet insights. The objective is to enable users (or nutritionists) to capture a meal image and receive a detailed nutrition report and health assessment.

---

## 🧰 Tech Stack

* **Language:** Python
* **Libraries/Tools:** `google-generativeai`, PIL or OpenCV, Streamlit (or similar for UI)
* **Model:** Gemini Pro Vision (for multimodal image + text inference)
* **Environment:** Jupyter Notebook / Google Colab / Web App

---

## 🔄 Workflow Summary

### 1. Data Collection & Image Input

* Users upload or capture food-dish images (JPEG/PNG).
* Input images are pre-processed (resize, normalise) before model inference.

### 2. Prompt Engineering & Model Inference

* A system prompt directs Gemini Pro Vision to behave as an expert nutritionist, e.g:

  ```
  You are a certified nutritionist. The image shows a meal. For each item in the image, estimate calories, macronutrient breakdown (carbs, proteins, fats), and total calories. Then provide whether the meal is balanced/healthy, and suggest one improvement or healthier alternative if needed.
  ```
* The processed image and prompt are both sent to the model via the API.
* The model returns structured textual output (itemised nutrition + summary insights).

### 3. Result Presentation & Insights

* The output is parsed and displayed in the UI: food items, calories, nutrient ratios, health assessment.
* Additional features:

  * Overall health rating of the meal
  * Dietary recommendation: e.g., portion adjustment, substitution suggestions
  * Historical tracking or meal-log export (optional)

### 4. User Interface

* Simple UI (Streamlit or Web) for image upload + “Analyse Meal” button.
* Display uploaded image + model output in reader-friendly format (tables, bullets).
* Optional export or log of nutrition report.

---

## 📁 Project Structure

```
Nutritionist-GenAI-Doctor-Gemini-Pro-Vision/
│── data/
│   └── sample_meals/
│── notebooks/
│   └── meal_analysis_pipeline.ipynb
│── src/
│   ├── app.py
│   ├── image_processor.py
│   └── nutrition_model_interface.py
│── README.md
│── requirements.txt
```

---

## 📈 Key Findings

* Gemini Pro Vision’s multimodal capabilities allow analysis of meal images to estimate calories and nutrient composition. ([app.readytensor.ai][1])
* Prompt quality (clear instructions to the model) strongly affects the accuracy of the nutrition outputs. ([Medium][2])
* Real-time image-based nutrition feedback supports user engagement and can assist in diet planning, portion control, and healthier meal choices.

---

## 🚀 Future Improvements

* Expand into meal-planning mode: given user diet goals (weight loss, muscle gain, maintenance), suggest meals and dietary schedule.
* Add food-recognition robustification: handle multiple dishes, ingredient breakdown, portion size estimation via depth/size cues.
* Introduce longitudinal tracking: users can log meals over time and visualise nutrition trends.
* Deploy to mobile (iOS/Android) for on-the-go meal scanning.
* Integrate external nutrient databases and user dietary restrictions (allergies, vegan, low-carb) to personalise suggestions.

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
