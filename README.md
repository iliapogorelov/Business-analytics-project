# Predicting Online News Popularity Using Machine Learning

This project was completed as part of a Business Analytics course at university.  
The objective was to identify key factors influencing online news popularity and build a predictive model to classify articles as popular or non-popular.

##  Problem Statement

In digital media, predicting article popularity is crucial for optimizing content strategy.  
We aimed to:

- Identify which features influence article popularity (measured by number of shares)
- Build a classification model to predict whether a future article will be popular

Dataset: 39,797 online news articles  
Source: Fernandes et al. (2015)

---

##  Data Preprocessing

- Cleaned feature names
- Checked for missing values and duplicates
- Analyzed skewness and outliers in the target variable (`shares`)
- Used the **median** as a threshold to classify articles as popular vs non-popular

---

##  Feature Engineering

Since original features showed weak correlation with popularity, we created 5 engineered variables:

- `virality_score`
- `topic_specialization`
- `text_complexity`
- `sentiment_power`
- `seo_strength`

Among them, **topic_specialization** showed the strongest individual predictive performance.

---

##  Classification Models

Two models were implemented:

- Logistic Regression
- Random Forest (with GridSearchCV)

### Best Model: Random Forest
- Accuracy: **0.662**
- Better balance between class predictions
- Improved performance across precision, recall, F1-score

This moderate accuracy reflects the inherent difficulty of predicting article popularity.

---

##  Feature Importance

The most important feature was:

- `kw_avg_avg` (average popularity of keywords)

One engineered feature (`virality_score`) ranked within the top 10 most important features.

---

##  Clustering Analysis

We applied:

- Agglomerative Clustering (k = 3)
- PCA for visualization

Findings:
- Articles form natural clusters based on topic, sentiment, complexity, and SEO strength
- Popularity depends on combinations of features rather than a single variable

---

##  Key Insight

Online news popularity is inherently difficult to predict.  
No single feature strongly explains it, but combining:

- Feature engineering
- Supervised learning
- Unsupervised clustering

provides meaningful insight into content performance patterns.

---

##  Tools & Technologies

- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib / Seaborn
- GridSearchCV
- PCA
- Agglomerative Clustering

---

##  Repository Structure

- `Project_code.ipynb` — Full data analysis and modeling workflow
- `Project_report.pdf` — Complete written report

