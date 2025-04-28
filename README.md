
## 📊 Objective

To extract insights using visual and statistical exploration.

## 🛠️ Tools & Libraries

- Python 3.x
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## Load the Data
```python
import pandas as pd

Titanic_train_df = pd.read_csv('train.csv')
Titanic_test_df = pd.read_csv('test.csv')
```

## Understanding the Dataset structure
```python
#Get summary of dataset
Titanic_train_df.info()

#Summary statistics
Titanic_train_df.describe()
```

## Check and Handle Missing Values
```python
# Count missing values
Titanic_train_df.isnull().sum()

# Fill missing Age with median
Titanic_train_df['Age'].fillna(Titanic_train_df['Age'].median(), inplace=True)

# Fill missing Embarked with mode
Titanic_train_df['Embarked'].fillna(Titanic_train_df['Embarked'].mode()[0], inplace=True)
# Fill missing Fare with median
Titanic_test_df['Fare'].fillna(Titanic_test_df['Fare'].median(), inplace=True)

# Drop Cabin due to too many missing values (optional)
Titanic_train_df.drop(columns=['Cabin'], inplace=True)

````
## 📈 Visualizations

Key visualizations include:

- Histograms of Age and Fare
  
![download](https://github.com/user-attachments/assets/f4ce68f3-278f-4995-a7e2-6023d25564e7)

- Countplots for Categorical Features
  
![download](https://github.com/user-attachments/assets/35529d3d-ef0b-4f2c-83c9-cd810af99022)

- Boxplot for Age and Survived
  
![download](https://github.com/user-attachments/assets/388e98a3-d6bc-4b69-8b33-e1957bb270e5)

- Boxplot for Fare and Survived
  
![download](https://github.com/user-attachments/assets/d3702dbc-09b6-4567-8a69-42504a03eaf6)

- Countplots for Survival by Categorical Features
  
![download](https://github.com/user-attachments/assets/28aa5bb4-2954-4c74-af06-322e7c4b0f1a)

- Correlation Heatmap
  
![download](https://github.com/user-attachments/assets/2becbdbe-b897-4e79-919d-fb5166a891ca)

- Pairplot for Pclass, Age and Fare

![download](https://github.com/user-attachments/assets/aedfe3f6-bc8a-40da-80f7-bae9e4e15eae)

- Age distribution histograms
  
![download](https://github.com/user-attachments/assets/f3ebdd34-cdfb-49bd-ac04-c9c57d6e9daf)

- Fare distribution histograms
  
![download](https://github.com/user-attachments/assets/b4762aed-a04f-47f1-99c2-8e268bd0f2d9)

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

