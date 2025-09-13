Mushroom Classification (Edible vs Poisonous)

Overview This project predicts whether a mushroom is edible or poisonous using the Mushroom Dataset. It demonstrates an end-to-end ML workflow: preprocessing → EDA → feature engineering → multiple ML models → ensemble methods → ANN → model comparison.
2.Dataset Source: UCI Mushroom Dataset

Rows: 8124 samples Classes: Edible (51.8%) | Poisonous (48.2%) Features (22 categorical): cap-shape, cap-surface, cap-color, bruises, odor gill-attachment, gill-spacing, gill-size, gill-color stalk-shape, stalk-root, stalk-surface-above-ring, stalk-surface-below-ring veil-type, veil-color, ring-number, ring-type spore-print-color, population, habitat Target: class → edible or poisonous

Note: stalk-root had ~30.5% missing values. They were replaced with NaN and imputed using mode. 3.Methodology 🔹 Exploratory Data Analysis (EDA) Odor is the strongest predictor (certain odors → poisonous). Gill size: Broad = edible | Narrow = poisonous. Bruises & spore-print color also influence classification. Dataset is well-balanced. 🔹 Preprocessing One-Hot Encoding applied to categorical features. Missing values imputed. PCA tested for dimensionality reduction. 🔹 Modeling Implemented multiple algorithms:

Baseline: Logistic Regression Tree-based: Decision Tree, Random Forest Distance-based: KNN Margin-based: SVM Probabilistic: Naive Bayes Boosting & Bagging: Gradient Boosting, AdaBoost, Bagging, XGBoost Deep Learning: Artificial Neural Network (ANN) 🔹 Experimentation Multiple train-test splits tested: 60:40, 65:35, 70:30, 75:25, 80:20 Accuracy compared across splits for stability ANN trained with different architectures, regularization, and optimizers 4.Results ✅ ANN achieved the highest accuracy (100%) ✅ KNN also performed very well (99.75%) ✅ Gradient Boosting, Decision Tree, Logistic Regression, and SVM achieved ~96–97% ✅ Bagging, AdaBoost, and XGBoost showed ~94–96% accuracy ✅ Naive Bayes was the weakest (91.9%), but still acceptable
