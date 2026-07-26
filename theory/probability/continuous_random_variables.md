## 


### Gaussian (Normal) Random Variable


### Gamma Random Variable



### Function of a Random Variable

Let $X$ be a random variable with probability density function $f_X(x)$ and let $g(x)$ be a real-valued function defined on the real line. </br>

Suppose that a new random variable $Y$ is determined by evaluating the function $g$ at all the values assumed by the random variable $X$. We define $Y = g(X)$. </br>

The probability density function of $Y$ can be derived from the probability density function of $X$ using the change of variables formula.  
The probability density function of $Y$ can be expressed as:

#### Case 1: Discrete Random Variable
If $X$ is a discrete random variable with probability mass function $p_X(x)$,

- Start with linear function. 
- Next apply square function.
- Then move to a general non-linear function. 
- Then take the special case of a bijective function. 


## Markov Inequality
- Provides a bound on the probability of an event when one has knowledge about the expected value of a non-negative random variable.
- Note this bound only applies to non-negative random variables, and it is not tight in general.

Formally, if X is a non-negative random variable and a > 0, then:

$$\Pr(X \ge a) \le \frac{\mathbb{E}[X]}{a}$$

### Proof: 

- Let $X$ be a non-negative random variable and $a > 0$. We can write:

$$\mathbb{E}[X] = \int_0^\infty x f_X(x) \, dx = \int_0^a x f_X(x) \, dx + \int_a^\infty x f_X(x) \, dx $$

- Since $x$ is non-negative, the first integral is non-negative, and we can bound the second integral as follows:

$$\mathbb{E}[X] \ge \int_a^\infty x f_X(x) \, dx $$

- Since, $a$ is the smallest value of $x$ in the second integral, we can further bound the second integral as follows:

$$\mathbb{E}[X] \ge \int_a^\infty a f_X(x) \, dx = a \int_a^\infty f_X(x) \, dx = a \Pr(X \ge a)$$

- By rearranging, we obtain the desired inequality:

$$\Pr(X \ge a) \le \frac{\mathbb{E}[X]}{a} $$



## Chebyshev Inequality

- Provides a bound on the deviation of a random variable from its mean when one has knowledge about the variance of the random variable.


## Chernoff Bound

- Provides a bound on the probability of that a random variable is greater than a certain value, as a function of the expected value of the exponential of the random variable.
- This is a more general bound than Markov's inequality and Chebyshev's inequality, and it can be used to derive tighter bounds in many cases.

## Characteristic Function: 




