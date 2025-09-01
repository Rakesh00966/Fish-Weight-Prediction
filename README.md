# 🎣 Fish Weight Prediction using Regression

## 📌 Project Overview
This project focuses on predicting the **weight of fishes** based on their physical characteristics.  
The dataset contains measurements of different fish species such as **Bream, Roach, Whitefish, Parkki, Perch, Pike, and Smelt**.  

We explore the dataset through **EDA (Exploratory Data Analysis)**, handle skewness and outliers, analyze feature relationships, and finally build a **regression model** to predict fish weight.

---

## 📂 Dataset
The dataset consists of **159 rows × 7 columns**:

- **Species**: Fish type (categorical)
- **Weight**: Weight of the fish in grams (target variable)
- **Length1**: Vertical length (cm)
- **Length2**: Diagonal length (cm)
- **Length3**: Cross length (cm)
- **Height**: Height of the fish (cm)
- **Width**: Diagonal width/thickness (cm)

---

## 🔎 Exploratory Data Analysis (EDA)

1. **Distribution Check**
   - Weight column is **right skewed** with presence of outliers.
   - Other features are slightly skewed but closer to normal distribution.

2. **Correlation**
   - Strong correlation between Weight and Length features (`~0.91+`).
   - High inter-correlation among Length1, Length2, and Length3.
   - Height and Width also show moderate correlation with Weight.

3. **Species Distribution**
   - Most fish samples are **Perch**.
   - Smelt has the least number of samples.

---

## 📊 Visualizations
- **Histograms** → Distribution and skewness of numerical features.
- **Scatter Plots** → Show strong positive relationship between fish length and weight.
- **Box Plots & Swarm Plots** → Species-wise weight distributions.
- **Heatmap** → Feature correlation matrix.

---

## 🛠️ Data Preprocessing
- No missing values found.
- Encoded `Species` column using **Label Encoding**.
- Tested feature reduction:
  - Length features are highly correlated → tried dropping redundant ones.

---

## 🤖 Model Building
- **Algorithm**: Linear Regression
- **Train-Test Split**: 80/20

### 📌 Model Performance:
- **R² Score**: ~0.90  
- **RMSE**: ~117 grams  

Even after removing highly correlated features (e.g., `Length1`), model performance remained almost the same.

---

## ✅ Conclusion
- Fish weight can be predicted with **~90% accuracy** using physical measurements.
- Strongest predictors: **Length (1,2,3)** and **Width**.
- Outliers and skewness in weight affect predictions slightly, but overall performance is strong.
- Possible improvements:
  - Try **log transformation** of Weight.
  - Experiment with **non-linear models** (Random Forest, XGBoost).

---

## 📌 Tech Stack
- **Python**
- **Pandas, NumPy**
- **Matplotlib, Seaborn**
- **Scikit-learn**
- **Statsmodels**

---

## 🚀 Future Work
- Apply feature engineering to handle correlated variables.
- Compare with advanced regression models.
- Build an interactive dashboard to visualize fish characteristics.


