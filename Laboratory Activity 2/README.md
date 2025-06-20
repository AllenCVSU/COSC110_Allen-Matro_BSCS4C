# Laboratory Activity 2: Data Cleaning and Analysis using Titanic dataset

## Description
This activity is a practice of full data‑preparation workflow followed by basic exploratory visualizations using the Titanic passenger dataset:

1. Mount Google Drive and load the raw CSV (`train.csv`).
2. Inspect the data structure and summary statistics.
3. Identify and handle missing values.
4. Remove duplicate records.
5. Fix data types and standardize column names.
6. Save the cleaned dataset (`titanic_cleaned.csv`).
7. Create basic visualizations:
   - Bar plot of total survivors vs. non‑survivors
   - Histogram of passenger age distribution
   - Bar chart of survival rate by gender
   - Bar chart of survival rate by passenger class

Each step is presented in the Jupyter notebook with code cells followed by commentary on the thinking behind each transformation.

---

## Folder

Laboratory Activity 2

- `README.md` --> # This file
- `lab2_titanic_Matro,Eugene_Allen.ipynb` --> # Main notebook with all questions
- `titanic.csv` --> # Titanic dataset 

---

## Requirements

- **Environment**: Google Colab or local Jupyter Notebook  
- **Python**: 3.x  
- **Libraries**:  
  - `pandas`  
  - `matplotlib`  
- **Data**:  
  - `train.csv` (place in the same folder or adjust path in the notebook)  

---

## Setup

1. **Mount Google Drive** (if using Colab)  

   `
   from google.colab import drive
   drive.mount('/content/drive')
   `

3. **Load the data**

   `
   import pandas as pd
   df = pd.read_csv("/content/drive/MyDrive/train.csv")
   `
4. **Install dependencies** (if needed)

   `
   pip install pandas matplotlib
   `
   
5. **Open the notebook**
   Launch `lab2_titanic_Matro,Eugene_Allen.ipynb` in Jupyter or Colab and run all cells sequentially.

---

## Activity

### Question 1: Data Preparation & Cleaning

**Objective:** Apply a systematic cleaning pipeline to prepare the Titanic data for analysis.

**Steps Covered:**

1. **Mount & Load**

   * Mount Google Drive (Colab).
   * Read `train.csv` into a DataFrame.

2. **Inspect & Understand**

   * Use `df.info()`, `df.describe()`, and `df.columns` to examine data types, summary statistics, and column names.

3. **Check for Missing Values**

   * `df.isnull().sum()` to quantify nulls in each column.

4. **Handle Missing Values**

   * Fill `Age` with its median value.
   * Drop the `Cabin` column due to excessive missingness.
   * (Optionally) fill or drop any remaining nulls in `Embarked`.

5. **Remove Duplicates**

   * `df.duplicated().sum()` to detect duplicates.
   * `df.drop_duplicates(inplace=True)` to remove them.

6. **Fix Data Types**

   * Convert `Survived` and `Pclass` to `category` dtype for efficient grouping.

7. **Standardize Column Names**

   * Lowercase all column names with `df.columns = df.columns.str.lower()`.

8. **Save Cleaned Dataset**

   * Export to `titanic_cleaned.csv` via `df.to_csv("titanic_cleaned.csv", index=False)`.

---

### Question 2: Basic Exploratory Visualizations

**Objective:** Generate simple plots to reveal key patterns in the cleaned data.

**Plots Included:**

1. **Survival Count Bar Plot**

   * `df["survived"].value_counts().plot(kind="bar")`
   * Titles and axis labels added for clarity.

2. **Age Distribution Histogram**

   * `df["age"].plot(kind="hist", bins=20, edgecolor="black")`
   * Shows overall age spread.

3. **Survival Rate by Gender**

   * Convert `survived` to `int` and `sex` to `str`.
   * `df.groupby("sex")["survived"].mean().plot(kind="bar")`
   * Highlights “women and children first” effect.

4. **Survival Rate by Passenger Class**

   * `df.groupby("pclass")["survived"].mean().plot(kind="bar")`
   * Reveals socioeconomic disparities in survival.

Each plot is followed by a brief interpretation of the insights gained.

---

## Notes

* Commentary in the notebook explains **what** each code block does, **why** that operation is applied, and **how** it generalizes to other datasets.
