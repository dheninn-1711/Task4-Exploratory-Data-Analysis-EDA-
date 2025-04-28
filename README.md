
## 📊 Objective

To understand and visualize the relationships between survival and other key features like gender, class, fare, and age, and to prepare data for predictive modeling.

## 🛠️ Tools & Libraries

- Python 3.x
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## 📈 Visualizations

Key visualizations include:

- Bar plots of survival by gender and class
- Age distribution histograms
- Correlation heatmaps
- Fare distribution vs. survival status

## 🚧 Future Work

- Feature engineering (e.g., family size, title extraction)
- Imputation strategies for missing data
- Predictive modeling (logistic regression, random forests, etc.)
- Hyperparameter tuning and cross-validation

## 📁 Data Source

- [Kaggle Titanic Dataset](https://www.kaggle.com/c/titanic/data)


## 🔍 Summary of Findings

- **Gender**: Females had significantly higher survival rates than males.
- **Class**: 1st class passengers were more likely to survive than those in 2nd or 3rd class.
- **Age**: Children under 15 had a better chance of survival.
- **Fare**: Higher fare correlates with higher survival.
- **Embarked**: Passengers from Cherbourg (C) had higher survival rates than those from Queenstown (Q) or Southampton (S).
- **Correlation**:
  - `Pclass` is negatively correlated with `Survived`.
  - `Fare` is positively correlated with `Survived`.
- **Missing Data**:
  - **Age** and **Cabin** contain missing values.
- **Test Dataset**: Shows a similar distribution to the training dataset, suitable for model validation.

