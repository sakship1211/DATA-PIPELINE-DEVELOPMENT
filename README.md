#  Titanic ETL Pipeline

##  Project Objective

Build an **automated, reproducible, and scalable ETL pipeline** for the Titanic dataset using Python, Pandas, and Scikit-learn.

This pipeline handles:
- Data ingestion
- Cleaning and transformation
- Feature extraction & encoding
- Splitting & exporting clean data for modeling

---

##  Dataset

- Source: [Kaggle Titanic Dataset](https://www.kaggle.com/c/titanic/data)
- Files used: `train.csv` (uploaded locally)

---

##  ETL Steps

1. **Data Ingestion**  
   Load the Titanic training dataset from CSV using `pandas`.

2. **Feature Extraction**  
   - Extracted passenger **Title** (Mr, Mrs, etc.) from the `Name` column.
   - Grouped rare titles under `'Rare'`.

3. **Feature Engineering**  
   - Created a new feature: **FamilySize** = `SibSp + Parch + 1`.

4. **Data Cleaning**  
   - Dropped unnecessary columns: `PassengerId`, `Ticket`, `Cabin`, `Name`.
   - Filled missing values in `Embarked` with the mode.
   - Imputed missing values in numeric columns using median.

5. **Categorical Encoding**  
   - Encoded `Sex`, `Embarked`, and `Title` using `LabelEncoder`.

6. **Feature Scaling**  
   - Scaled `Age`, `Fare`, and `FamilySize` using `StandardScaler`.

7. **Data Splitting**  
   - Split the cleaned dataset into training and testing sets (80/20).

8. **Export**  
   - Saved the final cleaned dataset to `titanic_cleaned.csv`.

---

##  Tools & Libraries

- `Python 3.8+`
- `pandas`
- `numpy`
- `scikit-learn`

---

##  Output

- `titanic_cleaned.csv`: Fully cleaned and transformed dataset
- `Titanic_ETL_Pipeline_Final_Submission.ipynb`: Notebook with the entire automated pipeline

---

## ✅ Notes

- This ETL pipeline is modular and easily extendable for future model integration.
- Categorical encoding is done manually for better control and understanding.
# DATA-PIPELINE-DEVELOPMENT
