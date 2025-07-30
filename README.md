# MENU-Generator
Hashira HACKATHON , custom menu generator application
# 🍽️ AI Menu Recommender - Weekly Smart Meal Planner

> 🧠 A smart, full-stack AI-powered application that dynamically generates *unique, calorie-balanced, and popularity-optimized meal combos* for every day of the week — built to resemble a luxurious restaurant menu.

---

## 🚀 Project Overview

This AI-driven application automatically recommends **3 unique meal combos per day** (for 7 days) from a curated dataset of food items. Each combo includes a **main course, side dish, and a drink**, intelligently matched based on:

- 🔥 **Calorie range** (550–800 kcal)
- ⭐ **Average popularity score**
- 🎨 **Taste profile alignment** (spicy, sweet, savory, or mixed)
- 🔁 **Non-repetition of items or combos across recent days**

All recommendations are presented with a clean and elegant **restaurant-style UI**, making the app intuitive, engaging, and suitable for practical deployment in food-tech, cafeterias, or fitness-focused meal planning.

---

## 🧠 Core Logic

1. **Input Data**  
   The dataset (`AI_Menu_Recommender_Items.csv`) includes food items with:
   - Category: `main`, `side`, `drink`
   - Calories
   - Taste profile: `spicy`, `sweet`, `savory`
   - Popularity score (0–1)

2. **Generation Rules**
   - For each of the 7 days, the app:
     - Selects 3 *unique* combos per day.
     - Ensures no item or combo is repeated within the last 3 days.
     - Total calories for each combo: **550–800 kcal**
     - Popularity scores across items: within ±0.1 of each other (for consistency)
     - Taste profiles are matched to day-based trends:
       - Monday/Friday → `savory`
       - Tuesday/Saturday → `sweet`
       - Wednesday → `spicy`
       - Thursday → `mix`
       - Sunday → `any` (free combination)

3. **Response Format**
   ```json
   {
     "combo_id": 1,
     "main": "Paneer Butter Masala",
     "side": "Garlic Naan",
     "drink": "Sweet Lassi",
     "total_calories": 760,
     "popularity_score": 0.85,
     "reasoning": "Savory and sweet profile fits Sunday trend. Popularity and calorie limits satisfied."
   }
💻 Tech Stack
Frontend	Backend	Tools/Data
ReactJS (HTML, CSS, JS)	FastAPI (Python)	Pandas, CSV Data
Elegant custom CSS UI	REST API (/menu_recommendation)	Taste-profiled dataset

🎨 UI Highlights
🍷 Luxurious & minimal design (restaurant-style layout)

📅 Day-wise cards with bold headers

🍛 Combos styled as fine-dine plates

📈 Details like total calories, popularity, and taste profile

🔁 Click Generate Menu to shuffle fresh combos every time

✨ Features
✅ 3 fresh meal combos per day
✅ Taste-profile-based reasoning for each combo
✅ No item repetition across week
✅ Daily uniqueness maintained
✅ Calorie-balanced and popularity-aware logic
✅ Fully responsive, elegant interface

