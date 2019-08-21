# 2 Getting Started

## 2.1 Insertion Sort
### Pseudocode
![](https://github.com/camilaferno/ADA/blob/master/Libros/images/Cormen2_1.png)
### Diagrama 
![](https://github.com/camilaferno/ADA/blob/master/Libros/images/Cormen2_2.png)
### Loop invariants and correctness of insertion sort
#### Loop invariants
**Loop invariant of insertion sort** The subarray A[1..j-1] because the elements are the same as before but now in a sorted order.
#### Correctness
Loop invariants can help us understand why an algorithm is correct.

We must show three things about a loop invariant:
1. Initialization: It is true prior to the first iteration of the loop.
2. Maintenance: It is true before the iteretaion of the loop and it remains true before the next iteration
3. Termination: When the loop terminates, the invariant gives us a useful property that helps show that the algorithm is correct.

Proof that the algorithm is correct
1. Initialization: We start by showing that the loop invariant holds before the first loop iteration, when j=2 The subarray A[1..j-1] therefore, consists of just the single element A[1], which is in fact the **original** element in A[1]. Moreover, this subarray is **sorted** (trivially, of course), which shows that the loop invariant holds prior to the first iteration of the loop.
2. Maintenance: Informally, the body of the for loop works by moving A[j-1], A[j-2], A[j-3] and so on by one position to the right until it finds the proper position for A[j] (lines 4–7), at which point it inserts the value of A[j]􏰀 (line 8). The subarray A[1..j]then consists of the elements originally in A[1..j]􏰀, but in sorted order. Incrementing j for the next iteration of the for loop then preserves the loop invariant.
3. Termination: The condition causing the for loop to terminate is that j > A.length = n. Because each loop iteration increases j by 1, we must have j = n+1 at that time. Substituting n+1 for j in the wording of loop invariant, we have that the subarray A[1..n] consists of the elements originally in A[1..n] but in sorted order. Observing that the subarray A[1..n] is the entire array, we conclude that the entire array is sorted. Hence, the algorithm is correct.

## 2.2 Analyzing Algorithms
Analyzing algorithms for this book means measuring the computational time. This book measures it by the RAM model in which none of the instructions are executed concurrently.
### Analysis of Insertion Sort
In general, the time taken by an algorithm grows with the size of the input, so it is traditional to describe the running time of a program as a function of the size of its input. To do so, we need to define the terms “running time” and “size of input”.
1. Size of input: Depends on the problem being studied
- **Sorting: Number of elements in array**
- Multiplying two integers: Total number of bits needed to represent the number in binary.
- Graph: Two numbers, vertices and edges.
2. Running time: Number of primitive operations or “steps” executed.
Each step takes a constant time to do.
