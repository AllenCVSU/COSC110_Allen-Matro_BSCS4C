# Laboratory Activity 1: Computational Thinking with the Titanic Dataset using Python

## Description
This activity walks through a classic data‐science workflow on the Titanic passenger dataset. The activity goes through the following:
1. Mount Google Drive and load the CSV file.
2. Inspect and understand the data structure.
3. Identify and handle missing values.
4. Compute basic statistics (e.g. survival rate).
5. Visualize age distributions of survivors vs. non‑survivors.

Each step is presented as questions in the Jupyter notebook, with code cells followed by plain‑English descriptions of the computational thinking and algorithms used.

---

## Folder

Laboratory Activity 1

- `README.md` --> # This file
- `lab1_titanic_Matro,Eugene_Allen.ipynb` --> # Main notebook with all questions
- `titanic.csv` --> # Titanic dataset

---

## Requirements

- **Environment**: Google Colab or local Jupyter Notebook
- **Python**: 3.x
- **Libraries**:
  - `pandas`
  - `matplotlib`
- **Data**:
  - `titanic.csv` (place in `data/` folder or update path in the notebook)

---

## Setup

1. **Prepare the data**

   * If running Colab locally, ensure `data/titanic.csv` exists.
   * If using Colab with Google Drive, the first cell mounts Google Drive and loads the file from `/content/drive/MyDrive/train.csv`.

     ```python
     from google.colab import drive
     drive.mount('/content/drive')
     ```

2. **Install dependencies** (if needed)

   ```bash
   pip install pandas matplotlib
   ```

3. **Open the notebook**
   Launch `Laboratory_Activity_1.ipynb` in Jupyter or Colab and run all cells in order.

---

## Activity

### Question 1: Data Loading & Inspection

* **Objective**: Load the CSV into a DataFrame and preview its structure.
* **Key Steps**:

  1. Import `pandas`.
  2. Read CSV with `pd.read_csv()`.
  3. Use `df.head()`, `df.info()`, and `df.describe()` to inspect the first rows, data types, and summary statistics.
* **Notebook Cells**:

  * Cell “Mount & Load”
  * Cell “Inspect Data”

### Question 2: Handling Missing Values

* **Objective**: Detect, decide on, and apply strategies for missing data.
* **Key Steps**:

  1. Compute `df.isnull().sum()` to find which columns have nulls.
  2. **Drop** the `Cabin` column (77% missing).
  3. **Fill** `Age` with the median, `Embarked` with the mode.
  4. Re‑inspect with `df.info()` to confirm no remaining nulls.
* **Notebook Cells**:

  * Cell “Missing Value Analysis”
  * Cell “Apply Imputation & Drop”

### Question 3: Survival Rate Calculation

* **Objective**: Calculate the overall survival rate.
* **Key Steps**:

  1. Compute `df["Survived"].mean()`.
  2. Interpret the result as a percentage.
  3. Use conditional logic (if/else) to comment on whether most passengers survived or not.
* **Notebook Cells**:

  * Cell “Compute Survival Rate”
  * Cell “Interpretation”

### Question 4: Age Distribution Visualization

* **Objective**: Compare the age distribution of survivors vs. non‑survivors.
* **Key Steps**:

  1. Filter `df` by `Survived == 1` and `== 0`.
  2. Plot two overlapping histograms with `matplotlib.pyplot`.
  3. Compute and compare mean ages for each group.
  4. Write up computational‑thinking commentary.
* **Notebook Cells**:

  * Cell “Plot Age Distribution”
  * Cell “Compute Mean Ages & Interpretation”

---

## Notes

At each stage can be found a short text explanation of:

* **What** the code is doing.
* **Why** it’s structured that way.
* **How** it can be generalized to other datasets or problems.

These notes reinforce the algorithmic approach—breaking tasks down into inspection, transformation, analysis, and visualization.
