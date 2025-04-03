# 🏀 March Machine Learning Mania 2025 — NCAA Tournament Predictor

This project was developed for the [Kaggle March Machine Learning Mania 2025](https://www.kaggle.com/competitions/march-machine-learning-mania-2025/overview) competition.  
It focuses on analyzing the data to gain the best insights and building predictive models that estimate the probability of one NCAA basketball team defeating another during the tournament.

---

## 📦 About the Data

The data used in this project is provided and pre-cleaned by Kaggle as part of the official competition.  
It is structured into five major sections:

### 🔹 Section 1: Basics
- **Team Info**: Historical teams and seasons (`MTeams.csv`, `MSeasons.csv`)
- **Seedings**: NCAA Tournament seedings for each team (`MNCAATourneySeeds.csv`)
- **Compact Results**: Regular and tournament win/loss summaries

### 🔹 Section 2: Boxscores
- **Detailed match results**: Full box scores including rebounds, assists, steals, etc.
- Enables more granular statistical analysis of team and player performance

### 🔹 Section 3: Geography
- **Game locations**: City-level data for where each game occurred
- Useful for modeling potential home-court or travel distance effects

### 🔹 Section 4: Rankings
- **Massey Ordinals**: Over 40 ranking systems, including Sagarin, Pomeroy, AP, etc.
- These rankings are tracked throughout the season and are a rich source of features

### 🔹 Section 5: Supplements
- **Coaching records**: Including season-by-season coach names and changes
- **Conference affiliations**, **secondary tourneys**, and **tourney slots**
- Extra depth for modeling team consistency, stability, and historical performance

> ✅ All datasets are **cleaned and standardized** for direct use — no additional preprocessing is necessary to begin analysis.

---

## 🔍 EDA Highlights

- **Seeds & Upsets**: Lower seeds dominate overall, but most upsets occur between seeds 9–13.
- **Conference Trends**: Certain conferences consistently under- or over-perform their seedings.
- **Coach Analysis**: Coaches with more career wins and clutch success reach deeper rounds more often.
- **Ranking Systems**: Aggregated system rankings (e.g., AP, Sagarin) offer predictive insight into team strength.
- **Deep Runs**: Teams with a history of late-stage appearances may carry hidden value beyond their seed.

---

## 🧠 Modeling Approach

- Engineered features from:
  - Tournament history
  - Elo ratings & ranking systems
  - Seed difference, win margins, upset counts
  - Coaching experience and clutch performance
  - Boxscore aggregates (FG%, steals, blocks, etc.)
- Used **LightGBM** as the main classifier due to its speed and performance
- Trained on historical matchups and predicted probabilities for 2025 tournament games

---

## 📊 Evaluation

Submissions are evaluated using the **Brier score**, which measures the accuracy of predicted probabilities — the lower, the better.

🎯 Our best submission achieved a **Brier score of 0.126** on the men's bracket,  
beating the public benchmark with strong feature engineering and model design.

---

## 📁 Project Structure

| File | Description |
|------|-------------|
| `ncaa_eda.ipynb` | Exploratory Data Analysis, visuals, and insights |
| `ncaa_feature_engineering_and_model.ipynb` | Feature engineering and LightGBM modeling |
| `README.md` | This documentation file |

---

## 🙋‍♀️ About Us

This project was built by my amazing mate **Dylan** and me (Thao)!  
We absolutely loved exploring this dataset — from the richness of the historical records to the excitement of seeing data turn into real March Madness insights.

🏀💥 We hope this work scores a three-pointer for you too.

- [Thao on GitHub](https://github.com/thaochu05)
- [Dylan on GitHub](https://github.com/DucDuyLe)

---

## 🙏 Acknowledgments

We extend our gratitude to:
- **Kenneth Massey** for providing much of the historical ranking data
- **Jeff Sonas** of Sonas Consulting for his support in assembling the full competition dataset

And big thanks to the Kaggle competition organizers for making this incredible basketball dataset available to the public.
