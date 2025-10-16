# 🍷 Wine Quality — Classification & Regression

> Final exam notebook for *Introduction to Data Science & Machine Learning*, HEC Paris — **41/40** (extra credit).

**📓 Notebook:** [`wine-quality-classification-regression.ipynb`](./wine-quality-classification-regression.ipynb)
**🛠️ Tools:** Python, pandas, seaborn, matplotlib, scikit-learn

---

## 📋 Context

This notebook is the practical part of a final exam covering supervised learning fundamentals: exploratory data analysis, classification, regression, and model evaluation. The dataset contains physicochemical measurements for white wines (volatile acidity, citric acid, sulfur dioxide, density, pH, sulphates, alcohol %) along with a quality score and a binary `sweet` label.

Several exercises were given as **screenshots of code and output** rather than executable cells — the task was to read, interpret, and critique someone else's model output without running it, which is reflected in the notebook's markdown answers.

---

## 🔍 What the notebook covers

### Part A — Exploratory data analysis
- Compared wine quality scores between sweet and non-sweet wines (descriptive stats, bar chart, crosstab)
- Identified a strong class imbalance in the dataset (85 sweet wines vs. 4,813 non-sweet)
- Investigated the correlation between alcohol content and density, including outlier handling

### Part B — Classification (predicting whether a wine is sweet)
- Train/test split (70/30) with a fixed random state for reproducibility
- **KNN classifier** tested at several values of K (21, 3, 115)
- **Logistic regression** tested with the default decision threshold (0.5) and an adjusted threshold (0.05)
- Diagnosed a classic pitfall: a 98% accuracy model that was in fact *no better than always predicting the majority class*, by comparing accuracy to the actual class distribution and inspecting the confusion matrix
- Reasoned through — without executing — what a KNN model would output given the class balance of the training set (K=115 with only 57 positive examples in training)

### Part C — Regression (predicting alcohol %)
- **OLS linear regression**, evaluated with RMSE against the baseline standard deviation
- Applied the same approach to a filtered subset (sweet wines only) and compared performance
- **KNN regression** with cross-validation across a range of K values to find the optimal K, reading the classic U-shaped bias-variance tradeoff curve (RMSE minimized at K=20)
- Compared OLS vs. KNN regression performance and discussed why results aren't directly comparable without matching evaluation methodology (cross-validation vs. single split)

---

## 🎯 Skills demonstrated

- Supervised learning: classification (KNN, logistic regression) and regression (OLS, KNN regression)
- Model evaluation: accuracy, confusion matrix, RMSE vs. standard deviation baseline
- Recognizing and diagnosing **imbalanced-data pitfalls** (misleading accuracy)
- Bias-variance tradeoff and overfitting/underfitting through hyperparameter (K) tuning
- Cross-validation for model selection
- Reproducibility practices (train/test split, fixed random state)
- Reading, interpreting, and critiquing model code and output — including reasoning about expected results before execution

---

## 📄 License

Academic work, shared for portfolio purposes.
