# Programming-and-Algorithms-in-Bioinformatics
Postgraduate Assignment  — Advanced Algorithmic & Privacy Pipeline
## Part 1: Algorithmic Efficiency & Complexity

## 📈  Section 1: Asymptotic Complexity


In this part of the assignment, we attempt to examine five mathematical functions as representatives 
of common algorithmic complexity classes: linear, logarithmic-linear, polynomial, exponential, and factorial. To determine the dominance intervals of the given complexity functions, it is necessary to identify the 
intersection points where f(x) = g(x). These points represent thresholds at which one function overtakes 
another in terms of growth.  
Based on numerical analysis performed in the notebook, the following intervals were identified:
Interval [0.59 - 1.18] → Dominant Function: 2x (Exponential) 
Interval (1.18 - 9.24] → Dominant Function: x5 (Polynomial)
Interval (9.24 - ) → Dominant Function: x! (Factorial)
This analysis also confirms the theoretical hierarchy of algorithmic complexity:  
x< xlogx < x5 < 2x < x!  
### 💻 Python Implementation

The following code was used to analyze the functions and generate the visualization for the mid-range interval:

```python
import numpy as np
import matplotlib.pyplot as plt
from scipy.special import gamma

# Define the logarithmic-linear function
def nlogn(n):
    return n * np.log2(n)

# Create 1000 evenly spaced numbers in the mid-range interval
x = np.linspace(1.18, 9.24, 1000)

# Plotting the 5 complexity functions
plt.plot(x, x, label='x')
plt.plot(x, nlogn(x), label='x log(x)')
plt.plot(x, x**5, label='$x^5$')
plt.plot(x, 2**x, label='$2^x$')
plt.plot(x, gamma(x), label='Factorial x!')

# Focus on the vertical growth of this specific interval
plt.ylim(0, 80000)
plt.legend()
plt.savefig('λήψη.png')
plt.show()



