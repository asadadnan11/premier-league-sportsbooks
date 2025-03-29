# ⚽️ Premier League Betting Prediction using Random Forest

## 📚 Project Overview
This project leverages a **Random Forest classification model** to predict the outcomes (Win/Loss) of Premier League matches. The model uses historical match data from 2008 to 2025 and considers rolling performance metrics, betting odds, and head-to-head performance to generate predictions.

---

## 🎯 Goal
The objective is to develop a predictive model that assists in **betting decisions** by accurately forecasting match results. By incorporating rolling performance stats and adjusting for betting odds, the model aims to identify patterns that influence match outcomes.

---

## 📊 Dataset
### 📁 Data Source
- **Premier League Match Data (2008–2025)**
- The dataset consists of multiple CSV files merged to form a combined dataset with over **69,000 rows**.
- **Key Features:**
  - `HomeTeam`, `AwayTeam` – Teams playing the match.
  - `FTHG`, `FTAG` – Full-time home and away goals.
  - `B365H`, `B365D`, `B365A` – Bet365 odds for Home Win, Draw, and Away Win.
  - Rolling metrics of past 5 games for goals scored, goals conceded, and goal differences.

---

## 🧠 Model Details
### 🤖 Model Used
- **Random Forest Classifier**
- Number of Trees: **350**
- Variables Tried at Each Split (mtry): **6**
- Model tuned using **Grid Search Cross-Validation** to optimize accuracy.

---

## 🔥 Features and Methodology
### ⚙️ Feature Engineering
1. **Rolling Goals Metrics**:  
   - Rolling averages for goals scored and conceded by home and away teams in the last 5 games.
   - Rolling Goal Difference (Goal Differential over the last 5 games).
2. **Win Rate Calculation**:  
   - Home and Away win rates over the last 5 games.
3. **Betting Odds**:  
   - Bet365 odds for home win, draw, and away win included to factor in market expectations.
4. **Head-to-Head Performance**:  
   - Historical performance of teams against each other.
   
---

## 📈 Model Performance
### 🎯 Results (Without Draws)
- **Accuracy:** 82.65%  
- **Kappa Score:** 0.6414  
- **Sensitivity (Win):** 86.11%  
- **Specificity (Loss):** 77.78%  

---

## 🧩 Predictive Strategy
### 🎲 Interactive Betting Prediction
The project includes an **interactive prediction feature** where users can:
- Input home and away teams.
- Provide current betting odds.
- Get real-time match outcome predictions based on historical patterns.

---

## 📝 Key Insights
- The model shows strong performance in predicting wins and losses, with a **balanced accuracy of 81.94%**.
- Rolling goal difference and home/away performance contribute significantly to the prediction quality.
- Betting odds (Bet365) improve model stability by adding context to the outcome predictions.

---

## ⚡️ Next Steps
1. **Threshold Optimization:** Fine-tune probability thresholds to improve classification confidence.
2. **Feature Expansion:** Include player-level performance metrics and injury data.
3. **Live Data Integration:** Deploy model for real-time betting predictions using APIs.
4. **XGBoost Comparison:** Benchmark model performance against XGBoost and explore further gains.

---

## 📷 Preview
📄 [View the Model Results (HTML)](model_1.html)  

---

## 💡 Business Impact
- **Betting Strategy Optimization:** Helps improve betting decisions with data-driven predictions.
- **Identifying Value Bets:** Detects games where odds may not reflect true probabilities, offering **value betting opportunities**.

---

## 👨‍💻 Author
**Asad Adnan**  
Master's in Business Analytics, University of Notre Dame  
*Passionate about applying machine learning to sports analytics and predictive modeling.*




