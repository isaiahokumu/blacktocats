# AI-Powered Nutrition Coach

### Problem Statement
Poor dietary habits and inadequate nutrition tracking has contributed to a significant rise in the rates of obesity, diabetes, hypertension and other lifestyle-related diseases. While there are many nutrition apps that exist, most of them often fail to personalize recommendations based on a user’s specific health conditions, cultural preferences and real-time dietary behavior.

Moreover, manual food logging is tedious which has led to low user engagement and inaccurate records. This tends to create a gap in the ability to proactively guide individuals toward optimal nutrition choices using AI, real-time APIs and intuitive user interfaces.

This project aims to develop an AI-powered nutrition coach that integrates voice-based food logging, personalized meal planning, and nutrient tracking through python modules to improve health outcomes through data-driven dietary recommendations.

An AI-powered nutrition coach that:
- Suggests **personalized meal plans** based on user health conditions, goals, and preferences.
- Retrieves **nutrition facts and recipes** from APIs.
- Supports **speech-to-text** food logging for quick entry.
- Tracks **daily nutrient intake** with visual dashboards.
- Uses **AI logic** to fill nutritional gaps and give recommendations.

---

## Features
1. **User Profile Setup**
   - Age, gender, weight, height, activity level
   - Health conditions (e.g., diabetes, hypertension)
   - Dietary preferences (vegan, gluten-free, low-carb)

2. **Daily Meal Plan Generator**
   - Pulls recipes from **Edamam API**
   - Balances macros and calories
   - Adjusts for health conditions (e.g., low sodium for hypertension)

3. **Speech-to-Text Food Logging**
   - "I ate 2 boiled eggs and a banana" → **Nutrition breakdown**
   - Uses **USDA API** for nutrition details

4. **Progress Dashboard**
   - Track calories, macros, vitamins
   - Charts of deficiencies and excesses

5. **AI-Powered Recommendations**
   - Suggest recipes to close nutrient gaps
   - Personalized health and lifestyle tips

---

## Tech Stack
- **Frontend:** Streamlit (quick dashboard)
- **Backend:** FastAPI (Python)
- **Database:** MySQL (user profiles, logs)
- **APIs:**
  - [Edamam Recipe Search API](https://developer.edamam.com/)
  - [USDA FoodData Central API](https://fdc.nal.usda.gov/api-key-signup.html)
  - [Google Speech-to-Text API](https://cloud.google.com/speech-to-text)
  - (Optional) OpenAI API for advanced personalization
- **Visualization:** Plotly
- **Deployment:** Docker + Vercel/Cloud Run

---

## Project Structure
nutrition_coach/
│── app/
│ └── main.py # FastAPI backend
│── utils/
│ └── tts.py # Text-to-speech helper
│── streamlit_app.py # Frontend UI
│── requirements.txt # Python dependencies
│── .env.example # API keys template
│── Dockerfile.backend # Backend Dockerfile
│── docker-compose.yml # Multi-container setup
│── README.md # Documentation
│── LICENSE

---

## Setup & Installation

### Clone the Repository
```bash
git clone https://github.com/yourusername/nutrition_coach.git
cd nutrition_coach

pip install -r requirements.txt

uvicorn app.main:app --reload

streamlit run streamlit_app.py

docker-compose up --build
