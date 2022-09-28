## DSA -Analysis

we have some steps to construct an algorithms, In those steps analysis is the last one. But before start the Problem solving we need to study the analysis part very well then only we can see our algorithms works well or not.

To find optimized code we need two mater to consider.
 
1. Time complexity
2. Space Complexity

Our Target should be lesser Time complexity and lower space complexity. Nowadays Time is more important than space as we can configure extra space today. Time machine is not available now. 

### Asymptotic Notations:

1. Big O -> Worst case scenario (Important
2. Omega -> Best case scenario 
3. Theta -> Average case scenario

There are two types of analysis:
1. **A posterior Analysis **- Depends on language, compiler and type of hardware used - Exact analysis
2. **A priory Analysis **- Independent of language, compiler and type of hardware used - Approximate analysis - Big O

# A priory Analysis:
Order of magnitude of a statement i.e A number of times any statement can run

### Notes:
- A time complexity is loop only
- Not only loops, a single statement also considerable but we should consider always bigger numbers.
- If there is no loop, time complexity is O(1)

## Complexity classes:

1.  Constant - O(1)
2.  Lograthemic - O(log n)
3.  Linear - O(n)
4.  Quadratic - O(n\square)
5. Cubic - O(n3)
6. Polynomial -  O(nc)
7.  Exponential - O(Cn)
