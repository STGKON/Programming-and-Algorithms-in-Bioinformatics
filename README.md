# Programming-and-Algorithms-in-Bioinformatics
Postgraduate Assignment Report — Advanced Algorithmic & Privacy Pipeline
Part 1: Algorithmic Efficiency & Complexity

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


## Section 2: Sorting Benchmarks (5-Second Timeout)
In this part, three sorting algorithms were evaluated under a 5-second execution constraint:
Brute Force Sort  
▪ Maximum input within 5 seconds: 10 elements (factorial growth: O(n!)). 

Bubble Sort 
▪ Maximum input within 5 seconds: ~ 7500 elements (quadratic growth: O(n2)). 

 QuickSort 
 ▪ Maximum input within 5 seconds:  ~ 1.200.000 elements (divide-and-conquer: O(nlogn)).
 These results clearly demonstrate that the growth rate of an algorithm is the dominant factor in 
performance, rather than raw hardware speed. 
This analysis highlights the importance of selecting algorithms with suitable asymptotic growth for 
large inputs. While simple algorithms may suffice small arrays, more efficient algorithms like 
QuickSort are essential for scaling to larger datasets.  
 
