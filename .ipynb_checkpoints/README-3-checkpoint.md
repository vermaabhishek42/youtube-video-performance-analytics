# YouTube Video Performance Analysis

## 📌 Project Overview

This project analyzes YouTube video performance using Exploratory Data
Analysis (EDA) and Machine Learning.\
The goal is to **identify key factors that drive video engagement and
predict video view counts**.

------------------------------------------------------------------------

## 📁 Dataset

The dataset includes the following key features:

-   `view_count`
-   `like_count`
-   `comment_count`
-   `duration_seconds`
-   `engagement_rate`
-   `likes_to_views_ratio`
-   `comments_to_views_ratio`
-   `video_age_days`

All preprocessing, visualization, and modeling steps were performed in
the Jupyter notebook.

------------------------------------------------------------------------

## 🧹 Data Preprocessing

Steps included:

1.  **Handling missing values**\
2.  **Converting `published_at` to datetime**\
3.  **Dropping useless columns like `favorite_count`**\
4.  **Creating derived columns**
    -   `duration_seconds`
    -   `video_age_days`
    -   `engagement_rate`
5.  Filtering numerical features for analysis and modeling

------------------------------------------------------------------------

## 📊 Exploratory Data Analysis (EDA)

The following visualizations were created:

### ✔ Distribution Plots

-   View Count Distribution\
-   Like Count Distribution\
-   Comment Count Distribution\
-   Duration Distribution

### ✔ Scatter Plots (Relationship Analysis)

-   Views vs Likes\
-   Views vs Comments\
-   Likes vs Comments\
-   Duration vs Engagement Rate (Log Scale)

### ✔ Correlation Heatmap

A full correlation matrix revealed: - Strong correlation: **views ↔
likes** - Moderate: **comments ↔ engagement rate** - Very weak:
**duration/age ↔ views**

------------------------------------------------------------------------

## 🤖 Machine Learning Model

A **Random Forest Regressor** was trained to predict `view_count`.

### Features used:

-   `like_count`
-   `engagement_rate`
-   `likes_to_views_ratio`
-   `duration_seconds`
-   `comments_to_views_ratio`
-   `video_age_days`
-   `comment_count`

### Model Metrics:

-   **R² Score:** \~0.79\
-   **RMSE:** \~17 million views

This indicates the model captures most relationships but tends to
struggle with very high-view outliers.

------------------------------------------------------------------------

## ⭐ Feature Importance (Random Forest)

Top predictors of view count:

1.  **like_count** (dominant feature)
2.  **engagement_rate**
3.  **likes_to_views_ratio**

Duration, age, and comment count contribute very little.

------------------------------------------------------------------------

## 🔮 Prediction Distribution (Actual vs Predicted)

A scatter plot of predicted vs actual view counts showed:

-   Good alignment for **low--mid view ranges**
-   Large variance for videos above **100M views** (outliers)

------------------------------------------------------------------------

## 📦 Output Files

The project generates the following:

-   Figures saved in: `reports/figures/`
-   Trained model predictions
-   PPT slides (optional)

------------------------------------------------------------------------

## 🚀 Conclusion

This analysis shows:

-   **Likes are the strongest predictor** of view count
-   Engagement-related metrics matter more than metadata like category
    or duration.\
-   Random Forest performs well but can't fully capture extreme viral
    outliers.

------------------------------------------------------------------------

