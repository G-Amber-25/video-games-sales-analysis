# 🎮 What Makes a Video Game a "Top-Seller"?
A machine learning analysis predicting commercial success in the global video game market using sales data, critic scores, and platform metadata.

Course: ANA 630 - Advanced Analytic Applications | National University | May 2025


## 📋 Project Overview
The global video game industry generates hundreds of billions in annual revenue, yet many releases fail to achieve commercial success. This project investigates whether a predictive model can identify top-selling games using features available prior to or shortly after release, helping inform investment, marketing, and development decisions.
The outcome variable Top_Seller_75 was engineered to classify games ranking in the top 25% of global sales.

## 🔍 Research Question

Can we predict whether a video game will be a top seller based on pre-release and early post-release features such as platform, genre, publisher, and critic/user engagement?


## 📊 Dataset
| Detail | Info |
|---|---|
| **Source** | Kaggle – Global Video Game Sales & Ratings |
| **Original Size** | 16,719 entries |
| **After Cleaning** | 6,825 observations |
| **Key Features** | Platform, genre, publisher, developer, critic/user scores, rating, year of release |
| **Target Variable** | Top_Seller_75 (top 25% of global sales = 1, all others = 0) |

| Step | Detail |
|---|---|
| Data cleaning | Removed rows with missing values; no imputation applied |
| Feature engineering | Engineered binary top-seller outcome variable |
| Train/test split | 80/20 |
| Validation | 5-fold cross-validation |
| Models | Logistic Regression, Random Forest |
| Tuning | GridSearchCV (best params: max_depth=10, n_estimators=300) |
| Evaluation | Accuracy, precision, recall, F1, ROC-AUC, confusion matrix |

## 📈 Key Findings

Global video game sales were heavily right-skewed. Most games sold modestly while a few blockbusters dominated the market.
Action was the most common genre overall (1,630 titles), but Misc, Shooter, and Sports had the highest top-seller hit rates at approximately 32%, 30%, and 28% respectively, meaning a larger share of games in those genres qualified as top sellers.
Logistic regression achieved an AUC of 0.80, providing a solid baseline, though precision for identifying top sellers was approximately 0.50 with recall around 0.70, indicating the model caught real top sellers but also produced notable false positives.
The tuned Random Forest improved performance substantially, achieving an F1 score of 0.69 for the top seller class and a weighted F1 of 0.84, with both precision and recall for top sellers reaching 0.69.
Surprisingly, user and critic engagement metrics (User_Count, Critic_Score, Critic_Count) outranked genre, publisher, and platform as predictors, suggesting that reception matters more than category.

## 📊 Visuals
<img width="555" height="312" alt="video game histogram" src="https://github.com/user-attachments/assets/793bd195-d493-4795-ae81-17fa3d485f53" />
<img width="528" height="308" alt="top sellers proportion" src="https://github.com/user-attachments/assets/fa8db469-5bf5-43b9-9a23-695c7c82d93d" />
<img width="536" height="299" alt="roc curve" src="https://github.com/user-attachments/assets/58dc14cb-352d-43cc-8b09-16e1d6582c0d" />
<img width="416" height="364" alt="confusion" src="https://github.com/user-attachments/assets/07938f1e-3db4-4d8d-a0f2-1c7c5c139233" />
<img width="624" height="355" alt="feature importance" src="https://github.com/user-attachments/assets/af1fa7b2-00ab-4b0a-b229-caa02861f059" />


## 📁 Repository Structure
```
├── README.md                              # Project overview
├── video_game_topseller_analysis.ipynb    # Python analysis notebook
└── video_game_sales_analysis_report.pdf   # Full written report (PDF)

```

🔗 Dataset available on Kaggle <https://www.kaggle.com/datasets/sidtwr/videogames-sales-dataset?select=Video_Games_Sales_as_at_22_Dec_2016.csv>


## 🎓 Academic Context
Course: ANA 630 – Advanced Analytic Applications
Institution: National University
Date: May 2025
