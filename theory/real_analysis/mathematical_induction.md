## Mathematical Induction

- Pre-reqs: Basic understanding of natural numbers, the notion of less than or equal to, and the well ordering property of natural numbers.

    The well ordering property states that every non-empty set of natural numbers has a least element. This property is fundamental in proving statements about natural numbers.

### Basic Principle of Mathematical Induction

Let $S$ be a subset of the natural numbers $\mathbb{N}$. If the following two conditions are satisfied:

1. **Base Case**: The number 1 is in $S$ (i.e., $1 \in S$).
2. **Inductive Step**: For every natural number $k$, if $k \in S$, then $k + 1 \in S$.

Then $S$ contains all natural numbers, i.e., $S = \mathbb{N}$

### Proof: Quite ingenious

- We prove the principle by contradiction. 

- Assume that $S \neq \mathbb{N}$. Then the set $\mathbb{N} \setminus S$ is non-empty. By the well ordering property, it has a least element, say $m$.
- Since $m$ is the least element not in $S$, we must have $m > 1$ (because $1 \in S$).
- If $m > 1$, then $m - 1$ is a natural number. 
- This means that $m - 1 \in S$ (since $m$ is the least element not in $S$).
- By the inductive step, $m - 1 \in S$ implies $m \in S$, which is a contradiction.
- Hence, our assumption is false, and $S = \mathbb{N}$.


## Generalized Mathematical Induction (TODO): 

## Applications of Mathematical Induction:

1. Proving formulas for sums of sequences (e.g., sum of the first n natural numbers, sum of squares, etc.).
    - The formula for the sum of the first n natural numbers is given by:
    $$
    S_n = 1 + 2 + 3 + \ldots + n = \frac{n(n + 1)}{2}
    $$
    - Proof: Show that the formula holds for the base case (n=1). 
    - Next, assume it holds for some arbitrary natural number k, i.e.,
    $$
    S_k = 1 + 2 + 3 + \ldots + k = \frac{k(k + 1)}{2}
    $$
    - Then, show that it holds for k + 1 (can be done by adding (k + 1) to both sides of the equation for S_k and simplifying):
    $$
    S_{k+1} = 1 + 2 + 3 + \ldots + k + (k + 1) = \frac{(k + 1)(k + 2)}{2}
    $$
    
2. Proving inequalities (e.g., AM-GM inequality, Bernoulli's inequality).
3. Proving properties of divisibility (e.g., if a number is divisible by a certain integer, then so is its multiple).
4. Proving properties of sequences and series (e.g., Fibonacci sequence, geometric series).
5. Proving properties of functions defined recursively (e.g., factorial function, Fibonacci function).
6. Proving properties of combinatorial objects (e.g., binomial coefficients, permutations, combinations).
7. Proving properties of graphs and trees (e.g., number of edges in a tree, properties of connected graphs).
8. Proving properties of algorithms (e.g., correctness of recursive algorithms, time complexity analysis).
9. Proving properties of mathematical structures (e.g., groups, rings, fields).
10. Proving properties of mathematical games (e.g., winning strategies, game invariants).
11. Proving properties of mathematical logic (e.g., tautologies, logical equivalences).
12. Proving properties of mathematical induction itself (e.g., strong induction, transfinite induction).

