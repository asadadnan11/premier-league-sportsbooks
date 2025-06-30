# Premier League Betting Prediction using Random Forest

## Project Overview
This project was developed as part of my **Business Analytics coursework** at Notre Dame, focusing on applying machine learning techniques to real-world business problems. Using a **Random Forest classification model**, I focused specifically on **predicting home team wins** in Premier League matches, leveraging the well-documented home advantage phenomenon. This targeted approach allowed for higher accuracy than trying to predict all possible outcomes, while exploring practical applications in sports betting markets.

---

## Goal & Learning Objectives
The primary goal was to **apply machine learning concepts** from coursework to a real-world problem with measurable business value. Rather than attempting to predict all match outcomes, I strategically focused on **home team wins only** - a binary classification problem that leverages football's inherent home advantage. This approach taught me the importance of problem framing and how narrowing scope can often lead to better, more actionable results.

---

## Dataset
### Data Source
- **Premier League Match Data (2008–2025)**
- The dataset consists of multiple CSV files merged to form a combined dataset with over **69,000 rows**.
- **Key Features:**
  - `HomeTeam`, `AwayTeam` – Teams playing the match.
  - `FTHG`, `FTAG` – Full-time home and away goals.
  - `B365H`, `B365D`, `B365A` – Bet365 odds for Home Win, Draw, and Away Win.
  - Rolling metrics of past 5 games for goals scored, goals conceded, and goal differences.

---

## Model Details
### Model Used
- **Random Forest Classifier**
- Number of Trees: **350**
- Variables Tried at Each Split (mtry): **6**
- Model tuned using **Grid Search Cross-Validation** to optimize accuracy.

---

## Features and Methodology
### Feature Engineering
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

## Model Performance
### Results (Home Team Win Prediction)
- **Accuracy:** 82.65%  
- **Kappa Score:** 0.6414  
- **Sensitivity (Home Win):** 86.11%  
- **Specificity (Not Home Win):** 77.78%  

### **Why This Performance Makes Sense**
Achieving 82.65% accuracy for home wins is realistic because:
- **Home advantage is real** - Premier League home teams win ~46% of matches historically
- **Binary classification** is simpler than predicting all outcomes (win/draw/loss)
- **Rich feature set** includes form, odds, and head-to-head data
- This performance translates to significant value in betting markets where **52.4%+ accuracy is profitable**  

---

## Predictive Strategy
### Home Win Prediction Focus
The model specifically predicts **"Will the home team win?"** which offers several advantages:
- **Higher accuracy** than trying to predict all outcomes (win/draw/loss)
- **Clearer betting strategy** - focus on home win markets only
- **Leverages home advantage** - a documented phenomenon in football
- Takes team form, historical matchups, and current betting odds to generate probability of home victory

---

## Key Insights & Learning Outcomes
- **Strategic Problem Framing**: Focusing on home wins rather than all outcomes led to higher accuracy and clearer business value - sometimes **narrowing scope improves results**.
- **Home Advantage Quantified**: The model confirmed that home advantage is measurable and predictable, with recent form being the strongest predictor beyond historical matchups.
- **Feature Engineering Impact**: Rolling goal difference and recent win rates proved most predictive, showing that **momentum matters more than season-long averages**.
- **Market Efficiency**: Incorporating betting odds improved model stability, suggesting bookmakers capture information that raw statistics miss.
- **Data Quality Reality**: Handling missing values and inconsistent team names across 17 seasons taught me practical skills that classroom exercises don't cover.

---

## Challenges & Limitations
### What I Learned the Hard Way
- **Overfitting Risks**: Early models achieved perfect training accuracy but dropped to ~70% on validation sets - a crucial lesson in the bias-variance tradeoff.
- **Temporal Dependencies**: Sports data has inherent time-series properties that standard cross-validation doesn't handle well.
- **External Factors**: The model struggles with unpredictable events (injuries, red cards, weather) that significantly impact outcomes but aren't captured in historical stats.
- **Sample Size Issues**: Some team matchup combinations have limited historical data, making reliable predictions challenging.

---

## What I'd Do Differently / Next Steps
1. **Time Series Approach:** Implement proper time-series cross-validation to better handle temporal dependencies.
2. **Ensemble Methods:** Compare Random Forest against XGBoost and potentially ensemble multiple models.
3. **Feature Engineering:** Explore player-level metrics and injury data if accessible.
4. **Economic Analysis:** Build a simulation to test actual betting profitability over time, not just accuracy metrics.
5. **Real-World Testing:** Validate predictions against actual matches in the current season (without real money, obviously!).

---

## Preview
[View the Model Results (HTML)](model_1.html)  

---

## Business Learning & Applications
- **Analytics in High-Stakes Environments:** This project taught me how to evaluate model performance when the cost of being wrong is real money.
- **Market Dynamics:** Learned how efficient markets (betting) incorporate information, and where analytical approaches might find edge cases.
- **Risk Management:** Understanding that even a "good" model needs proper bankroll management and risk controls in practice.
- **Stakeholder Communication:** How to explain technical results to non-technical decision makers who care about ROI, not R-squared.

---

## Author
**Asad Adnan**  
Master's in Business Analytics, University of Notre Dame  
*Passionate about applying machine learning to sports analytics and predictive modeling.*




