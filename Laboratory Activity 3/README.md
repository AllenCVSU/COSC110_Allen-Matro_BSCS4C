# Laboratory Activity 3: Introduction to SymPy

## Description
This activity is to learn the basics of symbolic mathematics in Python using the SymPy library:

1. Import the necessary SymPy modules.
2. Perform basic symbolic calculations (rationals, roots).
3. Define symbols and set up simple equations.
4. Simplify algebraic expressions.
5. Expand polynomial expressions.

Each step is laid out as a “Task” in the Jupyter notebook, with code cells followed by commentary explaining the computational thinking behind each operation.

---

## Folder

Laboratory Activity 3

- `README.md` --> # This file  
- `lab3_sympy_Matro,Eugene_Allen.ipynb` --> # Main notebook containing all tasks  

---

## Requirements

- **Environment**: Google Colab or local Jupyter Notebook  
- **Python**: 3.x  
- **Library**:
  - `sympy`

---

## Setup

1. **Install SymPy** (if needed)  

   `
   pip install sympy
   `

3. **Open the notebook**

   Launch `lab3_sympy_Matro,Eugene_Allen.ipynb` in Jupyter or Colab and run all cells sequentially.

---

## Activity

### Task 1: Import SymPy Modules

* **Objective**: Bring in all core functions and classes from SymPy.
* **Key Code**:

  `
  from sympy import *
  `

### Task 2: Basic Symbolic Calculations

* **Objective**: Compute exact values and their decimal approximations.
* **Expressions**:

  1. $(5/3) + (\sqrt{10}/2)$

     * Use `Rational(5, 3) + sqrt(10)/2`
     * Display both `evalf()` and pretty‑printed form.
  2. $\sqrt{50} \times \sqrt{5/9}$

     * Use `sqrt(50) * sqrt(Rational(5, 9))`
     * Show exact and decimal forms.

### Task 3: Defining Symbols & Equations

* **Objective**: Create symbolic variables and form equations.
* **Key Code**:

  `
  x, y = symbols('x y')
  eq1 = Eq(2*x + 3*y, 12)
  eq2 = Eq(x - y, 4)
  `
* **Goal**: Understand how to represent and display equations in SymPy.

### Task 4: Simplification

* **Objective**: Reduce complex rational expressions to simpler form.
* **Expressions**:

  1. $\frac{x^2 + 2x + 1}{x + 1}$ → `simplify((x**2+2*x+1)/(x+1))`
  2. $\frac{1 - \frac{1}{1 + \frac{1}{x}}}{1 + \frac{1}{x}}$ → simplify nested fractions.
* **Outcome**: Use `simplify()` to see how SymPy rewrites expressions.

### Task 5: Expansion

* **Objective**: Multiply out polynomial expressions.
* **Expressions**:

  1. $(2x + 2)^2$ → `expand((2*x+2)**2)`
  2. $(2x + y)\,(x - 2y)$ → `expand((2*x+y)*(x-2*y))`
* **Outcome**: See how `expand()` distributes and combines like terms.

---

## Notes

* Each notebook cell is followed by a brief write-up explaining **what** the code does, **why** this approach is used, and **how** these methods generalize to other symbolic problems.
* Make sure to run all cells from top to bottom to confirm that imports, definitions, and computations execute without errors.
