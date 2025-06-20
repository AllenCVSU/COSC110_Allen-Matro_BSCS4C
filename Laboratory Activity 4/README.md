# Laboratory Activity 4: Exploring Calculus using SymPy	

## Description

This activity demonstrates how Python’s SymPy library can be used to explore foundational ideas in calculus without manual derivations:

1. Play with symbolic variables and operations.
2. Investigate limits of functions.
3. Compute derivatives of expressions.
4. Generate series expansions.
5. Solve algebraic equations.
6. Reflect on your learning.

Each step appears as a “Task” in the Jupyter notebook, with code snippets followed by prompts and space for observations.

---

## Folder

Laboratory Activity 4

* `README.md` --> # This file
* `lab4_sympy_Matro,Eugene_Allen.ipynb` --> # Main notebook containing all tasks

---

## Requirements

* **Environment**: Google Colab or local Jupyter Notebook
* **Python**: 3.x
* **Library**:

  * `sympy`

---

## Setup

1. **Install SymPy** (if needed):

   `
   pip install sympy
   `
   
2. **Open the notebook**:
   Launch `lab4_calculus_sympy_Matro,Eugene_Allen.ipynb` in Jupyter or Colab and run all cells in order.

---

## Activity

### Task 1: Playing with Symbols

* **Objective**: See how SymPy treats symbols algebraically.
* **Key Code**:

  `
  x = symbols('x')
  x + x      # outputs 2*x
  x * x      # outputs x**2
  `
  
* **Prompt**: Explain what `x + x` and `x * x` represent.

### Task 2: Exploring Limits

* **Objective**: Compute the limit of a function as a variable approaches a value.
* **Key Code**:

  `
  limit(sin(x)/x, x, 0)  # outputs 1
  `
  
* **Prompt**: Describe the result and its meaning.

### Task 3: Playing with Derivatives

* **Objective**: Find the derivative of a polynomial.
* **Key Code**:

  `
  diff(x**2, x)  # outputs 2*x
  `
  
* **Prompt**: Interpret the derivative of $x^2$.

### Task 4: Series Expansion

* **Objective**: Generate the Taylor series expansion of an exponential function.
* **Key Code**:

  `
  exp(x).series(x, 0, 4)
  # outputs 1 + x + x**2/2 + x**3/6 + O(x**4)
  `
  
* **Prompt**: How many terms are shown? What does the `O(x**4)` indicate?

### Task 5: Solving Equations

* **Objective**: Solve a quadratic equation symbolically.
* **Key Code**:

  `
  solve(Eq(x**2 - 4, 0), x)  # outputs [-2, 2]
  `
  
* **Prompt**: Identify the solutions and classify the type of equation.

### Task 6: Final Thoughts

* **Objective**: Reflect on your experience.
* **Prompts**:

  1. What was your favorite part of the activity?
  2. What surprised you or what new insight did you gain?

---

## Notes

* Each code cell is followed by space for answers and reflections.
* Explanations in the notebook guide to focus on *what* the result is, *why* it works that way, and *how* to extend the idea.