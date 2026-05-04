# 🎮 What Makes a Video Game a "Top-Seller"?

A machine learning analysis predicting commercial success in the global video game market using sales data, critic scores, and platform metadata.

> **Course:** ANA 630 – Advanced Analytic Applications | National University | May 2025

---

## 📋 Project Overview

The global video game industry generates hundreds of billions in annual revenue, yet many releases fail to achieve commercial success. This project investigates whether a predictive model can identify top-selling games using features available prior to or shortly after release — helping inform investment, marketing, and development decisions.

The outcome variable **Top_Seller_75** was engineered to classify games ranking in the top 25% of global sales.

---

## 🔍 Research Question

> Can we predict whether a video game will be a top seller based on pre-release and early post-release features such as platform, genre, publisher, and critic/user engagement?

---

## 📊 Dataset

| Detail | Info |
|---|---|
| **Source** | [Kaggle – Global Video Game Sales & Ratings](https://www.kaggle.com/datasets/thedevastator/global-video-game-sales-ratings) |
| **Original Size** | 16,000+ entries |
| **After Cleaning** | 6,825 observations |
| **Key Features** | Platform, genre, publisher, developer, critic/user scores, rating, year of release |
| **Target Variable** | Top_Seller_75 (top 25% of global sales = 1, all others = 0) |

---

## 🛠️ Methods

| Step | Detail |
|---|---|
| Data cleaning | Removed rows with excessive missing values; no imputation applied |
| Feature engineering | Engineered binary top-seller outcome variable |
| Train/test split | 80/20 |
| Validation | 5-fold cross-validation |
| Models | Logistic Regression, Random Forest |
| Tuning | GridSearchCV hyperparameter optimization |
| Evaluation | Accuracy, precision, recall, F1, ROC-AUC, confusion matrix |

**Tools:** Python (pandas, scikit-learn, seaborn, matplotlib)

---

## 📈 Key Findings

- Global video game sales were heavily right-skewed — most games sold modestly while a few blockbusters dominated the market
- **Action** was the most common genre overall, but **Misc, Shooter, and Sports** titles were disproportionately represented among top sellers
- Logistic regression achieved an AUC of **0.80**, providing a solid baseline
- Tuned Random Forest improved performance significantly, pushing the **F1 score closer to 0.75**
- Surprisingly, **user and critic engagement metrics** (User_Count, Critic_Score, Critic_Count) outranked genre, publisher, and platform as predictors — suggesting that reception matters more than category

---

## 📁 Repository Structure

```
├── README.md                  # Project overview (you're here!)
├── notebook/                  # Python analysis notebook
└── report/                    # Full written report (PDF)
```

> 🔗 Dataset available on [Kaggle](https://www.kaggle.com/datasets/thedevastator/global-video-game-sales-ratings)

---

## 🎓 Academic Context

**Course:** ANA 630 – Advanced Analytic Applications  
**Institution:** National University  
**Date:** May 2025
