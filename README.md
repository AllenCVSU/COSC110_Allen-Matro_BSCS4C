```markdown
# Laboratory Activity 1: Titanic Dataset Analysis

## Description
This activity walks you through a classic data‐science workflow on the Titanic passenger dataset. You will:
1. Mount Google Drive (if using Colab) and load the CSV file.
2. Inspect and understand the data structure.
3. Identify and handle missing values.
4. Compute basic statistics (e.g. survival rate).
5. Visualize age distributions of survivors vs. non‑survivors.

Each step is presented as a separate “question” in the Jupyter notebook, with code cells followed by plain‑English descriptions of the computational thinking and algorithms used.

---

## 📂 Folder Structure

```

Laboratory Activity 1/
├── Laboratory\_Activity\_1.ipynb    # Main notebook with all questions (1–4)
├── README.md                      # This file
└── data/
└── titanic.csv                # Titanic dataset (copy into this folder or update path)

````

---

## ⚙️ Requirements

- **Environment**: Google Colab or local Jupyter Notebook
- **Python**: 3.x
- **Libraries**:
  - `pandas`
  - `matplotlib`
- **Data**:
  - `titanic.csv` (place in `data/` folder or update path in the notebook)

---

## 🚀 Setup Instructions

1. **Clone the repository**  
   ```bash
   git clone https://github.com/your‑username/your‑repo.git
   cd your‑repo/"Laboratory Activity 1"
````

2. **Prepare the data**

   * If running locally, ensure `data/titanic.csv` exists.
   * If using Colab, the first cell mounts your Google Drive and loads the file from `MyDrive/AAA_datasets/titanic/titanic.csv`.

     ```python
     from google.colab import drive
     drive.mount('/content/drive')
     ```

3. **Install dependencies** (if needed)

   ```bash
   pip install pandas matplotlib
   ```

4. **Open the notebook**
   Launch `Laboratory_Activity_1.ipynb` in Jupyter or Colab and run all cells in order.

---

## Activity Breakdown

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
  4. Write up your computational‑thinking commentary.
* **Notebook Cells**:

  * Cell “Plot Age Distribution”
  * Cell “Compute Mean Ages & Interpretation”

---

## Computational Thinking Notes

At each stage you’ll find a short text explanation of:

* **What** the code is doing.
* **Why** it’s structured that way.
* **How** it can be generalized to other datasets or problems.

These notes reinforce the algorithmic approach—breaking tasks down into inspection, transformation, analysis, and visualization.
