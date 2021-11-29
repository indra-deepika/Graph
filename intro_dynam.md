# 🐾: Introduction to Dynamic Programming 

<p>Dynamic programming is a technique that combines the correctness of complete search and the efficiency of greedy algorithms. Dynamic programming can be applied if the problem can be divided into overlapping subproblems that can be solved independently. </p>

<p>Dynamic programming is basically, recursion plus using common sense. In recursion, the same function can be called multiple times with the same arguments. In other words, the same result is calculated multiple times instead of just once. In dynamic programming, a recursive function is optimized by storing the intermediate results in a data structure and this process is called <b>Memoization</b> (memorizing or storing the values of some states so that they can be used while solving other subproblems) The intuition behind dynamic programming is that we trade space for time, i.e. to say that instead of calculating all the states taking a lot of time but no space, we take up space to store the results of all the sub-problems to save time later.</p>

Let us understand this better with the help of an example:

We are required to calculate the nth Fibonaci number. Let us see how the same problem can be solved by recursion and by dynamic programming to understand the difference and understand how dynamic programming is effective.

#### Recursion 

```
int fib (int n) {
        if (n < 2)
            return 1;
        return fib(n-1) + fib(n-2);
    }
```
<!-- Insert pic -->
Here the function fib is called 2 times once for n-1 and again for n-2 and hence the time complexity for the following becomes O(2<sup>n</sup>).

#### Dynamic Programming 

```
void fib () {
        fibresult[0] = 1;
        fibresult[1] = 1;
        for (int i = 2; i<n; i++)
           fibresult[i] = fibresult[i-1] + fibresult[i-2];
    }

```
Here we can see that by the time we have to compute fibresult[i], we already have computed the values of fibresult[i-1] , fibresult[i-2]. So we can see that the above function is linear ie Time complexity O(N).


<p>Dynamic Programming is used to solve 2 types of problems:

- Finding an optimal solution: We want to find a solution that is as large
as possible or as small as possible.
- Counting the number of solutions: We want to calculate the total number of possible solutions </p>

#### Every Dynamic Programming problem has a schema to be followed:

<!-- - Show that the problem can be broken down into optimal sub-problems.
- Recursively define the value of the solution by expressing it in terms of optimal solutions for smaller sub-problems.
- Compute the value of the optimal solution in bottom-up fashion.
- Construct an optimal solution from the computed information. -->

- It breaks down the complex problem into simpler subproblems.
- It finds the optimal solution to these sub-problems.
- It stores the results of subproblems (memoization). The process of storing the results of subproblems is known as memorization.
- It reuses them so that same sub-problem is calculated more than once.
- Finally, calculate the result of the complex problem. 


