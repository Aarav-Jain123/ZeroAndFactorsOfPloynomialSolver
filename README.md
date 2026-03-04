# Polynomial Root Solver using SymPy (Jupyter Notebook)

## Overview

This Jupyter Notebook demonstrates how to use the **SymPy** library in Python to symbolically define and solve a polynomial equation. The notebook walks through creating symbolic variables, defining a polynomial expression, computing its roots, and converting the symbolic solutions into numerical complex values.

This example highlights **symbolic mathematics in Python**, which is useful for algebra, calculus, and analytical computations.

---

## Features

* Creates symbolic variables using SymPy
* Defines a polynomial expression
* Computes exact symbolic roots of the polynomial
* Converts symbolic results into numerical complex values

---

## Requirements

Install the required Python package before running the notebook:

```bash
pip install sympy
```

Recommended environment:

* Python 3.x
* Jupyter Notebook / JupyterLab
* SymPy

---

## Code Explanation

### 1. Import SymPy

```python
import sympy as smp
```

The `sympy` library is imported and aliased as `smp` for convenience.

---

### 2. Create a Symbolic Variable

```python
x = smp.symbols('x')
x
```

* `smp.symbols()` creates a symbolic variable.
* This allows algebraic manipulation instead of numerical computation.

---

### 3. Define the Polynomial

```python
p = 7*x**5 - 3*x**4 + 12*x**3 - x**2 + 9*x - 6
```

This defines the polynomial:

[
7x^5 - 3x^4 + 12x^3 - x^2 + 9x - 6
]

---

### 4. Solve the Polynomial

```python
roots = smp.solve(p, x)
roots
```

* `smp.solve()` finds the roots of the polynomial.
* The results are returned symbolically.
* Some solutions may contain complex numbers expressed with `I` (imaginary unit).

---

### 5. Convert Symbolic Roots to Numeric Values

```python
[complex(r.evalf()) for r in roots]
```

* `evalf()` converts symbolic expressions to floating-point numbers.
* `complex()` converts them into standard Python complex numbers.

This makes the results easier to interpret numerically.

---

## Example Output

Symbolic solutions may appear like:

```
-1/2 - sqrt(3)*I/2
-1/2 + sqrt(3)*I/2
...
```

After conversion:

```
(-0.5-0.866j)
(-0.5+0.866j)
...
```

---

## Learning Goals

This notebook demonstrates:

* Symbolic algebra in Python
* Polynomial root finding
* Handling symbolic and numeric representations
* Working with complex numbers

---

## Possible Extensions

You could expand this notebook by:

* Plotting the polynomial
* Visualizing real vs complex roots
* Allowing user input for polynomial coefficients
* Comparing symbolic vs numerical solvers
* Factoring the polynomial using SymPy

Example:

```python
smp.factor(p)
```

---

## License

This project is intended for educational purposes.
